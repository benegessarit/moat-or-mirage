# Reality's Moat

A structured prompt for evaluating company defensibility when building software is free.

## The Framework

When code costs nothing, the only defensible advantage is **scar tissue** — operational knowledge earned in a shifting system where the current state isn't self-explanatory.

The prompt scores companies across 7 dimensions:

| # | Dimension | What it measures |
|---|---|---|
| D1 | Scar Tissue Ratio | Operational knowledge vs rebuildable code |
| D2 | Knowledge Type | Converging (anyone reaches same answer) vs diverging |
| D3 | System Dynamics | Settled vs shifting rules |
| D4 | Operational Depth | Observing the system vs operating in it |
| D5 | Compounding | Linear data vs width × depth accumulation |
| D6 | Verification Moat | Cost to build-your-own × cost of being wrong |
| D7 | System Replacement | Could the entire system be replaced? |

## Usage

Copy [`prompt.md`](prompt.md) into any LLM conversation as a system prompt or prefix. Then paste a company memo, pitch deck summary, or description.

The prompt will:
1. **Extract** company details and claimed advantages
2. **Research** evidence for/against each dimension
3. **Dissolve** advantages that don't survive free code
4. **Score** all 7 dimensions with evidence-backed ratings
5. **Synthesize** a scorecard, archetype match, and verdict

## Example Input

> Acme processes insurance claims for 200 mid-market carriers. Founded 2018. Claims their proprietary rules engine and dataset of 50M processed claims are key differentiators. https://acme.example.com

## What You Get

- Disqualification table showing which claimed advantages dissolve
- 7-dimension scorecard with confidence ratings
- Archetype comparison (Stripe, Chegg, Epic, etc.)
- Temporal placement on the scar tissue accumulation curve
- Three-paragraph verdict: what dissolved, what survives, the judgment

## License

MIT
