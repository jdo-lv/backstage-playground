# LiveCasino Cache system

The LiveCasino service uses Hazelcast as Cache system in order to keep the Dynamic data stored in a volatile system.

Given the LiveCasino service is running in a Kubernetes cluster, the CacheManager is configured with the following configuration characteristics:
- Multicast config is not enabled
- Kubernetes config is enabled
- The service-dns property is the internal DNS of a specific service of type with clusterIP none. 
This will allow the Hazelcast cluster communicate with the IP of the node directly and not through the kubernetes service IP.
- TTL (TimeToLive) of 5 seconds
- Max Idle of 5 seconds
- Eviction policy LFU (Least Frequently Used)

In order to abstract the application of the implementation of the cache used the management of the cache
is done by Spring with the `Cacheable` and `CachePut` annotations to read and write in the cache respectively.

In addition, a CacheRepository (LiveCasinoCacheRepository) has been implemented in order to populate the dynamic data
through the API endpoints.