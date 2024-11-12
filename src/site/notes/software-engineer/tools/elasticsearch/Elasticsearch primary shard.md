---
{"dg-publish":true,"dg-permalink":"software-engineer/tools/elasticsearch/Elasticsearch primary shard","permalink":"/software-engineer/tools/elasticsearch/Elasticsearch primary shard/","title":"Elasticsearch primary shard"}
---

- Elasticsearch shard 是 [[software-engineer/tools/elasticsearch/Elasticsearch\|Elasticsearch]] 最小的運作單元，每個 shard 持有一部分[[software-engineer/tools/elasticsearch/Elasticsearch index\|Elasticsearch index]] 的資料。
- 每個 shard 都是 [[Lucene\|Lucene]] 的個體，自身便是一個完整搜索引擎（[[Search Engine\|Search Engine]]）
- shard 是資料的容器（[[Container\|Container]]），其存放著許多的 [[software-engineer/tools/elasticsearch/Elasticsearch document\|Elasticsearch document]]，而 Shard 會被配置在 [[software-engineer/tools/elasticsearch/Elasticsearch node\|Elasticsearch node]] 中，形成 [[software-engineer/tools/elasticsearch/Elasticsearch cluster\|Elasticsearch cluster]]
- Elasticsearch shard 分為兩種分別是 [[software-engineer/tools/elasticsearch/Elasticsearch primary shard\|Elasticsearch primary shard]] 和 [[software-engineer/tools/elasticsearch/Elasticsearch replica shard\|Elasticsearch replica shard]]
- primary shard 的數量是在 [[software-engineer/tools/elasticsearch/Elasticsearch index\|Elasticsearch index]] 建立時固定下來的，後續不可再更動。
- 預設 [[software-engineer/tools/elasticsearch/Elasticsearch\|Elasticsearch]] 會設定五個 primary shard
- 在建立 Index 時設定 shard 的參數如下：
	```
	PUT /blogs
	{
		"settings": {
			"number_of_shards": 3,
			"number_of_replicas": 1
		}
	}
	```
	
	![Pasted image 20210911011816.png](https://i.imgur.com/Ivp0W7x.png)

	由於 replica shard 未完全運作，因此 cluster 健康狀態是黃色的
- 新建立索引（[[software-engineer/tools/elasticsearch/indexed\|indexed]]）的 [[software-engineer/tools/elasticsearch/Elasticsearch document\|Elasticsearch document]] 會先被放置在 primary shard 之後再會備份至 [[software-engineer/tools/elasticsearch/Elasticsearch replica shard\|Elasticsearch replica shard]]