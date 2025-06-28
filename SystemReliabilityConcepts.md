## System reliability key concepts: 

**1. CAP Theorem**:
   - ***Consistency***: All nodes see the same data at the same time.
   - ***Availability***: Every request receives a response, without guarantee that it contains the most recent version of the information.
   - ***Partition Tolerance***: The system continues to operate despite network partitions.
   -  Distributed systems can provide at most two from these three guarantees simultaneously: 
   -  If partition happens, you can choose between: Availability or Consistency.
  
**2. Eventual Consistency**:
   - A system is eventually consistent if, given enough time without new updates, all replicas will converge to the same state. If stop making updates to the system, all replicas will eventually become consistent with same state.
Eventual consistency make simple promises:
   - If you stop making updates, all replicas will eventually converge to the same state.
   - This increadibly powerfull for large scale systems.
   - Eventual consistent system writes complete immediately, without confirmation from all replicas. This improves performance and availability. 
        ##### But how the system handle conflicts when different replicas receive different updates?
       -  When conflicts occur system uses different strategies to resolve them, such as:
       - Last Write Wins (LWW): The most recent update is considered the correct one.
       - Version Vectors: Each replica maintains a version vector to track updates and resolve conflicts based on causality.
       - Custom Conflict Resolution: Application-specific logic to determine the correct state.
       - Dynamo db typically achives consistency within miliseconds under normal conditions.

**3. Load balancing**:
   - Load balancer distributes incomming requests across multiple servers to ensure no single server is overwhelmed. This improves performance and reliability by preventing bottlenecks.
   - Layer 4 load balancers operate at the transport layer (TCP/UDP) and make routing decisions based on IP addresses and ports.
   - Layer 7 load balancers operate at the application layer (HTTP/HTTPS) and can make routing decisions based on application-level data, such as URL paths or HTTP headers.
   - For higher availability, load balancers can be deployed in primary secondary configuration, where one load balancer is active and the other is on standby. If the active load balancer fails, the standby takes over.

**4. Consistent Hashing**:
   - It ensures same client always goes to the same server, even if the number of servers changes.

**5. Circuit Breaker**:
   - A circuit breaker is a design pattern used to prevent a system from repeatedly trying to execute an operation that is likely to fail. It helps to avoid cascading failures in distributed systems.
   - When a circuit breaker detects a failure, it "opens" the circuit, preventing further requests from being sent to the failing service. After a certain period, it "closes" the circuit and allows requests to be sent again.
   - This pattern helps to improve system reliability by allowing the system to recover from failures gracefully.

**6. Rate Limiting**:
   - It controls how many requests a client can make to  a server within a specific time period. This helps to prevent abuse and ensures fair usage of resources.

**7. Monitoring**:
   - Monitoring is the process of collecting and analyzing data about a system's performance and health. It helps to identify issues, track performance metrics, and ensure system reliability.
   - Common monitoring tools include Prometheus, Grafana, and ELK stack (Elasticsearch, Logstash, Kibana).
   - Key metrics to monitor include response time, error rates, throughput, and resource utilization (CPU, memory, disk).
