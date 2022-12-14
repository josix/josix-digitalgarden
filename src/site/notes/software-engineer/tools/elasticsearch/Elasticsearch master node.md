---
{"dg-publish":true,"dg-permalink":"software-engineer/tools/elasticsearch/Elasticsearch master node","permalink":"/software-engineer/tools/elasticsearch/Elasticsearch master node/"}
---

- Master node 負責管理 cluster 中的所有改變如 增刪 [[software-engineer/tools/elasticsearch/Elasticsearch index\|Elasticsearch index]]，增刪任何 [[software-engineer/tools/elasticsearch/Elasticsearch node\|Elasticsearch node]] 到 cluster 中。
- Master node 不會參與 [[software-engineer/tools/elasticsearch/Elasticsearch document\|Elasticsearch document]] 的增刪或搜尋，因此不會影響索引、檢索效能。
- 任何 [[software-engineer/tools/elasticsearch/Elasticsearch node\|Elasticsearch node]] 都可以成為 master node，若 master 故障，其他 node 會選舉出新的 master node，並將 [[software-engineer/tools/elasticsearch/Elasticsearch replica shard\|Elasticsearch replica shard]] 接替成為 [[software-engineer/tools/elasticsearch/Elasticsearch primary shard\|Elasticsearch primary shard]]