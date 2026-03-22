# Sources (SR-)

Raw inputs that feed the ideation pipeline. Sources are where everything begins — a paper you read, an observation you made, a conversation you had, telemetry from your system.

## Types

| Type | Description |
|------|-------------|
| `paper` | Academic papers, arXiv preprints, research |
| `article` | Blog posts, news articles, essays |
| `observation` | Something you noticed in your work or the world |
| `telemetry` | System metrics, logs, performance data |
| `conversation` | Ideas from talking with others |
| `book` | Books or book chapters |
| `video` | Talks, presentations, tutorials |

## Adding a Source

```bash
bun run ladder add source --title "Your source title" --type paper --url "https://..."
```

Or copy `TEMPLATE.md` and fill in the frontmatter.

## Downstream

Sources feed into **Ideas** (ID-). When a source sparks an idea, create an idea entry and link it back here.
