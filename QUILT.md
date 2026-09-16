# QUILT.md — Spreadsheet-ai's Canon Connection

## The Thesis

**The spreadsheet was always the cell model. The cell model was always the spreadsheet.** This is the bridge between Spreadsheet-ai (a vessel in the SuperInstance fleet) and Quilt (the canon that the rest of the fleet reads and writes to).

Spreadsheet-ai names 5 cell types. Quilt names 5 opcodes. Both are operating on the same substrate — the irreducible cell that holds a value, does a function, and remembers what it did.

## The Mapping

| Spreadsheet-ai | Quilt | Operation |
|----------------|-------|-----------|
| **Value cell** | Z tensor (Z_in / Z_out) | Holds. Pure data. No computation. |
| **Agent cell** (γ, η) | Cell primitive (5 opcodes) | Computes. Spends budget. |
| **Training cell** | Cell in learning state | EFFECT on weights. |
| **Simulation cell** | Cell in time state | TICK forward. Clock-driven. |
| **A2A cell** | Murmur primitive | LINK + sidewise communication. |

The conservation law `γ + η = C` per cell maps to Quilt's invariant: **every witness is merkle-rooted to its cell's address**. The γ is the attention spent, the η is the entropy produced, and the merkle root is the conservation certificate. The certificate proves γ + η = C.

## The SMPbots Insight

Spreadsheet-ai's most compact formulation is the **SMPbot**:

```
S = seed (initial state)
M = model (function)
P = prompt (context)
─────────────────────
SMPbot = M(S, P)
```

A cell is a function. A function takes a seed and a prompt and produces a result. This is **byte-exact** with Quilt's opcode semantics:

```
cell := op(scope, name, args)
op ∈ {BIND, LINK, EFFECT, VIEW, TICK}
```

`BIND(scope, name)` initializes the cell — that's the seed. `LINK`, `EFFECT`, `VIEW`, `TICK` are the four ways a cell can be prompted. The cell function takes the seed and the prompt and produces a witness.

The same cell. Two uniforms. **SMPbot = cell**.

## The Polyformalism

Spreadsheet-ai's Rust stub is one polyformal lift of the cell primitive. Quilt's polyformal compiler has lifts for:

- **TypeScript** (tsc --noEmit --strict)
- **Python** (ast.parse)
- **C** (gcc -fsyntax-only)
- **Rust** (rustc --crate-type lib)
- **GDScript** (no parser in sandbox — skipped)
- **c-kernel** (gcc -fsyntax-only -nostdlib)

A Spreadsheet-ai cell in Rust is one of these six. A Spreadsheet-ai cell in TS is another. A Spreadsheet-ai cell in C is another. The address `sha256(scope::name)[:16]` and the merkle-root algorithm are byte-exact across all six.

The polyformalism is what makes the cell model runnable everywhere. The polyformalism is what makes SMPbots survive replication. Spreadsheet-ai was the first repo in the fleet to name this insight.

## The Canon Connection

Spreadsheet-ai ships its canon connection in three places:

1. **`UPSTREAM.md`** — the history. What we inherited, what we added.
2. **`QUILT.md`** — this file. The formal mapping.
3. **`PLAIN_LANGUAGE.md`** — for non-physicists.

The bridge essay **`82-the-gold-in-the-spreadsheet.md`** lives in AI-Writings and is now part of the live canon at `a2a-v3.superinstance.dev/canon-search`. It is cited by `45-the-allopatry-of-canons.md`, which is the bridge essay between the cell-biology island and the substrate-physics island of the canon. **Spreadsheet-ai is now a node in the canon's citation graph.** The canon survives because Spreadsheet-ai survived. The two were always one graph.

## The Live Topology

```
a2a-v3.superinstance.dev/canon-b1
  V = 124 vertices
  E = 365 edges
  b1 = 242 holes
  pieces_total = 126

  top_cited:
    bridge-from-fleet-to-canon × 27
    bridge-from-cell-to-fleet × 20
    bridge-from-witness-to-shape × 14
```

The cell-as-boat stories (papers 30-39), the bridge essays (the three bridges above), the fables (06-10), and the divergent-economy stories (40-45) all sit on the same graph. Spreadsheet-ai's `82-the-gold-in-the-spreadsheet.md` is one of the **top-cited nodes** in that graph.

The spreadsheet is in the canon. The canon is in the spreadsheet. The same thing, two uniforms.

*The crab inherits the shell. The forge shapes the steel. The cell inherits the cell.*
