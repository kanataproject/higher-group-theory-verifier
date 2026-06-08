# higher-group-theory-verifier

**A computational verification tool for Takamura's higher group theory.**  
高村茂（京都大学）による高次群論の定理を計算機検証するツールです。

---

## Live Demo / デモ

| ツール | 内容 | URL |
|---|---|---|
| Ta10 ベズー型定理 | シナジー π とベズー型定理の手動・全数検証 | [index.html](https://kanataproject.github.io/higher-group-theory-verifier/) |
| Ta9 セクト・位数の法則 | Thm2.6・Thm3.9・Thm4.32 の全数検証 | [ta9.html](https://kanataproject.github.io/higher-group-theory-verifier/ta9.html) |
| SCh(G) 完全不変量の探索 | 相乗チャウ環による群の識別実験 | [sch.html](https://kanataproject.github.io/higher-group-theory-verifier/sch.html) |
| カスタム検証 | 任意の有限群を定義して検証 | [custom.html](https://kanataproject.github.io/higher-group-theory-verifier/custom.html) |

---

## Ta10 — ベズー型定理

高村による高次群論のベズー型定理（Theorem 1.3）を、有限群上で計算機検証します。

**検証定理:**

$$|H| \times |A| \times |K| = \sum_i m^{(i)} |H \cap K^{\alpha(i)}|$$

**全数検証結果:**

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

**全数検証結果:**

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

**注意:** このツールの指紋は簡易的なフィルターです。「指紋が違う → 確実に非同型（100%信頼）」ですが、「指紋が同じ → 同型とは限らない」点に注意してください。

**全ペア比較結果（登録8群、28ペア）:**

| 結果 | ペア数 |
|---|---|
| SCh(G) で区別できた（非同型ペア） | 28 |
| 反証候補（SCh一致かつ非同型） | 0 |

---

## カスタム検証 — 任意の有限群で検証

乗積表を入力するだけで、任意の有限群に対して全定理を検証できます。既存の群だけでなく、研究者が独自に定義した群も検証対象にできます。

---

## 総計 / Total

全ツール合計 **39,439 ケース**、不成立 **0 件**。

---

## References / 参照論文

- Takamura, S. "Bézout type theorem for higher order objects of groups" (2024), to appear in *Osaka Journal of Mathematics.* [Ta10]
- Takamura, S. "The orders of subgroup products and coset products", *Transactions on Combinatorics*, 14(4), 223–250, 2025. DOI: [10.22108/toc.2024.141562.2176](https://doi.org/10.22108/toc.2024.141562.2176) [Ta9]
- Takamura, S. "Intersection theory for groups and their Chow rings" (2025), Preprint. [Ta13]

---

## License / ライセンス

[![CC BY-NC-ND 4.0](https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/)

This work is licensed under [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).
