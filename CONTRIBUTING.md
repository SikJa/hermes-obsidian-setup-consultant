# Contributing

Thanks for considering a contribution to **Obsidian Setup Consultant**.

This project is intentionally small: the goal is to make it easier for humans and AI agents to create Obsidian vaults that are simple, portable, and useful.

## Useful contributions

Good first contributions include:

- testing the skill with a real Obsidian setup and reporting confusing steps;
- adding example vault structures for specific use cases;
- improving templates for source notes, processed notes, project notes, or index notes;
- documenting sync pitfalls for iCloud, Google Drive, OneDrive, Dropbox, Git, or Syncthing;
- adding screenshots or short walkthroughs;
- improving multilingual documentation.

## How to propose a change

1. Open an issue describing the use case or problem.
2. Keep the default setup beginner-friendly.
3. Preserve the core principle: raw sources should not be overwritten by AI summaries.
4. Submit a pull request with a concise explanation and, when possible, a before/after example.

## Skill editing guidelines

When editing `skill/obsidian-setup-consultant/SKILL.md`:

- keep the frontmatter valid;
- keep the 10-question discovery flow intact unless improving it directly;
- avoid adding too many plugins as defaults;
- prefer practical examples over abstract advice;
- include safety notes for agent-written files.

## Maintainer checklist

Before merging:

- [ ] The change keeps the setup understandable for non-technical users.
- [ ] Raw-source preservation is still explicit.
- [ ] Agent rules are safe and do not encourage destructive rewrites.
- [ ] README links still work.
- [ ] Examples are realistic and reusable.
