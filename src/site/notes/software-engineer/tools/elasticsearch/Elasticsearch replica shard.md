---
{"dg-publish":true,"dg-permalink":"software-engineer/tools/elasticsearch/Elasticsearch replica shard","permalink":"/software-engineer/tools/elasticsearch/Elasticsearch replica shard/","title":"Elasticsearch replica shard"}
---

- Replica shard 是 [[software-engineer/tools/elasticsearch/Elasticsearch primary shard\|Elasticsearch primary shard]] 的備份，用於提供多餘的資料備份以防硬體故障。除此以外也提供讀取資料的服務，例如 搜尋及取得 [[software-engineer/tools/elasticsearch/Elasticsearch document\|Elasticsearch document]]
- Replica shard 的數量不僅在 [[software-engineer/tools/elasticsearch/Elasticsearch index\|Elasticsearch index]] 建立時可以設定，在任何時刻都可以更動。
- 加入 replica shard 只需要啟動任何 [[software-engineer/tools/elasticsearch/Elasticsearch node\|Elasticsearch node]] 並且有著相同的 `cluster.name` 即可，即使是在同一台機器的同個位置下執行 [[software-engineer/tools/elasticsearch/Elasticsearch\|Elasticsearch]]。
-  新加入的 [[software-engineer/tools/elasticsearch/Elasticsearch node\|Elasticsearch node]] 會自動配置 replica shard
-  更新 replica shard 的數量可以透過 `PUT /<index>/_settings` 更新：
	```
	PUT /blogs/_settings
	{
		"number_of_replicas": 2
	}
	```
	`number_of_replicas` 為 replica shard 應為 [[software-engineer/tools/elasticsearch/Elasticsearch primary shard\|Elasticsearch primary shard]] 數量的幾倍
- replica shard 與 [[software-engineer/tools/elasticsearch/Elasticsearch primary shard\|Elasticsearch primary shard]] 不可以在同一個 [[software-engineer/tools/elasticsearch/Elasticsearch replica shard\|Elasticsearch replica shard]]