# Rate Limiting: 

Rate limiting is a control mechanism used to restrict the number of requests a user, IP address, or service can make to a system within a specific timeframe.

# Why Rate Limiting is Important in Distributed Systems:

i. Prevents Resource Exhaustion
ii. Enhances Security
iii. Ensures Fair Resource Usage
iv. Improves Scalability


# Caching

Caching is a technique used to temporarily store copies of data in a faster,
more accessible location, so that future requests for that data can be served 
quickly without requiring a full retrieval from the original data source.

Cached data is typically stored in memory (RAM).
Caches can be located on the client side, server side, or in between (like a CDN)

# Types of Caching:

i. database Caching.
ii. web Caching
iii. CDN 
iv. Application level Caching

# Common Caching Challenges

i. Cache Invalidation Complexity: Keeping cache in sync with the main data source can be complex, 
   especially in distributed systems.

ii. Cached data can become outdated, so it's essential to design caching strategies with 
    expiration or refresh mechanisms.

iii. Memory Usage: Storing data in memory can consume significant resources, 
     so balancing cache size and system memory is crucial.