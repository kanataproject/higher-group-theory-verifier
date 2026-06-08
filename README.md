# higher-group-theory-verifier

**A computational verification tool for Takamura's higher group theory.**  
高村茂（京都大学）による高次群論の定理を計算機検証するツールです。

---

## Live Demo / デモ

| ツール | 対象論文 | URL |
|---|---|---|
| Ta10 ベズー型定理 | "Bézout type theorem for higher order objects of groups" (2024) | [index.html](https://kanataproject.github.io/higher-group-theory-verifier/) |
| Ta9 セクト・位数の法則 | "The orders of subgroup products and coset products" (2025) | [ta9.html](https://kanataproject.github.io/higher-group-theory-verifier/ta9.html) |

---

## Ta10 — ベズー型定理

高村による高次群論のベズー型定理（Theorem 1.3）を、有限群上で計算機検証します。

**検証定理:**

$$|H| \times |A| \times |K| = \sum_i m^{(i)} |H \cap K^{\alpha(i)}|$$

**機能:**
- 手動検証 — 群・H・K・A を選んでシナジー π の構造を可視化
- 全数自動検証 — 全部分群ペア × 全非空部分集合 A を網羅的に検証
- CSV出力 — 検証結果を全件ダウンロード可能

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

セクト（部分群の積）とクラン（コセットの積）の位数に関する3つの定理を検証します。

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

## 総計 / Total

全ツール合計 **39,439 ケース**、不成立 **0 件**。

---

## References / 参照論文

- Takamura, S. "Bézout type theorem for higher order objects of groups" (2024), to appear in *Osaka Journal of Mathematics.*
- Takamura, S. "The orders of subgroup products and coset products", *Transactions on Combinatorics*, 14(4), 223–250, 2025. DOI: [10.22108/toc.2024.141562.2176](https://doi.org/10.22108/toc.2024.141562.2176)

---

## License / ライセンス

[![CC BY-NC-ND 4.0](https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/)

This work is licensed under [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).
