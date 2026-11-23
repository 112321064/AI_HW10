# S03 · IBM Quantum Learning〈Circuits〉

- 書目　IBM Quantum Learning，*Basics of quantum information*，Quantum circuits 單元。
- 來源　[Circuits 原課程](https://quantum.cloud.ibm.com/learning/en/courses/basics-of-quantum-information/quantum-circuits/circuits)
- 取用日期　2026-11-23。
- 擷取位置　〈Quantum circuits〉，單量子位元的 `H`、`S`、`H`、`T` 範例、Qiskit 位元順序與測量範例。

## 擷取要點

1. 水平線代表量子位元。電路上的閘按時間由左向右施作，先施作的算子在矩陣乘積的右側。教材依序施作 `H`、`S`、`H`、`T`，總算子寫成 `THSH`。
2. 實心圓連到目標操作代表受控閘。教材用 CNOT、Toffoli 和 Fredkin 示範控制端與目標端的畫法。
3. Qiskit 最上方的 `q0` 是位元字串的最右一位。對照教材圖與 Wiki 的 `(控制位, 目標位)` 公式時，先確認每個位置對應哪一條線。
4. 教材也用量測符號表示計算基底量測，並把結果寫入經典位元。用 $U^\dagger$ 反轉的推導適用於酉閘段。量測後只保留結果時，原先振幅之間的相位一般無法從結果還原。

[基本可逆閘](../wiki/02-gates.md) · [酉性與逆電路](../wiki/03-unitarity.md) · [Wiki 首頁](../README.md)
