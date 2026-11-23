# S01 · Bennett（1973）〈Logical Reversibility of Computation〉

- 書目　Charles H. Bennett，*IBM Journal of Research and Development* 17(6)，525–532，1973。
- 來源　[原論文掃描（Duke University）](https://users.cs.duke.edu/~reif/courses/complectures/AltModelsComp/Bennett/LogRevComp.pdf)
- 取用日期　2026-11-23。
- 擷取位置　原刊頁 525–526 的引言，以及〈Logically reversible Turing machines〉與表 1（頁 527）。

## 擷取要點

1. 可用額外的歷史帶記錄原本會丟棄的資訊，使正向運算的每一步都能回推。這會增加暫存需求。
2. 算出結果後，先把結果寫到一條原本空白的獨立磁帶，再用逆轉移倒著跑第一階段。最後歷史帶回到空白，保留原始輸入與另存的結果。
3. 如果不同輸入可能得到同一輸出，單靠輸出無法還原是哪一個輸入。保留原始輸入，使整個運算的輸入依然可辨識。

## 適用範圍

論文的模型是經典可逆圖靈機。對應到量子閘電路時，另存的是計算基底中的函數值，可用 CNOT 依線性方式操作。量子電路的實作見 [S04](04-ibm-classical-simulation.md)。

[可逆性的判準](../wiki/01-reversibility.md) · [反計算](../wiki/04-uncomputation.md) · [Wiki 首頁](../README.md)
