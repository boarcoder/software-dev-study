### Algorithm
- LSMTree (uses SStables)
- Quorum: minimum of 3 nodes allows for distributed read/write.

### QPS

#### Writes QPS
 - NOT A PROBLEM! We can do regular writes with ease. 
 - 1mm QPS with additional nodes @Netflix
	 - i2.xlarge, 285 nodes
 - 40k max Write/UPDATE query: 40k max @i3.4xlarge
#### Reads QPS 
- 30k max Read, 5ms, @i3.4xlarge
- Limiting factor even on 50/50 read/write
#### Sample: i3.4xlarge
- Cluster size: 3
- vCPU: 16 (48 total)
- Memory: 122 GiB
- Storage: 2x 1.9TB NVMe RAID0 -striping without parity (2x max speed)

Read only: 40k QPS MAXIMUM @ 10 ms, before hitting **∞** ms
![[Pasted image 20240908163533.png]]
Write only: 