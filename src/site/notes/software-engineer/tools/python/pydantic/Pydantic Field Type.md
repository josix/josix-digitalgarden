---
{"dg-publish":true,"dg-permalink":"software-engineer/tools/python/pydantic/Pydantic Field Type","permalink":"/software-engineer/tools/python/pydantic/Pydantic Field Type/","title":"Pydantic Field Type"}
---

- [[Pydantic\|Pydantic]] 支援 Python 內建的[[Python typing\|Python typing]] 作為欄位的型態，但還有其他常見的型態會由 [[Pydantic Types\|Pydantic Types]] 來補強，若還有需要自定義的型態也可以透過 [[Pydantic Custom Data Types\|Pydantic Custom Data Types]] 定義
- Python Standard Library ([[Python typing\|Python typing]])
	- [[typing.Optional\|typing.Optional]] ：[typing.Union]\[x, None\] 的簡寫，若為必填可以在帶入 ellipsis(...) 或 `Field(...)` ([[Pydantic Field function\|Pydantic Field function]])