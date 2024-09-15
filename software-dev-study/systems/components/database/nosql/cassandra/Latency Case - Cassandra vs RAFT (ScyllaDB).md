- Most of this study is using 3 node clusters for both products.
- The 50/50 read write caps Cassandra at 40k QPS (as per its read limitations)
- If you want guaranteed 99% < 10ms, you either have to keep Cassandra under 20k QPS, or use ScyllaDB.
	- However, this is again thinking of 50/50 read/write.
	- **Cassandra** can handle write only loads at much higher QPS than the table shows, scaling with nodes added (Netflix study at 1mm QPS).

![[Pasted image 20240909132233.png]]

![[Pasted image 20240909132038.png]]

![[Pasted image 20240909132150.png]]


Source: https://www.scylladb.com/2021/08/24/apache-cassandra-4-0-vs-scylla-4-4-comparing-performance/
