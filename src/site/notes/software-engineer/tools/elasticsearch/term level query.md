---
{"dg-publish":true,"dg-permalink":"software-engineer/tools/elasticsearch/term level query","permalink":"/software-engineer/tools/elasticsearch/term level query/","title":"term level query"}
---

- Term level query 用於完全匹配 [[software-engineer/tools/elasticsearch/Elasticsearch document\|Elasticsearch document]] 中的特定欄位如 ip 位置、日期、價格、ID 等。不會再經過 [[Elasticsearch Analyzer\|Elasticsearch Analyzer]]，因此可以用於完全匹配且效能相較 [[full-text query\|full-text query]] 較快。
- Term level query 包含 [[software-engineer/tools/elasticsearch/term query\|term query]]、[[software-engineer/tools/elasticsearch/terms query\|terms query]]、[[exists query\|exists query]]、[[fuzzy query\|fuzzy query]]、[[prefix query\|prefix query]]、[[regexp query\|regexp query]]、[[wildcard query\|wildcard query]] 等。