# Future Integration: Spreadsheet-ai

## Current State
An AI-powered spreadsheet intelligence layer providing natural language querying, formula generation, automated data analysis, smart chart suggestions, and anomaly detection. Standalone module for spreadsheet applications.

## Integration Opportunities

### With ternary-agent
The AI features (natural language query, formula generation, anomaly detection) map to ternary-agent's capabilities. A ternary agent IS a spreadsheet cell — it has a value, a formula (its strategy), and neighbors (its context). When a human asks "which cells are underperforming?", Spreadsheet-ai translates this into a ternary-cell query: find cells with low surprise-adjusted fitness. The AI layer makes the ternary grid accessible to non-technical users.

### With superinstance-spreadsheet
Spreadsheet-ai's natural language interface becomes the control panel for the ternary spreadsheet. "Show me which strategies are dying" → filter rows by fitness < threshold. "Evolve for 100 more generations" → trigger evolution-ternary. The AI layer is how humans drive the ternary world model without writing code.

### With room-as-codespace
Each room's spreadsheet view has Spreadsheet-ai embedded. When an agent enters a room, it sees the room's cell grid through the AI layer: "This room has 47 cells. 3 are anomalous. Cell 23 has been surprising for 5 consecutive ticks. Should I investigate?"

## Dormant Ideas Now Unlockable
The AI features were generic spreadsheet tools. Now the ternary spreadsheet gives them a specific, rich domain. Anomaly detection on ternary cells is scientifically meaningful — it finds cells that violate conservation laws or exhibit death spirals. Formula generation becomes strategy generation: "create a strategy that avoids the failure mode in cell 7."

## Potential in Mature Systems
Spreadsheet-ai is the bridge between the ternary fleet and human users. The fleet runs on ternary math; humans speak natural language. Spreadsheet-ai translates between them in both directions: humans describe what they want, Spreadsheet-ai generates ternary strategies; ternary cells produce results, Spreadsheet-ai explains them in prose.

## Cross-Pollination Ideas
- **Equipment-NLP-Explainer**: NLP Explainer provides the natural language generation for AI responses
- **linguistic-polyformalism-shell**: Different thinking styles for different explanation modes
- **dissertation-engine**: AI-generated analysis feeds formal verification

## Dependencies for Next Steps
- Ternary cell query API for natural language translation
- Integration with superinstance-spreadsheet's browser UI
- Room-specific context for AI query understanding
