# Reference: prototype-with-claude

When you open `https://github.com/sinned/prototype-with-claude`, here is what you will find and what to do.

## What the repo is

`prototype-with-claude` is a build environment for AI feature prototyping. It
teaches the workflow:

```
Write SKILL.md → Run in Claude Code → Eval → Improve → Export to Python
```

It is not a general coding environment. It is specifically designed for building
and validating AI agent behaviors before writing production code.

## What you will find

```
prototype-with-claude/
├── WALKTHROUGH.md          ← Read this first (20-min lead qualifier build-along)
├── .claude/
│   ├── skills/
│   │   ├── qualify-lead/   → /qualify-lead <company>    (built-in example)
│   │   ├── research-agent/ → /research-agent <topic>    (built-in example)
│   │   ├── generate-content/ → /generate-content        (built-in example)
│   │   └── starter-agent/  → template to copy
│   └── commands/
│       ├── new-skill.md    → /new-skill    (guided wizard)
│       ├── eval-skill.md   → /eval-skill   (grade outputs)
│       ├── improve-skill.md → /improve-skill (fix failures)
│       └── export-to-sdk.md → /export-to-sdk (generate Python)
└── docs/
    ├── skill-patterns.md   ← Design patterns for the three skill shapes
    └── sdk-migration-guide.md ← How to graduate to production
```

## What to do when you open it

**Step 1: Read WALKTHROUGH.md** (10 min) — understand the eval/improve loop

**Step 2: Run `/new-skill`** — this starts a guided wizard that asks you:
- What is the job? (use your prototype scope document)
- What are the inputs? (from your scope)
- What does success look like? (from your success criteria)

**Step 3: Write the SKILL.md** with Claude's help. Use your prototype scope as input.

**Step 4: Run your first test case.** Your test case from the scope document becomes
your first eval case.

**Step 5: Run `/eval-skill`** — Claude grades the output against your criteria.

**Step 6: Run `/improve-skill`** — Claude edits the SKILL.md to fix failures.

**Step 7: Repeat** until the behavior is reliable on your test cases.

**Step 8: Return to `founding-with-claude`** and run `/prototype-review`.

## The three skill patterns (relevant to your build)

Your prototype likely fits one of these:

| If your prototype... | Pattern | Use as starting point |
|---------------------|---------|----------------------|
| Researches, gathers, and synthesizes information | Research & Synthesize | `examples/01-research-agent/` |
| Takes input and scores/classifies it | Score & Classify | `examples/02-lead-qualifier/` |
| Takes a brief and produces content variations | Generate & Iterate | `examples/03-content-generator/` |

## Time expectations

- Writing your first SKILL.md: 15-30 minutes with `/new-skill`
- First test run: 2-5 minutes
- One eval/improve cycle: 10-15 minutes
- Getting to reliable behavior: 2-4 cycles (30-60 minutes total)

Plan for 2-4 hours total for a simple prototype skill.
Plan for 1-2 days for a skill with complex tool use or multiple steps.
