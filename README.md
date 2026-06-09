# higher-group-theory-verifier

**A computational verification tool for Takamura's higher group theory.**  
高村茂（京都大学）による高次群論の定理を計算機検証するツールです。

> ※本ツールは計算機による検証を目的としたものであり、数学的証明を代替するものではありません。

---

## Live Demo / デモ

| ツール | 内容 | URL |
|---|---|---|
| Ta10 ベズー型定理 | シナジー π とベズー型定理の手動・全数検証 | [index.html](https://kanataproject.github.io/higher-group-theory-verifier/) |
| Ta9 セクト・位数の法則 | Thm2.6・Thm3.9・Thm4.32 の全数検証 | [ta9.html](https://kanataproject.github.io/higher-group-theory-verifier/ta9.html) |
| SCh(G) 完全不変量の探索 | 相乗チャウ環による群の識別実験 | [sch.html](https://kanataproject.github.io/higher-group-theory-verifier/sch.html) |
| カスタム群 検証・計算 | 任意の有限群を構成して全定理を検証・計算 | [custom.html](https://kanataproject.github.io/higher-group-theory-verifier/custom.html) |

---

## Ta10 — ベズー型定理

高村による高次群論のベズー型定理（Theorem 1.3）を、有限群上で計算機検証します。

**検証定理:**

$$|H| \times |A| \times |K| = \sum_i m^{(i)} |H \cap K^{\alpha(i)}|$$

**全数検証結果（プリセット群）:**

| 群 | 総ケース数 | 成立 | 不成立 |
|---|---|---|---|
| S₃（6元） | 2,268 | 2,268 | 0 |
| D₄（8元） | 25,500 | 25,500 | 0 |
| Q₈（8元） | 9,180 | 9,180 | 0 |
| Z₆（6元） | 1,008 | 1,008 | 0 |
| **合計** | **37,956** | **37,956** | **0** |

---

## Ta9 — セクト・位数の法則

**検証定理:**

$$\text{Theorem 2.6:} \quad |H_1 H_2 \cdots H_n| \equiv 0 \pmod{\mathrm{lcm}(|H_1|, |H_n|)}$$

$$\text{Theorem 3.9:} \quad |H_1 H_2 \cdots H_n| \geq n \times \max(|H_1|, |H_n|) \quad \text{(irredundantのとき)}$$

$$\text{Theorem 4.32:} \quad |G| - |K_1 K_2 \cdots K_m| \geq \max(|K_1|, |K_m|)$$

**全数検証結果（プリセット群）:**

| 群 | 総セクト数 | Thm 2.6 | Thm 3.9 | Thm 4.32 | 不成立 |
|---|---|---|---|---|---|
| S₃（6元） | 208 | 208 | 208 | 208 | 0 |
| D₄（8元） | 999 | 999 | 999 | 999 | 0 |
| Q₈（8元） | 208 | 208 | 208 | 208 | 0 |
| Z₆（6元） | 68 | 68 | 68 | 68 | 0 |
| **合計** | **1,483** | **1,483** | **1,483** | **1,483** | **0** |

---

## SCh(G) — 完全不変量の探索

相乗チャウ環 SCh(G) を用いて、非同型な群が識別できるかを実験します。

**注意:** 「指紋が違う → 確実に非同型（100%信頼）」ですが、「指紋が同じ → 同型とは限らない」点に注意してください。このツールは簡易的なフィルターであり、SCh(G) が完全不変量かどうかは未解決問題です。

**全ペア比較結果（登録8群、28ペア）:**

| 結果 | ペア数 |
|---|---|
| SCh(G) で区別できた（非同型ペア） | 28 |
| 反証候補（SCh一致かつ非同型） | 0 |

---

## カスタム群 検証・計算

基本群（Z_n・D_n・S_n・Q₈）を直積で組み合わせて任意の有限群を構成し、全定理を検証・計算できます。

**対応している基本群:**

| 記号 | 内容 | 制限 |
|---|---|---|
| Z_n | 位数nの巡回群 | n ≤ 20 |
| D_n | 位数2nの二面体群 | n ≤ 20 |
| S_n | n!元の対称群 | n ≤ 4（S₅以上は計算コスト過大のため対象外） |
| Q₈ | 四元数群（8元） | — |

直積（×）で組み合わせ可能。位数128超は制限あり。

**計算の透明性:** 各ステップの計算過程（シナジーの全写像・両側コセット分解・重複度）を全て表示します。

---

## 総計 / Total

プリセット群による全検証ケース合計 **39,439 件**、不成立 **0 件**。

---

## References / 参照論文

- Takamura, S. "Bézout type theorem for higher order objects of groups" (2024), to appear in *Osaka Journal of Mathematics.* [Ta10]
- Takamura, S. "The orders of subgroup products and coset products", *Transactions on Combinatorics*, 14(4), 223–250, 2025. DOI: [10.22108/toc.2024.141562.2176](https://doi.org/10.22108/toc.2024.141562.2176) [Ta9]
- Takamura, S. "Intersection theory for groups and their Chow rings" (2025), Preprint. [Ta13]

---

## License / ライセンス

[![CC BY-NC-ND 4.0](https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/)

This work is licensed under [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).
