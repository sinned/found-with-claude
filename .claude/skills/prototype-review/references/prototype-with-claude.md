# Reference: prototype-with-claude (for Prototype Review)

When running `/prototype-review`, look for evidence of the build in `../prototype-with-claude`.

## Where to find prototype output

```
prototype-with-claude/
├── output/
│   ├── evals/          ← Eval reports (what criteria passed/failed)
│   └── [custom dirs]   ← Output from running the skill
└── .claude/skills/
    └── [your-skill]/
        └── SKILL.md    ← The actual behavior that was built
```

## What to read for the review

1. **The SKILL.md that was built** — in `.claude/skills/[skill-name]/SKILL.md`.
   Does it match what was scoped? Is the one job clear?

2. **The eval report** — in `output/evals/[skill-name]-report.md`.
   What percentage of criteria passed? What were the top failure patterns?

3. **Sample output** — any files in `output/` that show what the skill produced.
   Do the outputs match the success criteria from the prototype scope?

## What a strong build looks like

From `prototype-with-claude` conventions, a validated skill should:
- Have a clear SKILL.md with explicit steps and output format
- Pass 80%+ of its eval criteria
- Produce output that matches the stated format on real test cases
- Have gone through at least one `/improve-skill` cycle

## What a weak build looks like

Warning signs:
- SKILL.md has vague steps ("research the topic and produce a summary")
- No eval report exists (was never evaluated)
- Output is inconsistent across test cases
- The skill does too many things (scope creep during build)

If you see these signs in the prototype review, note them. They indicate the
behavior is not production-ready, even if it "looks okay on 3 examples."
