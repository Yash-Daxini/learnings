## System reliability key concepts: 

1. **CAP Theorem**:
   - ***Consistency***: All nodes see the same data at the same time.
   - ***Availability***: Every request receives a response, without guarantee that it contains the most recent version of the information.
   - ***Partition Tolerance***: The system continues to operate despite network partitions.
>
   > [!NOTE] 
   > Distributed systems can provide at most two from these three guarantees simultaneously:
  
  If partition happens, you can choose between: Availability or Consistency.
  
2. **Eventual Consistency**:
   - A system is eventually consistent if, given enough time without new updates, all replicas will converge to the same state. If stop making updates to the system, all replicas will eventually become consistent with same state.
Eventual consistency make simple promises:
   - If you stop making updates, all replicas will eventually converge to the same state.
    - This increadibly powerfull for large scale systems.
     -   Eventual consistent system writes complete immediately, without confirmation from all replicas. This improves performance and availability. 

    ##### But how the system handle conflicts when different replicas receive different updates?
    When conflicts occur system uses different strategies to resolve them, such as:
   - Last Write Wins (LWW): The most recent update is considered the correct one.
   - Version Vectors: Each replica maintains a version vector to track updates and resolve conflicts based on causality.
   - Custom Conflict Resolution: Application-specific logic to determine the correct state.

        Dynamo db typically achives consistency within miliseconds under normal conditions.

**3. Load balancing**: 
- Distributing the load
Load balancer distributes incomming requests across multiple servers to ensure no single server is overwhelmed. This improves performance and reliability by preventing bottlenecks.

