# Voter Configuration and District Scenarios

## Grid

The game uses a 5×5 grid of 25 blocks: 15 cyan (C) and 10 green (G).
Rows are numbered 0–4 top to bottom; columns 0–4 left to right.
Each district contains exactly 5 contiguous blocks and is won by the party with a majority (≥3 blocks).

## Voter Configuration

Green forms a roughly diamond-shaped interior cluster, offset slightly left.
Rows 1 and 3 have green in columns 1–3; row 2 has green in columns 0–3.
The entire border and column 4 are cyan.

```
     Col: 0  1  2  3  4
Row 0:    C  C  C  C  C
Row 1:    C  G  G  G  C
Row 2:    G  G  G  G  C
Row 3:    C  G  G  G  C
Row 4:    C  C  C  C  C
```

---

## Scenario A: 4 Cyan, 1 Green — Cyan Gerrymander

Pack all green voters into one central district; spread the remaining green thin across four cyan-winning districts.

```
     Col: 0   1   2   3   4
Row 0:   [D2][D2][D2][D2][D2]
Row 1:   [D3][D1][D4][D4][D4]
Row 2:   [D3][D1][D1][D5][D4]
Row 3:   [D3][D1][D1][D5][D4]
Row 4:   [D3][D3][D5][D5][D5]
```

| District | Blocks                        | Composition | Winner |
|----------|-------------------------------|-------------|--------|
| D1       | (1,1)(2,1)(2,2)(3,1)(3,2)     | 5G          | Green  |
| D2       | (0,0)(0,1)(0,2)(0,3)(0,4)     | 5C          | Cyan   |
| D3       | (1,0)(2,0)(3,0)(4,0)(4,1)     | 4C + 1G     | Cyan   |
| D4       | (1,2)(1,3)(1,4)(2,4)(3,4)     | 3C + 2G     | Cyan   |
| D5       | (2,3)(3,3)(4,2)(4,3)(4,4)     | 3C + 2G     | Cyan   |

**Result: 4 cyan, 1 green**

---

## Scenario B: 3 Cyan, 2 Green — Proportional

Two green districts carve out the central blob; three cyan districts take the borders.

```
     Col: 0   1   2   3   4
Row 0:   [D3][D3][D3][D3][D4]
Row 1:   [D3][D2][D2][D2][D4]
Row 2:   [D1][D1][D1][D2][D4]
Row 3:   [D5][D1][D1][D2][D4]
Row 4:   [D5][D5][D5][D5][D4]
```

| District | Blocks                        | Composition | Winner |
|----------|-------------------------------|-------------|--------|
| D1       | (2,0)(2,1)(2,2)(3,1)(3,2)     | 5G          | Green  |
| D2       | (1,1)(1,2)(1,3)(2,3)(3,3)     | 5G          | Green  |
| D3       | (0,0)(0,1)(0,2)(0,3)(1,0)     | 5C          | Cyan   |
| D4       | (0,4)(1,4)(2,4)(3,4)(4,4)     | 5C          | Cyan   |
| D5       | (3,0)(4,0)(4,1)(4,2)(4,3)     | 5C          | Cyan   |

**Result: 3 cyan, 2 green**

---

## Scenario C: 2 Cyan, 3 Green — Green Gerrymander

Slice the board into horizontal bands, giving green a plurality in three districts while cyan's votes are concentrated in two all-cyan districts.

```
     Col: 0   1   2   3   4
Row 0:   [DA][DD][DD][DD][DD]
Row 1:   [DA][DA][DA][DA][DD]
Row 2:   [DB][DB][DB][DB][DB]
Row 3:   [DE][DC][DC][DC][DC]
Row 4:   [DE][DE][DE][DE][DC]
```

| District | Blocks                        | Composition | Winner |
|----------|-------------------------------|-------------|--------|
| DA       | (0,0)(1,0)(1,1)(1,2)(1,3)     | 3G + 2C     | Green  |
| DB       | (2,0)(2,1)(2,2)(2,3)(2,4)     | 4G + 1C     | Green  |
| DC       | (3,1)(3,2)(3,3)(3,4)(4,4)     | 3G + 2C     | Green  |
| DD       | (0,1)(0,2)(0,3)(0,4)(1,4)     | 5C          | Cyan   |
| DE       | (3,0)(4,0)(4,1)(4,2)(4,3)     | 5C          | Cyan   |

**Result: 2 cyan, 3 green**

---

## Notes

The asymmetric shape of the green cluster — extending to column 0 in row 2 but not rows 1 or 3 — is what enables the horizontal-band strategy for the green gerrymander.

Two classic gerrymandering techniques are at work:

- **Packing** — concentrate one party's voters into a district where they win by a large margin, wasting their surplus votes.
- **Cracking** — split a party's voters across multiple districts where they are always in the minority.

For the cyan gerrymander (Scenario A), green is *packed* into D1 and *cracked* across D3–D5.
For the green gerrymander (Scenario C), cyan is *packed* into DD and DE while green is spread across three narrow-majority districts.
