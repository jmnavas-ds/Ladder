# Contributing to Ladder

Ladder welcomes contributions at every stage of the pipeline. Here's how to submit work.

## Quick Start

1. Fork the repository
2. Create a branch: `git checkout -b add-my-contribution`
3. Add your entry following the templates below
4. Commit: `git commit -m "Add: SR-00042 — Paper on semantic caching"`
5. Push and create a Pull Request

## Using the CLI

The fastest way to add entries:

```bash
# Add a source
bun run ladder add source --title "arXiv paper on neural caching" --type paper --url "https://arxiv.org/abs/..."

# Add an idea
bun run ladder add idea --title "Apply neural caching to API gateway" --source SR-00001

# Add a hypothesis
bun run ladder add hypothesis --idea ID-00001 --title "Neural cache reduces p99 latency by 30%"

# Add an experiment
bun run ladder add experiment --hypothesis HY-00001 --title "Load test with/without neural cache"

# Record a result
bun run ladder add result --experiment EX-00001 --title "Neural cache reduced p99 by 22%"

# Add an algorithm
bun run ladder add algorithm --title "Semantic similarity caching for REST APIs"
```

## Manual Entry

Each directory contains a `TEMPLATE.md`. Copy it, fill in the frontmatter and body, and name the file with the next available ID:

```
SR-00042—Neural_Caching_Paper.md
ID-00015—Apply_Neural_Caching.md
HY-00008—Cache_Reduces_Latency.md
```

## Entry Requirements

### All entries must have:
- Valid YAML frontmatter with all required fields
- A unique ID using the correct prefix
- A clear, descriptive title
- A status field (`draft`, `active`, `testing`, `complete`, `archived`)

### Linking
- Ideas should reference their source(s): `sources: [SR-00001, SR-00002]`
- Hypotheses must reference their parent idea: `idea: ID-00001`
- Experiments must reference their parent hypothesis: `hypothesis: HY-00001`
- Results must reference their parent experiment: `experiment: EX-00001`
- Algorithms can reference supporting experiments: `experiments: [EX-00001]`

## What Makes a Good Entry?

### Sources
- Include the URL or reference
- Categorize the type (paper, article, observation, telemetry, conversation)
- Note what caught your attention — what problem does this relate to?

### Ideas
- Be specific about what you'd do differently
- Note which cognitive phase this came from (CONSUME, DREAM, DAYDREAM, CONTEMPLATE, STEAL, MATE)
- Link to the source that inspired it

### Hypotheses
- Make it testable — "If X, then Y"
- Define what success looks like
- Specify the metric you'd measure

### Experiments
- Describe the methodology clearly enough for someone else to run it
- Specify the algorithm or approach used
- Define success criteria before running

### Results
- Report honestly — negative results are valuable
- Include the data or evidence
- Note what you'd do differently next time
- Flag if this result suggests a new source, idea, or hypothesis (the loop)

## Code of Conduct

Be honest. Report negative results. Don't fabricate data. The value of Ladder is in its integrity.
