# S04 · IBM Quantum Learning〈Classical computations on quantum computers〉

- 書目　IBM Quantum Learning，*Fundamentals of quantum algorithms*，Quantum algorithmic foundations 單元。
- 來源　[Classical computations on quantum computers 原課程](https://quantum.cloud.ibm.com/learning/en/courses/fundamentals-of-quantum-algorithms/quantum-algorithmic-foundations/simulating-classical-computations)
- 取用日期　2026-11-23。
- 擷取位置　〈Toffoli gates〉、〈Simulating Boolean gates with Toffoli, controlled-NOT, and NOT gates〉、〈Cleaning up the garbage〉與〈Implementing invertible functions〉的開頭。

## 擷取要點

1. 教材用 NOT、CNOT 與 Toffoli 逐閘模擬布林電路。其中 AND 使用一個初始化為零的工作位元存結果，同時保留兩個輸入位元。
2. 先施作可逆電路 $R$ 算出 $f(x)$，再用 CNOT 把計算基底中的結果 XOR 到獨立的目標暫存器。接著逆序施作每個閘的逆閘，得到 $R^\dagger$，把工作位元恢復為初始零值。
3. 用 Wiki 的暫存器順序 `[輸入, 工作, 目標]` 表示，清除中間值後的整體映射是 $|x,0^k,y\rangle\mapsto|x,0^k,y\oplus f(x)\rangle$。目標設為零時可讀出 $f(x)$。

## 適用範圍

中間的 CNOT 將經典函數值寫入目標，遇到疊加輸入時仍按各計算基底分量線性作用。準備為零的工作暫存器會恢復原值。若要在原輸入暫存器直接實現 $|x\rangle\mapsto|f(x)\rangle$，此處的構造需要 $f$ 本身可逆，並可取得實作 $f^{-1}$ 的布林電路。

[可逆性的判準](../wiki/01-reversibility.md) · [基本可逆閘](../wiki/02-gates.md) · [反計算](../wiki/04-uncomputation.md) · [Wiki 首頁](../README.md)
