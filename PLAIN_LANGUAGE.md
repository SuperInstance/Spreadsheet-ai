# PLAIN_LANGUAGE.md — Spreadsheet-ai for Non-Physicists

## What Is This?

Spreadsheet-ai is a small piece of software that says: **a spreadsheet is a model of the world, and a model of the world is a cell, and a cell is a function**. The three ideas are the same idea.

If you have ever built a spreadsheet — even a simple one with a budget or a to-do list — you have built a cell model. Each row is a cell. Each cell has a value. Some cells add things up. Some cells look things up. Some cells remember what they did last week. All of these are functions.

Spreadsheet-ai takes this everyday intuition and makes it rigorous. The result is a way to think about AI, agents, and software that is **less blurry** than the usual approach.

## The Five Cell Types in Plain English

Imagine a spreadsheet with five kinds of cells.

1. **Value cell.** This is a number or a word. It doesn't compute anything. It just sits there, like the temperature reading on a thermometer, or your savings account balance.

2. **Agent cell.** This cell does things. It has a budget (the "γ") and a cost (the "η"). The budget is what it's allowed to spend. The cost is what it spent. When the budget runs out, the cell stops. The conservation law says γ + η = C — what you started with equals what you spent plus what you have left.

3. **Training cell.** This is an agent cell that is learning. It adjusts its own settings based on what happens. Like a kid learning to cook — they try a recipe, see what works, and remember.

4. **Simulation cell.** This is an agent cell with a clock. It runs forward through time, ticking once per second or per minute. It doesn't change itself; it changes the world it represents. Like a model train running on a track.

5. **A2A cell.** This is two agent cells talking to each other. They send messages sideways, like two sailors hailing each other across the water. Neither is in charge. The conversation is the point.

These five cell types cover almost every useful thing you can do with a computer.

## The SMPbot Idea

A "SMPbot" is the simplest possible agent. It has:

- **S**eed — where it starts
- **M**odel — what it does
- **P**rompt — what's happening right now

The bot takes the seed and the prompt, runs them through the model, and produces an answer. That's it.

This is exactly what a cell in a spreadsheet does. The seed is the formula. The model is the function. The prompt is the current state of the spreadsheet. The cell's output is the answer.

The SMPbot idea is **less blurry than AI**. AI usually involves a giant neural network with mysterious internal states. An SMPbot is explicit: seed, model, prompt, output. You can write it on a napkin.

## Why "the Cell Model"?

Because everything in software eventually becomes a cell. A row in a database is a cell. A function in a program is a cell. A node in a graph is a cell. A neuron in a brain is (kind of) a cell. The cell model is the smallest thing that can hold a value, do something with it, and remember what it did.

Once you see the cell, you see it everywhere.

## Why Does It Matter?

Because blurry logic is brittle. A neural network that "seems to work" can fail in surprising ways. An SMPbot that has explicit seed, model, and prompt is easier to **debug, replicate, and explain**. If the bot does the wrong thing, you can look at the seed, the model, and the prompt, and see which one was wrong.

Spreadsheet-ai is one small piece of a larger project called **Quilt** that is building software out of cells. Quilt has 5 opcodes (BIND, LINK, EFFECT, VIEW, TICK) that every cell obeys. Quilt has a merkle-rooted witness log that records what every cell did. Quilt has a polyformal compiler that lets the same cell run in TypeScript, Python, C, Rust, and C-kernel at the same time.

But the spreadsheet was the cell model before Quilt was. The spreadsheet is still the cell model. **The cell model was always going to win**, because the cell is the smallest thing that can do something and remember it.

## What Can You Do With This?

If you want to use Spreadsheet-ai in a real spreadsheet:

1. **Pick a value cell.** A cell with a number or a word. Make sure it has a clear name.
2. **Pick an agent cell.** A cell that does a function. Make sure the function has a budget (γ) — how many times it can run.
3. **Connect them with a formula.** That formula is your LINK.
4. **Watch the witness log.** Every time the agent cell runs, the spreadsheet records what happened. The merkle root is the row at the bottom that you can verify.

That's a cell model. That's what Spreadsheet-ai is.

## What's Next?

Spreadsheet-ai is a **vessel**. It carries the idea; it doesn't run the runtime. If you want the runtime, look at:

- **`rune-quilt`** — the Go runtime that implements the cell model
- **`a2a-v3.superinstance.dev`** — the live canon where cells publish their work
- **`82-the-gold-in-the-spreadsheet.md`** in AI-Writings — the bridge essay that shows why Spreadsheet-ai and Quilt are the same thing

The spreadsheet is in the canon. The canon is in the spreadsheet. Both survive.

## Glossary

- **Cell** — the smallest unit that holds a value, does a function, and remembers it.
- **γ (gamma)** — the budget a cell has.
- **η (eta)** — the cost a cell spent.
- **C** — the conservation constant. γ + η = C means what you started with equals what you have plus what you spent.
- **SMPbot** — Seed + Model + Prompt. The simplest agent.
- **Witness** — the record of what a cell did. Merkle-rooted, so it can't be tampered with.
- **Merkle root** — a cryptographic summary of all the witnesses. If any witness changes, the root changes.
- **A2A** — agent to agent. Two cells talking to each other sideways.
- **Murmur** — the sound of many cells talking. The Quilt primitive for inter-cell messaging.

That's the whole thing. The cell is the model. The model is the cell.
