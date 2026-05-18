# Treasure Hunt in the Exhibition Area

## Description

You are given a two-dimensional grid of size `n × n`.

The outer boundary of the grid is surrounded by walls; that is, every cell whose row index or column index equals `0` or `n + 1`
is considered a wall cell.

Inside the grid, there are additionally `m` wall cells,
while all remaining cells are empty cells.

It is guaranteed that all wall cells are **4-connected**.

You may move between empty cells according to the following rules:

- Moving one cell vertically or horizontally costs `2` seconds.
- Moving one cell diagonally costs `3` seconds.

For diagonal movement, it is only required that both the starting cell
and the destination cell are empty.

You are given `q` queries.  
For each query, determine the minimum required time to move
from one empty cell to another empty cell.

If the destination is unreachable, output `-1`.

---

## Input Format

The first line contains three integers:

```text
n m q
```

- `n` : size of the grid
- `m` : number of additional wall cells
- `q` : number of queries

The next `m` lines each contain two integers:

```text
x y
```

representing a wall cell.

The following `q` lines each contain four integers:

```text
x1 y1 x2 y2
```

representing a query from `(x1, y1)` to `(x2, y2)`.

---

## Output Format

For each query, output a single integer:

- the minimum required time, or
- `-1` if the destination cannot be reached.

---

## Constraints

```text
1 ≤ n ≤ 1e5
1 ≤ m, q ≤ 3e5
```

---

## Limits

- Time Limit: `4s`
- Memory Limit: `1024MB`

---

## Notes

- Horizontal/vertical moves use the 4-neighbor directions.
- Diagonal movement does **not** require checking intermediate corner cells.
- All wall cells are guaranteed to form a single 4-connected component.

---

## Example

### Input

```text
5 2 1
2 2
3 3
1 1 5 5
```

### Output

```text
12
```
