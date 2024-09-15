- Optimized for **time-series** data.
- **Primary dimension**: Timestamp
- **Indexed on Timestamp** to allow intervals or windows quickly
	- Indexing occurs all **automatically** on this column. No interaction needed.
- **Rows**: Trillions - as time-series index is that efficient.


![[Pasted image 20240908150417.png]]
https://medium.com/@david.wang_1754/apache-druid-making-1000-qps-for-analytics-look-easy-512cce818778

![[Pasted image 20240908151840.png]]

The storage in time chunks allows faster RANGE queries!