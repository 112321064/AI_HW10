# S06 · Barenco 等人（1995）〈Elementary gates for quantum computation〉

- 書目　Adriano Barenco 等人，*Physical Review A* 52，3457–3467，1995，DOI `10.1103/PhysRevA.52.3457`。
- 來源　[arXiv 書目及作者全文](https://arxiv.org/abs/quant-ph/9503016) · [作者全文 PDF](https://arxiv.org/pdf/quant-ph/9503016)
- 取用日期　2026-11-23。
- 擷取位置　摘要、§1〈Background〉的酉演化、§4 引理 4.1 的正交條件、§6.1 引理 6.1 與推論 6.2、§6.2〈Three-bit gates congruent to ∧²(U)〉。

## 擷取要點

1. 任意單量子位元酉閘與 CNOT 能組成任意有限量子位元上的酉操作。這裡允許使用整個 $U(2)$ 的單量子位元閘。
2. 引理 6.1 分解雙控制閘。當兩個控制位均為 `1` 時，在目標施作 $V^2=U$。其他控制組合在目標實作恆等操作。推論 6.2 指出，令 $U=X$ 就得到 Toffoli 閘，且此閘的逆操作就是原閘。
3. §6.2 給出帶輸入相依相位的較短分解。兩個電路若有相同的布林真值表，仍可能在計算基底振幅上產生不同符號，從而改變疊加態的干涉結果。

## 適用範圍

通用性結論依賴任意單量子位元酉閘與 CNOT 的組合。將帶相對相位的分解代入含疊加的電路時，需要核對相位是否會影響後續運算。

[基本可逆閘](../wiki/02-gates.md) · [酉運算與電路反轉](../wiki/03-unitarity.md) · [相位回踢](../wiki/05-phase-kickback.md) · [Wiki 首頁](../README.md)
