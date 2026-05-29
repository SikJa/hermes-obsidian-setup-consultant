---
name: obsidian-setup-consultant
description: "Use this skill whenever the user wants to install, configure, migrate, design, or connect Obsidian as a second brain, knowledge base, cloud-synced vault, or AI/Hermes-readable memory. It is especially important when the user asks for an Obsidian setup prompt, vault architecture, folder structure, plugin recommendations, Obsidian Sync/iCloud/Drive/Git/Syncthing choices, Web Clipper workflows, or Hermes/agent integration. Always start with the 10-question discovery before proposing a final vault structure unless the user already answered them."
---

# Obsidian Setup Consultant

Use this skill to guide someone from zero to a usable Obsidian vault that can work as a second brain, project memory, research base, or agent-readable knowledge system.

The goal is not to create the most complex Obsidian possible. The goal is to make a vault the user will actually use, with a clear capture flow, stable folders, and a structure that future AI agents can read without guessing.

## Core principle

Obsidian is a folder of Markdown files. That makes it ideal for humans and agents:

- Humans use Obsidian to browse, link, write, graph, clip and review.
- Agents such as Hermes can use filesystem tools to search, read, create, patch and organize notes.
- Cloud/sync is optional; it only decides where the folder lives and how devices share it.

## Start with 10 questions

Before proposing structure or plugins, ask these questions and wait for answers:

1. What do you want to use Obsidian for mainly: business, study, projects, writing, personal life, research, AI agents, or a mix?
2. What information will you save most often: notes, PDFs, links, videos, transcripts, audios, ideas, tasks, clients, code, or documentation?
3. Do you want a simple folder structure or a more complete personal operating system?
4. Will you use it on one computer, multiple computers, or also on mobile?
5. Which sync/cloud option do you prefer or already use: Obsidian Sync, iCloud, Google Drive, OneDrive, Dropbox, Git, Syncthing, or local only?
6. Do you want Hermes or another AI agent to read, search, create and edit notes in the vault?
7. What 3–7 big areas of life/work should exist from day one?
8. Do you want to preserve full sources separately from processed summaries?
9. Which plugin categories matter: navigation, Web Clipper, Canvas, Excalidraw, graph, calendar, tasks, Dataview, templates, or minimalism?
10. What is one real thing you will capture tomorrow, and how would you want to find it later?

If the user already provided some answers, only ask for the missing ones. Do not force all 10 again if the context is clear.

## Recommended output after answers

After the user answers, produce:

1. **Case summary** — 5 bullets about the user's actual needs.
2. **Recommended setup** — local/cloud/Hermes-friendly recommendation.
3. **Folder structure** — concise tree with human names.
4. **What goes where** — explain each folder and what does not belong there.
5. **Capture workflow** — inbox → full source → processed note → project/area.
6. **Plugin list** — minimum plugins and optional plugins.
7. **Cloud/sync guidance** — recommendation and conflict risks.
8. **Hermes/AI integration** — how the agent should read/write the vault.
9. **Templates** — source note and processed note.
10. **Installation checklist** — step-by-step for the user's OS/devices.

## Default vault architecture

Use this as a starting point, then adapt:

```text
00 Centro/
  Inbox/
  Plantillas/
  Índices/
01 Negocio/
02 Contenido/
03 Proyectos/
04 Sistema IA/
05 Aprendizaje/
06 Personal/
90 Fuentes/
```

For a Syka-style agent-readable vault, prefer:

```text
00 Centro/El Origen/00_Por procesar/
00 Centro/El Origen/01_Procesadas/
00 Centro/El Origen/02_Requiere pregunta/
00 Centro/El Origen/03_Duplicados/
01 Negocio/
02 Marca personal/
03 Proyectos/
04 Syka System/
05 Aprendizaje/
06 Personal/
90 Fuentes/
Excalidraw/
```

Avoid too many top-level folders at the start. A vault becomes useful because the capture and review workflow works, not because the taxonomy is perfect.

## Installation checklist

### Desktop

1. Download Obsidian from `https://obsidian.md`.
2. Install it normally.
3. Create a new vault or open an existing folder.
4. Choose a stable folder path that agents and backup tools can access.
5. Create the initial folders.
6. Add templates.
7. Enable only the plugins needed right now.
8. Test capture: create one source note and one processed note.
9. Test search and wikilinks.
10. If using Hermes, verify the agent can read the vault path.

### Mobile / sync

- **Obsidian Sync:** simplest and safest for most users; paid but fewer conflicts.
- **iCloud:** convenient for Apple-only users; can create file availability issues if files are offloaded.
- **Google Drive / OneDrive / Dropbox:** works on desktop; mobile support varies and can create sync conflicts.
- **Git:** good for technical users; not ideal for non-technical mobile-first users.
- **Syncthing:** powerful local/private sync; requires setup discipline.

Warn the user: do not edit the same note simultaneously from multiple devices when using generic cloud sync.

## Plugin recommendations

Start small.

Minimum:

- **Obsidian Web Clipper** — capture web pages into an inbox.
- **Templates / core templates** — consistent source and processed notes.
- **Canvas** — visual maps when needed.
- **Graph view** — useful for exploration, not mandatory for daily workflow.

Optional:

- **Excalidraw** — diagrams and hand-drawn visual thinking.
- **Dataview** — dashboards from metadata; only if the user accepts structure.
- **Tasks** — if Obsidian will manage tasks.
- **Calendar/Periodic Notes** — only if the user explicitly wants daily/weekly notes.
- **Advanced Canvas / graph plugins** — visual users and presentations.
- **Notebook Navigator / vertical tabs** — better navigation for large vaults.

For Sikora's current vault, known community plugins include: cognitive-glow, notebook-navigator, vertical-tabs, 3d-graph, advanced-canvas, obsidian-excalidraw-plugin, obsidian-living-graph.

## Hermes / AI integration pattern

When connecting Obsidian to Hermes or another agent, explain it simply:

1. Obsidian stores notes as Markdown files in a normal folder.
2. Hermes can use file tools to search, read, write and patch those files.
3. The vault needs a clear schema so the agent knows where things belong.
4. The agent should read rules/index files before reorganizing.
5. Important sources should be preserved complete; summaries are separate.
6. The agent should update indexes/logs only for meaningful changes.

Recommended operating rule:

```text
User captures raw material → Inbox
Agent reads full source → classifies it
Agent preserves source → creates processed note
Agent links it to area/project → updates index if useful
```

## Templates

### Source note template

```markdown
---
type: source
status: inbox
created: YYYY-MM-DD
source_url:
areas: []
projects: []
---

# Title

## Original source

[Paste or preserve the complete source here.]

## Notes

- 
```

### Processed note template

```markdown
---
type: processed-note
status: active
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: []
areas: []
projects: []
---

# Title

## Summary

## Key ideas

## Decisions / implications

## Actions

## Links

- [[Related note]]
```

## Common mistakes to prevent

- Creating a huge folder system before the user has a capture habit.
- Mixing raw sources and polished notes in the same place without labels.
- Treating Obsidian as a task manager by default.
- Adding too many plugins on day one.
- Using cloud sync without explaining conflict risks.
- Letting agents rewrite or summarize sources without preserving originals.
- Creating folders with cryptic names the user will not remember.

## Short answer format

When the user wants a quick resource for a video description, give:

- a mini recap of the setup;
- the 10-question prompt;
- a short plugin list;
- the Hermes connection explanation;
- one copy-paste block.
