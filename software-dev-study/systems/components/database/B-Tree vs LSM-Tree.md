
|               | B-Tree              | LSM-Tree           | SSTables           | Skip List    | BT/LSM Combo                         |
| ------------- | ------------------- | ------------------ | ------------------ | ------------ | ------------------------------------ |
| Read Latency  | x                   |                    |                    |              | x                                    |
| Write Latency |                     | x                  | x                  | x            |                                      |
| Read QPS      | x                   |                    |                    |              | x                                    |
| Write QPS     |                     | x                  | x                  | -            | x                                    |
| Range Query   | x                   |                    |                    |              |                                      |
| Best Use Case | Read-heavy          | Write-heavy        | Write-heavy        | Memory-based | High-scale<br>Unpredictable workload |
|               |                     |                    |                    |              |                                      |
| Examples      | MySQL<br>PostgreSQL | RocksDB<br>LevelDb | Cassandra<br>HBase | Redis        | DyanmoDb                             |
### Takeaway

| Scenario | Best Product                              | Algorithm |
| -------- | ----------------------------------------- | --------- |
| Read     | MySQL, Postgres                           | B-Tree    |
| Write    | NOSQL - Cassandra                         | SSTables  |
| Range    | MySQL, Postgres<br>Though Redis also good | B-Tree    |
