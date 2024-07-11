## functional requirements

- user uploads video
- user watches video, and data is collected during watching
- user searches for video

### call out
- cold-start is a problem, if there is a new user.
	- opportunity for
		- reinforcement learning
		- multi-arm bandit
- reinforcement - exploit: "should we show videos from channels user watched before?"
- reinforcement - explore: "should we show new channels?"

## model

1. PageRank
	1. PageRank uses graph db and Pregel.
	2. We will use `inverted index` instead graph db as pages are not interconnected.
	3. No personalization in step 1
2. Personalization and ranking
	1. Use `content-based filtering, with classifier of Logistic regression, or linear regression`



