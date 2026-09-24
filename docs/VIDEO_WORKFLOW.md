# Video Production Workflow

## Goal
Turn a reference video or concept into a reproducible Hypit project while minimizing Codex reasoning/token usage.

## Stages

1. NEW
2. REFERENCE_ANALYSIS
3. CREATIVE_DIRECTION
4. PRODUCTION_LOCKED
5. ASSET_PLANNING
6. READY_FOR_CODEX
7. ASSET_GENERATION
8. RENDER_V1
9. V1_READY_FOR_QC
10. REVISION_REQUIRED
11. RENDER_V2
12. FINAL

## Phase 1 — Reference intake
Input:
- video URL or uploaded MP4
- target platform
- target duration
- business/content objective

ChatGPT analyzes the reference using a Hypit-oriented production model:
- hook
- narrative beats
- A-roll/B-roll
- shot boundaries
- camera behavior
- dialogue
- captions
- sound effects
- music
- overlays
- reusable structure
- word/dialogue anchors
- assets that need generation

Output: `REFERENCE_ANALYSIS.md`

## Phase 2 — Creative direction
ChatGPT and user decide:
- what remains faithful to the reference
- what changes
- final script
- characters
- locations
- style
- CTA
- model allocation
- target fidelity

Output: `PRODUCTION.md`

## Phase 3 — Asset planning
Every generated shot gets:
- shot id
- provider
- duration
- aspect ratio
- camera
- action
- dialogue
- prompt
- negative constraints
- input references
- output filename

Providers may include:
- Jimeng CLI
- Google Flow / Veo
- local assets
- Hypit-native/code-rendered visuals

Outputs:
- `ASSETS.md`
- `GENERATE.md`
- prompt files

## Phase 4 — Hypit authoring
ChatGPT prepares:
- main.svml
- recipes.svs if needed
- runtime/provider config if needed
- asset paths
- word/timeline anchors
- caption/effect logic

## Phase 5 — Codex handoff
Codex reads:
1. repository `AGENTS.md`
2. project `STATUS.md`
3. project `CODEX_TASK.md`

Codex should execute rather than redesign.

Typical tasks:
- install/check dependencies
- generate Jimeng assets from prompt files
- identify Flow assets requiring human generation
- run Hypit build/runtime
- fix technical/runtime errors
- render V1
- update STATUS.md

## Phase 6 — QC loop
User supplies rendered V1 to ChatGPT.
ChatGPT produces concrete QC:
- exact timecode
- problem
- required change
- regeneration requirement if any
- revised prompt when needed

Codex applies technical changes and rerenders.

## Local sync
Production branch:
`video-production`

Normal sync:
```bash
git checkout video-production
git pull
```

All final production artifacts should remain reproducible from repository files.
