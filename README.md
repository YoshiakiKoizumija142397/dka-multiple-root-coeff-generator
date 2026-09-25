# MethodDKA Multiplicity & Coefficient Generator

## 1. 概要 (Overview)
MethodDKA 多重根・係数ジェネレータ (`dka-multiple-root-coeff-generator.html`) は、代数方程式の全根同時直接解法である **Durand-Kerner-Aberth (DKA) 法** の数値計算アルゴリズム検証およびベンチマークテストのために設計された Web アプリケーションです。

特に多重根や近接根群を含む複素多項式の係数を `Decimal.js` を用いて任意精度（32〜128桁以上）で高精度に展開・生成できます。

## 2. 数学的定式化 (Formulation)
与えられた $K$ 個の複素根 $z_k$ と重複度 $m_k$ に対し、最高次数が $N = \sum_{k=1}^{K} m_k$ の多項式を展開します：

$$P(x) = \prod_{k=1}^{K} (x - z_k)^{m_k} = a_N x^N + a_{N-1} x^{N-1} + \dots + a_0$$

## 3. 3重根収束ベンチマーク検証結果 (200桁精度)

| 反復回数 | 経過時間 | 誤差半径 | 有効精度 ($x=1$) | 評価 |
| :---: | :---: | :---: | :---: | :--- |
| **100 回** | 00:00:00 | $1.5 	imes 10^{-22}$ | 約 21 桁 | 収束途上 |
| **250 回** | 00:00:01 | $2.0 	imes 10^{-58}$ | 約 57 桁 | 1秒実用領域 |
| **325 回** | **00:00:01** | **$2.9 	imes 10^{-76}$** | **約 74 桁** | **★ 1秒枠での最高効率点** |
| **400 回** | **00:00:02** | **$4.6 	imes 10^{-77}$** | **約 75 桁** | **★ 理論限界精度到達** |
| **500 回** | 00:00:03 | $3.1 	imes 10^{-77}$ | 約 75 桁 | 安定領域 |
| **20,000 回** | 02:01:00 | $3.0 	imes 10^{-78}$ | 約 77 桁 | 飽和領域 |

## 4. 使用方法 (Usage)
1. 複素平面キャンバスで根をクリック追加、またはプリセットを選択。
2. 画面上の `最高次数 N` を確認。
3. `MethodDka用コピー` ボタンを押し、`MethodDka.html` の一括ペースト欄に貼り付けて計算を実行。
開発者　小泉嘉章
リポジトリ　YoshiakiKoizumija142397/MethodDka

# MethodDKA Multiplicity & Coefficient Generator

## 1. Overview
The MethodDKA Multiplicity & Coefficient Generator (`dka-multiple-root-coeff-generator.html`) is a web application designed for verifying numerical calculation algorithms and running benchmark tests for the **Durand-Kerner-Aberth (DKA) method**, a direct method for simultaneously finding all roots of an algebraic polynomial.

In particular, it expands and generates coefficients for complex polynomials containing multiple roots or clusters of closely spaced roots with high precision using `Decimal.js` at arbitrary precision levels (from 32 to over 128 digits).

## 2. Mathematical Formulation
Given $K$ complex roots $z_k$ with multiplicities $m_k$, the polynomial with maximum degree $N = \sum_{k=1}^{K} m_k$ is expanded as:

$$P(x) = \prod_{k=1}^{K} (x - z_k)^{m_k} = a_N x^N + a_{N-1} x^{N-1} + \dots + a_0$$

## 3. Triple Root Convergence Benchmark Results (200-Digit Precision)

| Iterations | Elapsed Time | Error Radius | Effective Precision ($x=1$) | Evaluation |
| :---: | :---: | :---: | :---: | :--- |
| **100** | 00:00:00 | $1.5 \times 10^{-22}$ | Approx. 21 digits | Converging |
| **250** | 00:00:01 | $2.0 \times 10^{-58}$ | Approx. 57 digits | Practical 1-second limit |
| **325** | **00:00:01** | **$2.9 \times 10^{-76}$** | **Approx. 74 digits** | **★ Peak efficiency within 1-second window** |
| **400** | **00:00:02** | **$4.6 \times 10^{-77}$** | **Approx. 75 digits** | **★ Reached theoretical precision limit** |
| **500** | 00:00:03 | $3.1 \times 10^{-77}$ | Approx. 75 digits | Stable region |
| **20,000** | 02:01:00 | $3.0 \times 10^{-78}$ | Approx. 77 digits | Saturation region |

## 4. Usage
1. Click on the complex plane canvas to add roots, or select a preset.
2. Verify the `Maximum Degree N` displayed on the screen.
3. Click the `Copy for MethodDka` button, then paste the contents into the batch paste field of `MethodDka.html` to execute the calculation.

Developer　Yoshiaki Koizumi
Repositry YoshiakiKoizumija142397/MethodDka
