# S02 · Toffoli（1980）〈Reversible Computing〉

- 書目　Tommaso Toffoli，*Automata, Languages and Programming*（ICALP 1980），632–644。
- 來源　[會議論文掃描（Università della Svizzera italiana）](https://cqi.inf.usi.ch/qic/80_Toffoli.pdf)
- 取用日期　2026-11-23。
- 擷取位置　§5〈Invertible primitives and reversible networks〉，式 (5.1)、圖 5.1、定理 5.1–5.3 與圖 5.3。

## 擷取要點

1. 式 (5.1) 的廣義 AND/NAND 元件保留控制位元，將這些位元的 AND 值 XOR 到目標位元。三位元版本即 CCNOT，寫成 `(a,b,t) → (a,b,t ⊕ (a∧b))`。目標預設為 `0` 時得到 AND，預設為 `1` 時得到 NAND。
2. 控制位保持原值，所以執行第二次會對同一目標 XOR 相同的值，使其回到初始狀態。圖 5.1 將 NOT、XOR/FAN-OUT 與 AND/NAND 列為同一家族的前三種情況。
3. 定理 5.3 使用最多三線的廣義 AND/NAND 元件，容許暫存線，實現有限可逆布林函數。圖 5.3 先算出中間值，使用後再用鏡像電路撤銷，使暫存線恢復。

## 適用範圍

定理討論的是經典可逆組合電路。定理 5.2 指出，有些固定線數的映射無法只靠更少線數的同類元件組成。定理 5.3 的暫存線條件因此要一併保留。

[可逆性的判準](../wiki/01-reversibility.md) · [基本可逆閘](../wiki/02-gates.md) · [反計算](../wiki/04-uncomputation.md) · [Wiki 首頁](../README.md)
