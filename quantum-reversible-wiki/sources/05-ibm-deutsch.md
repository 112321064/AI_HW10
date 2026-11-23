# S05 · IBM Quantum Learning〈Deutsch's algorithm〉

- 書目　IBM Quantum Learning，*Fundamentals of quantum algorithms*，Quantum query algorithms 單元。
- 來源　[Deutsch's algorithm 原課程](https://quantum.cloud.ibm.com/learning/en/courses/fundamentals-of-quantum-algorithms/quantum-query-algorithms/deutsch-algorithm)
- 取用日期　2026-11-23。
- 擷取位置　〈Quantum circuit description〉、〈Analysis〉與〈Further remarks on the phase kickback〉。

## 擷取要點

1. Deutsch 問題對 $f:\{0,1\}\to\{0,1\}$ 判定 $f(0)\oplus f(1)$。結果為 `0` 代表兩個函數值相同，結果為 `1` 代表兩個函數值不同。
2. 查詢閘對目標位實作 $X^{f(x)}$。目標準備為 $|-\rangle$ 時，利用 $X|-\rangle=-|-\rangle$ 得到 $U_f|x\rangle|-\rangle=(-1)^{f(x)}|x\rangle|-\rangle$。目標仍可寫成同一個 $|-\rangle$ 態，輸入的各疊加分量各自取得對應相位。
3. 輸入為 $|+\rangle$ 時，兩個分量之間的相對符號由 $f(0)\oplus f(1)$ 決定。最後的 Hadamard 閘把相對符號轉成可測量的 `0` 或 `1`。

## 適用範圍

此處使用單輸入位元的查詢模型，並假設能使用指定的 $U_f$。一次量子查詢與兩次保證正確的經典查詢，比的是黑箱呼叫次數。課程的 ket 位置遵循 Qiskit 慣例，本筆記把輸入寫在目標前面。

[酉運算與電路反轉](../wiki/03-unitarity.md) · [相位回踢](../wiki/05-phase-kickback.md) · [Wiki 首頁](../README.md)
