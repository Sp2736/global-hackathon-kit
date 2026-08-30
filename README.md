# Antigravity Global Hackathon Engineering Kit

## What this is

A reusable Antigravity configuration kit for hackathons and general software projects.

It contains:

```text
GEMINI.md
  ↓
global always-on engineering behavior

skills/hackathon-engineering/SKILL.md
  ↓
deep reusable engineering skill

workflows/
  ↓
repeatable /hackathon-start, /ship and /review processes

resources/reference-vault.md
  ↓
tool/reference links
```

## Global installation

Google Antigravity currently supports global rules at:

```text
~/.gemini/GEMINI.md
```

Global skills are supported under:

```text
~/.gemini/config/skills/<skill-folder>/SKILL.md
```

So install:

```text
GEMINI.md
→ ~/.gemini/GEMINI.md

skills/hackathon-engineering/
→ ~/.gemini/config/skills/hackathon-engineering/
```

Global workflows can be created through Antigravity's Customizations → Workflows panel. The included workflow files are ready to copy into the global workflow configuration.

## Workspace installation

For a project-specific copy:

```text
.agents/
├── skills/
│   └── hackathon-engineering/
│       └── SKILL.md
└── rules/
    └── ...
```

Use workspace rules when a project needs different conventions from the global defaults.

## Important

The global `GEMINI.md` is the part intended to provide persistent global behavior.

The skill is reusable specialized knowledge. Antigravity discovers skills from their descriptions and activates relevant skills when appropriate; it should not be treated as a guarantee that every skill is injected into every prompt.

The official Antigravity docs currently document global rules, global skills, workspace skills/rules, workflows, and progressive skill disclosure.

## Updating the vault

When adding a new favorite tool:

1. Add the URL to `resources/reference-vault.md`.
2. Add a decision rule to `SKILL.md` only if it changes engineering behavior.
3. Keep `GEMINI.md` focused because global rules are persistent.
4. Prefer small specialized skills over turning one skill into an enormous universal instruction dump.
