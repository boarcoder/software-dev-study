| Type         | Product   | R                | W                | Latency                                |
| ------------ | --------- | ---------------- | ---------------- | -------------------------------------- |
| Memory cache | Redis     | 1-10 mm/sec (Xu) | 1-10 mm/sec (Xu) | 0.001-.002 ms<br>AKA 100 nano- seconds |
| Memory cache | Memcached |                  |                  |                                        |

## Redis

### Persistence

- Append only long (Aol)
- Snapshot interval

Data required = Cache * snapshot interval
RAM = 256GB typical server, application should be = (kb/key) * keys