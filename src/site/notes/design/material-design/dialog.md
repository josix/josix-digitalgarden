---
{"dg-publish":true,"dg-permalink":"design/material-design/dialog","permalink":"/design/material-design/dialog/","title":"dialog"}
---

## 什麼是對話框（Dialog）
Dialog 用於提醒使用者執行特定任務，包含要求使用者進行選擇、確認資訊甚至執行是複雜的邏輯。
## 使用時機
Dialog 是互動視窗 （[[Modal\|Modal]]）的一種，對話框會顯示在所有頁面的最前方並且讓使用者操作互動視窗，直到使用者關閉視窗或是執行完指定任務。

Dialog 通常用於要求使用者做出特定決定以讓服務可以繼續運行，另外也用於確保使用者有明確接收到系統傳達的資訊。

Dialog 用於呈現會導致系統無法執行的錯誤訊息、也用於要求使用者執行複雜任務、或是確認特定資訊。相較 [[Snackbar\|Snackbar]]、[[Banner\|Banner]]， Dialog 用於呈現最重要的資訊其次是 Banner 最後則是 Snackbar，Dialog 會遮蔽頁面直到使用者完成任務，Banner 會顯示資訊直到使用者自行關閉或該狀態取消顯示 Banner，而 Snackbar 則會自行消失

## 原則
Dialog 有三種原則有利於要求使用者完成特定任務：
- 專注：由於 Dialog 會遮蔽頁面的其他資訊僅保留 Dialog 可以互動，因此可以讓使用者專注在 Dialog 上。
- 指示：Dialog 有指示性，讓使用者可以專注遵循對話框的內容完成指令。
- 幫助：Dialog 可以確保使用者接收任何動作執行後的回饋，使其瞭解系統操作的行為。