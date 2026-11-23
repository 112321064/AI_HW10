# 量子可逆電路 LLM Wiki

[開啟教學 HTML 簡報](../quantum-reversible-slides.html)

**核心問題**　如果只知道 AND 的輸出，能推回原本的輸入嗎？保留哪些資訊，才能把 AND 放進可反轉的量子電路？

這份 Wiki 面向學過基本布林邏輯、剛接觸量子電路的讀者。可以從真值表讀起，再用同一個 AND 例子理解酉運算、反計算與相位回踢。

## 閱讀路線

| 順序 | 觀念頁 | 讀完能解釋的問題 |
| --- | --- | --- |
| 1 | [什麼是可逆計算？](wiki/01-reversibility.md) | 為什麼 AND 無法從單一輸出推回輸入？如何用 XOR 保留資訊？ |
| 2 | [X、CNOT 與 Toffoli 閘](wiki/02-gates.md) | 哪些輸入會讓目標位元翻轉？如何從 Toffoli 的真值表讀出 AND？ |
| 3 | [酉運算與電路反轉](wiki/03-unitarity.md) | 為什麼反轉量子電路要倒轉閘的順序並逐閘取逆？真值表能告訴我們多少？ |
| 4 | [反計算與輔助量子位元](wiki/04-uncomputation.md) | 如何保留計算結果，同時把暫存空間還原為零？ |
| 5 | [相位回踢](wiki/05-phase-kickback.md) | 目標位元準備成 `|−⟩` 後，受控翻轉如何讓相對相位改變？ |

本 Wiki 按名稱由左到右讀取字串。例如 `110` 代表 `(a,b,t) = (1,1,0)`，`a`、`b` 是控制位元，`t` 是目標位元。`⊕` 代表 XOR，`ab` 代表 AND。

## 已匯入的來源

每張來源卡記錄原始連結、閱讀位置、摘要、使用條件，以及引用它的觀念頁。觀念頁透過同一組來源編號回連。

| 編號 | 來源卡 | 取用重點 |
| --- | --- | --- |
| S01 | [Bennett（1973），*Logical Reversibility of Computation*](sources/01-bennett.md) | 留存運算歷程，再反向清理暫存資訊 |
| S02 | [Toffoli（1980），*Reversible Computing*](sources/02-toffoli.md) | 經典可逆邏輯與 AND/NAND 元件 |
| S03 | [IBM Quantum Learning，*Circuits*](sources/03-ibm-circuits.md) | 電路、酉閘、受控閘與量測符號 |
| S04 | [IBM Quantum Learning，*Classical computations on quantum computers*](sources/04-ibm-classical-simulation.md) | 布林電路的可逆實作與反計算 |
| S05 | [IBM Quantum Learning，*Deutsch’s algorithm*](sources/05-ibm-deutsch.md) | XOR 查詢閘與相位回踢 |
| S06 | [Barenco 等人（1995），*Elementary gates for quantum computation*](sources/06-barenco.md) | 酉演化與量子閘集合的通用性 |

- [建置與查核紀錄](workflow.md)記錄選題、六筆資料的匯入、查核用例及回修流程，也說明各張 HTML 投影片如何取用 Wiki 內容。
