---
{"dg-publish":true,"dg-permalink":"software-engineer/tools/elasticsearch/indexed","permalink":"/software-engineer/tools/elasticsearch/indexed/","title":"indexed"}
---

- Every field that is [[software-engineer/tools/elasticsearch/indexed\|indexed]] in [[Lucene\|Lucene]] is converted into a fast search structure for its particular type.
	- The [[text field\|text field]] is split into tokens, if analyzed or saved as a single [[token\|token]]
	- The [[numeric fields\|numeric fields]] are converted into their fastest binary representation
	- The date and [[datetime fields\|datetime fields]] are converted into binary forms