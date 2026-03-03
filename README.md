# Instance Format (Short)

This dataset uses plain `.txt` files.

- **Line 1**: `T_max st_max`
- **Next lines**: node data, one node per line: `x y profit`
  - Node 1 = start depot
  - Node 2 = end depot
  - Remaining nodes = customers
- **Then**: coverage-time matrix for **L mode** (`CT_L`), with `n` rows and `n` values per row
- **Then one marker line**: `[CT_N]`
- **Then**: coverage-time matrix for **N mode** (`CT_N`), with `n` rows and `n` values per row

Notes:
- `n` is the total number of nodes in that file.
- Matrix diagonal entries are `0`.
- Use `CT_L` when solving in L mode, and `CT_N` when solving in N mode.
