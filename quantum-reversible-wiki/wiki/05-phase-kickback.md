# 相位回踢

當受控操作作用在目標位元的特徵態上，目標位元可以保持原態，卻讓控制暫存器的某些疊加分支多出相位。這個現象稱為**相位回踢（phase kickback）**。Deutsch 演算法用它將布林函數值編入相對相位，再透過干涉讀取資訊。來源 [S05，IBM Quantum 的 Further remarks on the phase kickback](../sources/05-ibm-deutsch.md)。

## 用 XOR 寫入的 oracle

對單位元輸出的布林函數 $f$，可逆 oracle $U_f$ 的基底規則是 $|x\rangle|t\rangle\mapsto |x\rangle|t\oplus f(x)\rangle$。準備目標為 $|{-}\rangle=(|0\rangle-|1\rangle)/\sqrt2$ 時，$X|{-}\rangle=-|{-}\rangle$。因此，$f(x)=0$ 的分支保留原振幅，$f(x)=1$ 的分支振幅乘上 $-1$，兩者的目標位元最後都是 $|{-}\rangle$。來源 [S05，從 XOR oracle 到相位的推導](../sources/05-ibm-deutsch.md)。

$$
U_f\bigl(|x\rangle|{-}\rangle\bigr)
=(-1)^{f(x)}|x\rangle|{-}\rangle.
$$

## Toffoli 在哪一個分支留下負號？

沿用相同規則，自行選擇 $f(a,b)=ab$，此時 oracle 就是 Toffoli。依 $(a,b,t)$ 排列，輸入選為 $|{+}\rangle|1\rangle|{-}\rangle$，其中 $|{+}\rangle=(|0\rangle+|1\rangle)/\sqrt2$。在 $(a,b)=(0,1)$ 的分支，目標保持 $|{-}\rangle$。在 $(a,b)=(1,1)$ 的分支，目標受 $X$ 作用，等價於讓該分支多出負號。

$$
\mathrm{CCX}\bigl(|{+}\rangle|1\rangle|{-}\rangle\bigr)
=\frac{|01\rangle-|11\rangle}{\sqrt2}|{-}\rangle
=|{-}\rangle|1\rangle|{-}\rangle.
$$

直接用計算基底測量第一個位元，$0$、$1$ 各有 $1/2$ 的機率。若先在第一個位元加上 Hadamard 閘 $H$，由 $H|{-}\rangle=|1\rangle$ 可知，測量結果一定是 $1$。這個步驟將相對負號轉換為可觀察的測量差異。

## 自我檢查

**問題**　同一個 Toffoli 範例若將目標換成 $|{+}\rangle$，測量前仍在第一個位元加 $H$，會得到什麼？

**答案**　一定得到 $0$。因為 $X|{+}\rangle=|{+}\rangle$，兩個分支保留同號，第一個位元在 Toffoli 後仍是 $|{+}\rangle$，再由 $H$ 轉為 $|0\rangle$。

[上一頁　反計算與輔助量子位元](04-uncomputation.md) · [Wiki 首頁](../README.md)
