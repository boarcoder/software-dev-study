Druid is a real-time analytics db, that offers some of the highest QPS. (1k+)


| QPS | Q/day | Events/S | RTT   | Rows                  | Citation          |
| --- | ----- | -------- | ----- | --------------------- | ----------------- |
|     | 4 mm  |          | 300ms |                       | Target            |
| 350 |       | 5 mm     |       |                       | Confluent Health+ |
|     |       | 2 mm     |       | 1.5 tt, q<br>1.5 bb/d | Netflix           |
|     |       |          |       |                       |                   |


## Official Architecture
https://druid.apache.org/docs/latest/design/architecture/architecture

![[Pasted image 20240908142923.png]]

## Netflix

![[Pasted image 20240908151528.png]]
https://imply.io/case-studies/how-druid-provides-internet-scale-observability-at-netflix/
![[Pasted image 20240908151508.png]]

![[Pasted image 20240908151835.png]]
https://netflixtechblog.com/how-netflix-uses-druid-for-real-time-insights-to-ensure-a-high-quality-experience-19e1e8568d06

## Walmart Labs Case

![[Pasted image 20240908143150.png]]

## Salesforce - Event Bus model

![[Pasted image 20240908143657.png]]

## Confluent Health+ Monitoring Service

### Highest Usage
- **100 nodes**, Historical processes.
- **75 nodes**, MiddleManager processes.
- **3mm EPS** ingested
- **250 QPS**
- Data **Tiering**: 7 days of queryable data, since 90% of queries are <15min. Hot data tier is separated, with more CPU on hot data.

![[Pasted image 20240908143715.png]]

![[Pasted image 20240908145958.png]]

.