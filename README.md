# higher-group-theory-verifier

**A computational verification tool for Takamura's higher group theory.**  
高村茂（京都大学）による高次群論のベズー型定理を計算機検証するツールです。

---

## Overview / 概要

This tool computationally verifies the **Bézout-type theorem** (Theorem 1.3)
from Takamura's higher group theory, using finite groups.

高村による高次群論のベズー型定理（定理1.3）を、有限群上で計算機検証します。

**Verified theorem / 検証定理:**

$$|H| \times |A| \times |K| = \sum_i m^{(i)} |H \cap K^{\alpha(i)}|$$

---

## Live Demo / デモ

🔗 https://kanataproject.github.io/higher-group-theory-verifier/

---

## Features / 機能

- **手動検証** — 群・H・K・A を選んでシナジー π の構造を可視化
- **全数自動検証** — 全部分群ペア × 全非空部分集合 A を網羅的に検証
- **CSV出力** — 検証結果を全件ダウンロード可能

---

## Exhaustive Verification Results / 全数検証結果

| 群 | 総ケース数 | 成立 | 不成立 |
|---|---|---|---|
| S₃（6元） | 2,268 | 2,268 | 0 |
| D₄（8元） | 25,500 | 25,500 | 0 |
| Q₈（8元） | 9,180 | 9,180 | 0 |
| Z₆（6元） | 1,008 | 1,008 | 0 |
| **合計** | **37,956** | **37,956** | **0** |

---

## Reference / 参照論文

Takamura, S. "Bézout type theorem for higher order objects of groups" (2024),  
to appear in *Osaka Journal of Mathematics.*

---

## License / ライセンス

[![CC BY-NC-ND 4.0](https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/)

This work is licensed under [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).
