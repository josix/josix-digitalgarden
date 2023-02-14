---
{"dg-publish":true,"dg-permalink":"software-engineer/designing-data-intensive-application/transaction","permalink":"/software-engineer/designing-data-intensive-application/transaction/"}
---

<!-- # 筆記本體 -->

Transaction 是資料庫執行邏輯上單一不可切割的執行單位，其中包含了多個讀取、寫入的行為。在 transaction 中執行的所有讀取和寫入，其概念上會被視為是單獨的執行行為，其結果只有全部成功（commit）或是失敗（abort, rollback）。

Transaction 帶來的好處在於排除了部分失敗的情境，資料庫的錯誤處理將會簡單並且容易許多，在於 concurrency 的使用情境下開發人員也省去判斷發生錯誤的可能性，因為資料庫具有ㄧ定的安全性保證（safety guarantees）。

## ACID
對於資料庫提供的安全性保證（safety guarantees）我們通常視其包含四個特性，其各方面達到的程度依照每個資料庫實作細節亦有所不同：

- 原子性（Atomicity）：
- ㄧ致性（Consistency）：
- 隔離性（Isolation）：
- 持久性（Durability）：持久性意味著每當 transaction 成功完成時，寫入的資料將可以預期其永遠存在於資料庫當中，即便發生硬體故障或是資料庫崩潰，我們都可以在未來恢復正常時得到過去寫入的資料。在單一節點的情況下，持久性代表著資料庫要將資料寫入非揮發記憶體如 HDD，SSD 等，然而在分散式系統中，意味著每一次資料的寫入會經過 [[Replication\|Replication]]，將資料備份在其他機器上，才能夠告訴使用者該筆資料寫入完成。


<!-- 
## 延伸問題
## See Also
-->
## References
- Designing Data Intensive Application - Chapter 7 Transactions