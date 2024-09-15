---
tags:
  - top_k_songs_spotify
  - "#leaderboard"
  - trending_topics
  - popular_videos
  - ad_click_aggregator
  - metrics_monitoring
  - alex_xu
  - sdfc
---
## Functional Requirements

- User can view top k elements
- User can select time range from a->b time
	- Sometimes we could have this as: last 10 minutes, last 1 hour, last day, last month.

SDFS data analysis needs you to have adequate tags on your classes. Genre, Rating, Views, Comments - so that we can get top k of different categories.

Counter distributed, build that.