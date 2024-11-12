---
{"dg-publish":true,"dg-permalink":"software-engineer/tools/elasticsearch/boost","permalink":"/software-engineer/tools/elasticsearch/boost/","title":"boost"}
---

boost 在 [[software-engineer/tools/elasticsearch/terms query\|terms query]] 中用於拉高特定匹配到欄位的權重，並提高最終文件算分的總分，該值介於 0 到 1.0 之間會調低[[相關性分數\|相關性分數]]，大於 1.0 會提高 [[相關性分數\|相關性分數]]。