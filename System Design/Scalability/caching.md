## CACHING

### What is a cache? 
A cache is a small memory, fast-access local store to store frequently accessed data. It stores copies of frequently used application data in a layer of smaller, faster memory in order to improve data retrieval times, throughout and compute costs.

### What is locality?
Caching is based on the principal of locality. There are two kinds: 
1. Temporal Locality: Data that has been referenced recently is likely to be referenced again. 
2. Spatial Locality: Data that is stored near recently referenced data is also likely to be referenced again.  

### How does a cache work? 
If a copy of the data is in a cache, then it's a *cache hit*. If it's not, then it's a *cache miss*.

_Diagram 1_:
![Cache Miss and Hit](../../img/cache_miss_hit.png)

[Image Source](https://medium.com/geekculture/system-design-basics-caching-46b1614915f8)


### What are the types of caches?
* Application Server Cache:
* Distributed Cache:
* Global Cache:


#### Sources:
- [System Design Basics: Caching](https://medium.com/geekculture/system-design-basics-caching-46b1614915f8) - An article on Medium discussing the basics of caching in system design.
