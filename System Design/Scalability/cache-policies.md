## Cache Writing Policies
A cache policy is a set of rules which define how the data will be loaded and evicted from a cache memory. A cache is made of copies of data and is transient storage. When writing, we need to decide when to write to the cache and when to write to the primary data store.

### Write-Through Caching
| ABOUT                                    | PROS                                     | CONS                                            |
|------------------------------------------|------------------------------------------|-------------------------------------------------|
| Data is written into the cache and DB at the same time | Cache ensures fast retrieval              | Every write operation is done 2x which leads to more latency |
|                                          | Complete consistency between cache and DB |                                                 |

* **Characteristics:** 
  * Data is written to the cache and the primary data store simultaneously. 
  * This ensures consistency between the cache and the storage but can result in higher latency for write operations.
* **Common Usage:** 
  * Preferred in scenarios where data consistency and safety are critical, such as financial transactions or other mission-critical applications.

![Write-Through](https://miro.medium.com/v2/resize:fit:720/format:webp/1*44jAwLEit1u8bcwnbrroGw.png)

### Write-Around Caching
| ABOUT                                               | PROS                                                         | CONS                                                      |
|-----------------------------------------------------|--------------------------------------------------------------|-----------------------------------------------------------|
| Data is written directly to the primary data store. | The primary data store always being consistent.              | Cache might be behind the primary storage at times.        |
| Cache checks with the primary data store to sync.   |  |                                                           |

* **Characteristics:** 
  * Data is written directly to the primary data store, bypassing the cache. 
  * The cache is then updated to reflect this change. 
  * This reduces the cache being flooded with write operations, but can lead to a temporary inconsistency until the cache is updated.
* **Common Usage:** 
  * Useful in read-heavy environments where it's important to not overload the cache with write operations that are not frequently accessed.

![Write-Around](https://miro.medium.com/v2/resize:fit:720/format:webp/1*6kTs8J9JUBSAEDKaTAkepQ.png)

### Write-Back Caching 
| ABOUT                                                                                                                                 | PROS                                                                                    | CONS                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| Data is written into the cache first, then into the primary data store. The cache may update the primary store immediately or upon entry removal marked by a dirty bit. | Used in write-heavy operations where write speed is critical.                             | Prone to data loss if the cache is not persisted. |

* **Characteristics:** 
  * Data is initially written to the cache only and later written to the primary data store, usually when the cache is full or the data is no longer needed (marked with a dirty bit). 
  * This can significantly improve write performance but risks data loss if the cache is not properly synchronized before a failure occurs.
* **Common Usage:** 
  * Suited for write-heavy and performance-sensitive applications where the risk of data loss is mitigated by other factors like frequent backups or non-volatile cache memory.

![Write-Back](https://miro.medium.com/v2/resize:fit:720/format:webp/1*VpzJCKqQHKq7MvtqRaTy4Q.png)

## Cache Eviction Policies
Cache eviction policies define a set of rules that decide what data must be removed when the cache is full and a new entry is to be added. 

A good replacement policy will ensure that the cached data is as relevant as possible to the app and that it used the principle of locality to optimize for cache hits. 

* First-In First-Out (FIFO): Cache evicts the first entry in the cache, regardless of how many times it was called
* Least Recently Used (LRU): Cache evicts the least recently used items first
* Most Recently Used (MRU): Cache evicts the most recently used items first 
* Least Frequently Used (LFU): Cache counts how often an entry was read from the cache. Those that are used the least often are discarded first. 
* Random Replacement (RR): Randomly select a candidate item and discard it to make space necessary. 



#### Sources
[System Designs: Basics on Caching](https://medium.com/geekculture/system-design-basics-caching-46b1614915f8)