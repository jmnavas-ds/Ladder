# Experiments (EX-)

Structured tests of hypotheses. An experiment takes a hypothesis and subjects it to reality — running the test, collecting data, and reporting what actually happened.

## Requirements

Every experiment must define:

1. **Methodology** — clear enough for reproduction
2. **Success criteria** — defined before running
3. **Data collection plan** — what you'll measure

## Adding an Experiment

```bash
bun run ladder add experiment --hypothesis HY-00001 --title "A/B test semantic cache"
```

## Upstream / Downstream

- **From**: Hypotheses (HY-)
- **To**: Results (RE-)
- **Uses**: Algorithms (AL-) for methodology
