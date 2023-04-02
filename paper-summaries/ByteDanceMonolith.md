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

