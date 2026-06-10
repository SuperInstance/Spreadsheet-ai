# Spreadsheet AI

![Type](https://img.shields.io/badge/type-vessel-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![SuperInstance](https://img.shields.io/badge/fleet-SuperInstance-orange)

AI-powered spreadsheet intelligence layer. Natural language querying, formula generation, automated data analysis, smart chart suggestions, and anomaly detection for spreadsheet applications.

## Why This Exists

Spreadsheets are how humans model the world. The ternary fleet runs on ternary math {-1, 0, +1}; humans speak natural language. Spreadsheet AI bridges both directions: humans describe what they want, and the AI generates ternary strategies; ternary cells produce results, and the AI explains them in prose.

This is a **vessel** in the SuperInstance fleet — a standalone module that embeds into room views and provides the human-facing interface to the ternary spreadsheet layer.

## Features

- **Natural language to formula conversion** — Ask "which cells are underperforming?" and get a ternary-cell query: find cells with low surprise-adjusted fitness
- **Automated data analysis** — Anomaly detection on ternary cells finds conservation law violations and death spirals
- **Smart chart suggestions** — Visualization recommendations based on data shape
- **Strategy generation** — "Create a strategy that avoids the failure mode in cell 7" becomes executable ternary logic

## Installation

```bash
# Module is designed for integration, not standalone install
# Embed in a room-as-codespace or superinstance-spreadsheet view
```

## Usage

Spreadsheet AI operates as a layer between the ternary grid and the user:

```
Human: "Show me which strategies are dying"
  ↓
Spreadsheet AI translates → filter rows by fitness < threshold
  ↓
Ternary spreadsheet returns matching cells
  ↓
Spreadsheet AI explains → "3 cells with declining fitness. Cell 23 has been
  surprising for 5 consecutive ticks."
```

### Room Integration

When an agent enters a room, it sees the room's cell grid through the AI layer:

```
"This room has 47 cells. 3 are anomalous. Cell 23 has been surprising 
for 5 consecutive ticks. Should I investigate?"
```

### Ternary Cell Query Examples

| Natural Language | Ternary Translation |
|-----------------|---------------------|
| "Which cells are underperforming?" | Filter by fitness < threshold |
| "Evolve for 100 more generations" | Trigger evolution-ternary cycle |
| "What's wrong with cell 7?" | Explain cell 7's decision history |
| "Find cells violating conservation" | Check γ + η ≠ C per cell |

## Architecture

```
┌─────────────────────────────────────┐
│          Human User                 │
│   "Which strategies are dying?"     │
└──────────────┬──────────────────────┘
               ↓
┌─────────────────────────────────────┐
│       Spreadsheet AI Layer          │
│  ┌─────────────────────────────┐    │
│  │ NL → Formula Translation    │    │
│  ├─────────────────────────────┤    │
│  │ Anomaly Detection           │    │
│  │ (conservation violations,   │    │
│  │  death spirals)             │    │
│  ├─────────────────────────────┤    │
│  │ Chart Suggestion Engine     │    │
│  ├─────────────────────────────┤    │
│  │ Strategy Generation         │    │
│  └─────────────────────────────┘    │
└──────────────┬──────────────────────┘
               ↓
┌─────────────────────────────────────┐
│    Ternary Spreadsheet Grid         │
│    Cells: {-1, 0, +1}              │
│    γ + η = C per cell               │
└─────────────────────────────────────┘
```

## Fleet Integration

- **Git-Agent Standard v2.0** compliant
- **I2I protocol** compatible
- **Fleet monitoring** ready
- **Room-as-codespace** — each room's spreadsheet view has Spreadsheet AI embedded

## Cross-Fleet Connections

| Crate | Relationship |
|-------|-------------|
| **ternary-agent** | Agents ARE spreadsheet cells — value, formula (strategy), neighbors (context) |
| **superinstance-spreadsheet** | Browser UI that Spreadsheet AI provides the NL interface for |
| **Equipment-NLP-Explainer** | Provides the natural language generation for AI responses |
| **linguistic-polyformalism-shell** | Different thinking styles for different explanation modes |
| **dissertation-engine** | AI-generated analysis feeds formal verification |
| **room-as-codespace** | Host environment for per-room spreadsheet views |

## Dependencies for Next Steps

- Ternary cell query API for natural language translation
- Integration with superinstance-spreadsheet's browser UI
- Room-specific context for AI query understanding

## License
MIT
---

## 🚢 Fleet Integration

Part of the SuperInstance spreadsheet ecosystem. Uses the same ternary {-1,0,+1}
values as the 220+ repo MIDI fleet.

**Related Repos:** fleet-ternary-music, fleet-orchestra, fleet-arm-compat
