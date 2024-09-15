
### READS: Cassandra Quorum read vs PAXOS

| Product                           | RTT                                               | Size | Definition                                                  | Pros                   | Cons                                                 |
| --------------------------------- | ------------------------------------------------- | ---- | ----------------------------------------------------------- | ---------------------- | ---------------------------------------------------- |
| CassandraDB                       | ∞ @ 20k QPS<br>(quorum)<br><br>**20ms** @ 15k QPS | 4kb  | follower><br>getMessage><br>forceLog><br>sendAck><br>Leader |                        | Quorum read requires 2 replicas, check for conflicts |
| PAXOS based datastore (spinnaker) | 5ms @ 60k QPS                                     | 4kb  |                                                             | VERY fast read latency |                                                      |

### WRITE: Cassandra Quorum Write vs PAXOS

| Product                           | RTT                         | Size | Definition                                                  | Pros                  | Cons                          |
| --------------------------------- | --------------------------- | ---- | ----------------------------------------------------------- | --------------------- | ----------------------------- |
| CassandraDB                       | 60 - 75ms<br><br>@ 0-5k QPS | 4kb  | follower><br>getMessage><br>forceLog><br>sendAck><br>Leader | Slightly faster write |                               |
| PAXOS based datastore (spinnaker) | 65-80ms<br><br>@ 0-5k QPS   | 4kb  |                                                             |                       | Slightly slower write latency |

| Product                           | Algorithm                       |
| --------------------------------- | ------------------------------- |
| CassandraDB                       | SSTables,<br>Quorum consistency |
| PAXOS based datastore (spinnaker) | PAXOS                           |
### WRITE: 

[Using Paxos to Build a Scalable, Consistent, and Highly Available Datastore](https://arxiv.org/pdf/1103.2408)

![[Pasted image 20240908155856.png]]

![[Pasted image 20240908155903.png]]
.