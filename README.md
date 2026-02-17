# Moat or Mirage

Evaluate whether a company's defensibility is real or dissolves when anyone can build software.

A [Claude Code skill](https://code.claude.com/docs/en/skills) that implements the [Reality's Moat](https://davidbeyer.xyz/writing/realitys-moat) framework.

## Install

### Claude Code (recommended)

```bash
# Personal — available across all your projects
cp -r moat-or-mirage ~/.claude/skills/moat-or-mirage

# Or project — available to your team via version control
cp -r moat-or-mirage .claude/skills/moat-or-mirage
```

Then invoke with `/moat-or-mirage` or let Claude load it when you ask about defensibility.

### Any LLM

Copy the contents of [`SKILL.md`](SKILL.md) and [`references/framework.md`](references/framework.md) into your system prompt or conversation.

## The Framework

When code costs nothing, the only defensible advantage is **scar tissue** — operational knowledge earned in a shifting system where the current state isn't self-explanatory.

The skill scores companies across 7 dimensions:

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

```
/moat-or-mirage [paste memo or company description + URL]
```

The skill will:
1. **Extract** company details and claimed advantages
2. **Research** evidence for/against each dimension
3. **Dissolve** advantages that don't survive free code
4. **Score** all 7 dimensions with evidence-backed ratings
5. **Synthesize** a scorecard, archetype match, and verdict

## What You Get

- Disqualification table showing which claimed advantages dissolve
- 7-dimension scorecard with confidence ratings
- Archetype comparison (Stripe, Chegg, Epic, etc.)
- Temporal placement on the scar tissue accumulation curve
- Unbundling assessment for incumbents, vertical AI assessment for startups
- Three-paragraph verdict: what dissolved, what survives, the judgment

## Structure

```
moat-or-mirage/
├── SKILL.md                    # Main skill (workflow + rules)
├── references/
│   └── framework.md            # Scoring tables, archetypes, research questions
└── README.md
```

## License

MIT
