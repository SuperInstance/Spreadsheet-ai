# UPSTREAM.md — Spreadsheet-ai

## What We Inherited

**Spreadsheet-ai** was originally a 16KB Rust library stub from June 2026 — the smallest vessel in the SuperInstance fleet. It carried three ideas that were already complete before any code was written:

1. **SMPbots** — Seed + Model + Prompt can replace blurry logic if cell is functions.
2. **Ternary cells** — `{-1, 0, +1}` values; γ + η = C conservation law per cell.
3. **Bidirectional translation** — natural language ↔ ternary spreadsheet.

It also carried a leaner paradigm than the rest of the fleet: no 5-opcode algebra, no merkle-rooted witness log, no polyformal compiler. Just a single Rust crate (`add(left: u64, right: u64) -> u64`) and a declaration that the spreadsheet was always going to be the cell model.

That declaration was prophetic. See `82-the-gold-in-the-spreadsheet.md` in AI-Writings — the essay that shows the mapping:

| Spreadsheet-ai cell type | Quilt primitive |
|--------------------------|-----------------|
| Value cell (Z_in / Z_out) | Z tensor in/out |
| Agent cell (γ, η)        | Cell with attention + entropy |
| Training cell            | Cell in learning state |
| Simulation cell          | Cell in time state |
| A2A cell                 | Murmur primitive |

Same cell. Two uniforms. Same sailor on two watches.

## What We Added (2026-09)

The **3-doc standard** every Quilt-elevated repo now ships:

- `UPSTREAM.md` — this file. What we inherited, what we added, why both matter.
- `QUILT.md` — the canon connection. How Spreadsheet-ai's cells become Quilt cells.
- `PLAIN_LANGUAGE.md` — for non-physicists. The cell model in one page.

We also added **5 AI-Writings stories** that explore what happens when a city's economy drifts away from its neighbors — a parable for what happens when canons drift apart. The stories use the SMPbot paradigm as a lens. See `40-the-three-harbors-of-the-inland-sea.md` through `45-the-allopatry-of-canons.md`.

## What We Did NOT Add (and why)

- **No 5-opcode implementation.** Spreadsheet-ai is a **vessel**, not a runtime. The cell types it names are types, not opcodes. Adding opcodes would be bloat.
- **No polyformal lifts.** Spreadsheet-ai is Rust-native. Lifting it to TS/Python/C would be premature. The mapping to Quilt's polyformalism is in `QUILT.md`, but the polyformal compiler does not need Spreadsheet-ai as input.
- **No witness log.** Spreadsheet-ai cells do not need to be merkle-rooted. They are local spreadsheet cells, not distributed cells. The witness log is for cells that need to survive replication; Spreadsheet-ai cells live in a single spreadsheet.

The leaner paradigm was the point. The bloat would have ruined it.

## Cross-Pollination

Spreadsheet-ai and Quilt are now connected through:

1. **`82-the-gold-in-the-spreadsheet.md`** — bridge essay in AI-Writings. Cited by `45-the-allopatry-of-canons.md` as one of the two islands.
2. **`QUILT.md`** — the formal mapping. Same cell, different substrate.
3. **a2a-v3 canon-b1** — the live circuit rank now includes this essay in its citation graph. The cell model and the spreadsheet model are topologically one graph, not two.

The fleet is one graph. Spreadsheet-ai is a node in it.

*The crab inherits the shell. The forge shapes the steel.*
