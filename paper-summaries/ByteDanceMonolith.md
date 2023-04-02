## ByteDance Monolith

https://www.tiktok.com/@brookebytes/video/7165959125925448962
https://arxiv.org/pdf/2209.07663.pdf

- Better collisionless embedding
- Better real time training - loops

### Problem

Typical PyTorch and TF models don't work well because they are designed for batch training which is bad for the real-time training that TikTok depends on. Additionally, the feature structure varies highly and is dense, which isn't easily accomodated by this architecture -- constantly changing vectors because of changing trends on TikTok, and highly sparse because there's a huge variety of features that different pieces of content may not have (it looks like there wasn't a good way to get collision-less with typical arch).

### Solution

Collision-less embedding optimizations:
- Expirable embeddings
- Frequency filtering to reduce memory footprint

Online Training:
- High fault-tolerance
- Lose reliability for online learning

### Problem again, this time more simply

- Features are sparse as individual pieces of data may only fit in a couple of categories
- Undelrying distribution of training data is non-stationary (content keeps getting created)

### Solution, this time pretty much the same lmfao

- Collisionless hash table + dynamic feature eviction
- Loop serving feedback to training in real-time w/ online training

### Performance Metric

Online serving AUC - Performance of real-time recommendation system. Measures accuracy in making recommendations to users while system is in production and serving live traffic. AUC is "Area Under Curve", measuring area under curve plotting true positive rate vs false positive rate.

### Design

- Worker-Parameter Server arch, workers access param servers for weights
- Custom trained HashTable alternative to a trained TF Variable based embedding. The HashTable is based on the Cuckoo Hashmap, and additionally filters adding IDs based on incoming frequency and evicts IDs based on usage.
- Online Training: optimize by updating sparse parameters more frequently (they're also more relevant to recommendations). This optimizes for bandwidth usage and memory
- Fault Tolerance: 1 Day snapshots of PS captured, works well enough for them
