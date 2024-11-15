---
{"dg-publish":true,"dg-permalink":"software-engineer/tools/elasticsearch/terms query","permalink":"/software-engineer/tools/elasticsearch/terms query/","title":"terms query"}
---

- terms query 用於搜尋多個完全匹配的 term 時，另外也可以可以透過 [[bool query\|bool query]] 達成
- terms query 的 query 格式如下：
```
POST /mybooks/_search
{
  "query": {
    "terms": {
	  "uuid": [
	    "3333",
		"2222"
	  ]
	}
  }
}
```
- terms query 類似 [[software-engineer/tools/elasticsearch/term query\|term query]] 差別在於可以搜尋多個 term，當要進行過濾多個值時會常使用到 terms query
- terms query 類似 SQL 中的 where 子句中的 in 關鍵字，例如：`Select * from *** where color in ("red", "green")`
- terms query 支援額外的參數包含：
	- [[software-engineer/tools/elasticsearch/minimum_match\|minimum_match]]/[[software-engineer/tools/elasticsearch/minimum_should_match\|minimum_should_match]]：用於控制最少希望匹配到的 term 數量。
	- [[software-engineer/tools/elasticsearch/boost\|boost]]：用於拉高特定匹配到欄位的權重，並提高最終文件算分的總分，該值介於 0 到 1.0 之間會調低[[相關性分數\|相關性分數]]，大於 1.0 會提高 [[相關性分數\|相關性分數]]。
	```
	"terms": {
	  "fruit": [
	    "apple",
		"banana",
		"orange"
	  ],
	  "minimum_should_match": 2,
	  "boost": 1.0,
	}
	```