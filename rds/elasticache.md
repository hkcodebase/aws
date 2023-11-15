# ElastiCache
- This is in-memory db provide high preformance and low latency
- Managed Cache service by AWS on Redis or Memcached
- Manged by AWS so maintenance of Cache infrastructure is managed by AWS 
- Application code needs to be changed to use ElastiCache

## Use Cases:
 1. Improve read peroformance - read from cache before database
 2. Store Session data - session data can be stored in cache and retrieved over multiple intances of application


 ### ElastiCache Redis vs Memcache
 - Redis : Multi AZ with Auto-Failover, Memcached - Multinode for partitioning of data
 - Redis: Read replicas to scale reads and high availability, Memcached : No High availability
 - Redis: Backup and restore, Memcached: no backup and restore
 - Redis: Supports Sets and Sorted Sets, Memcached: Multi threaded architecture

### Caching Implementation factors 
- Is it safe to cache data?
- 