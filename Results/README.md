# Results (RE-)

Verified outcomes from experiments. Results are the truth — what actually happened when a hypothesis was tested. Negative results are as valuable as positive ones.

## Outcomes

| Outcome | Description |
|---------|-------------|
| `success` | Hypothesis validated |
| `partial` | Some aspects confirmed, needs refinement |
| `failure` | Hypothesis invalidated — valuable learning |
| `inconclusive` | Need more data or better methodology |

## The Loop

The most important field in a result is `loops_to` — what does this result feed back into?

A result might suggest:
- A new **source** (something to investigate further)
- A new **idea** (a different approach to try)
- A new **hypothesis** (a refinement of the original)
- A validated **algorithm** (a proven method)

This feedback loop is what makes Ladder a system, not just a collection.

## Adding a Result

```bash
bun run ladder add result --experiment EX-00001 --title "Cache reduced p99 by 22%"
```

## Upstream

- **From**: Experiments (EX-)
- **Loops to**: Sources (SR-), Ideas (ID-), Hypotheses (HY-), Algorithms (AL-)
