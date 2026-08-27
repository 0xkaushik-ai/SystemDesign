Caching means storing frequently used data in a faster location so future requests can be answered
  quickly.

  Client → Cache → Database
            ↑
       Fast response

  Example:

  1. User requests a stock price.
  2. The system checks the cache.
  3. If the data exists, it returns it quickly.
  4. Otherwise, it reads from the database and stores the result in the cache.

  ### Important terms

  - Cache hit: Data is found in the cache.
  - Cache miss: Data is not found, so the system checks the original database or service.
  - TTL: How long cached data remains valid.
  - Cache invalidation: Removing or updating stale cached data.

  ### Common caching locations

  - Browser cache
  - CDN cache
  - Application/server cache
  - Database cache
  - Distributed cache such as Redis or Memcached

  ### Benefits

  - Lower latency
  - Reduced database load
  - Better scalability
  - Lower network usage

  ### Main challenge

  Cached data can become outdated. This is especially important in a trading system, where incorrect
  prices or account balances could be dangerous.

  A common interview principle is:

  > Use caching for data that is read frequently and can tolerate some staleness; avoid caching      
  > highly sensitive, rapidly changing data unless consistency is carefully designed.                


› what is multicaching


• “Multicaching” is not usually a formal term. In system design, people generally mean multi-level
  caching: using multiple cache layers.

  User
   ↓
  Browser cache
   ↓
  CDN cache
   ↓
  Application cache, e.g. Redis
   ↓
  Database

  Each layer can reduce latency and load on the next layer.

  Example:

  - Browser cache serves static files immediately.
  - CDN serves content close to the user.
  - Redis stores frequently accessed application data.
  - Database is used only when all caches miss.

  This is also called cache hierarchy or layered caching.

  Another related concept is distributed caching, where one cache such as Redis is spread across
  multiple servers so it can handle more data and requests.
 

Distributed caching means storing frequently used data in a cache shared across multiple
  application servers.

  Users
    ↓
  Load Balancer
    ↓
  App Server A ─┐
  App Server B ─┼── Distributed Cache, e.g. Redis
  App Server C ─┘
                  ↓
               Database

  Without a shared cache, each application server may have its own separate cache, causing duplicated
  data and cache misses. A distributed cache lets all servers access the same cached data.

  ### Example

  For a trading platform, many servers may need a user’s portfolio or instrument metadata. Instead of
  querying the database repeatedly, they read commonly requested data from Redis.

  ### Benefits

  - Faster responses
  - Reduced database load
  - Shared data across servers
  - Better scalability
  - Cache remains available even when requests move between servers

  ### Challenges

  - Cache invalidation and stale data
  - Cache server failures
  - Network latency
  - Memory limits
  - Distributed-cache consistency
  - Hot keys receiving too many requests

  Common technologies include Redis, Memcached, Hazelcast, and cloud services such as Amazon
  ElastiCache.

  The basic principle is:

  > Multiple application servers share a fast cache layer positioned between the application and the 
  > database.                                                                                        
 
 
 

 
