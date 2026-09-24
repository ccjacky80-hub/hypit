# Project Execution Rules

Applies to all directories under `projects/`.

## Source of truth
Read in this order:
1. `STATUS.md`
2. `CODEX_TASK.md`
3. `PRODUCTION.md`
4. `ASSETS.md`
5. prompt files

## Locked decisions
If `STATUS.md` or `PRODUCTION.md` marks a decision as LOCKED:
- do not rewrite copy
- do not alter shot structure
- do not replace providers
- do not reinterpret the creative direction

Only make technical changes required to execute the specified production.

## Asset naming
Video:
`assets/video/shot_XXX.mp4`

Image:
`assets/image/<name>`

Audio:
`assets/audio/<name>`

Jimeng prompts:
`prompts/jimeng/shot_XXX.txt`

Flow prompts:
`prompts/flow/shot_XXX.txt`

## Human Flow handoff
When a Flow shot cannot be generated automatically:
- mark project status as `BLOCKED_FLOW`
- list exact missing shot IDs
- do not substitute another model without instruction

## Completion
After execution:
- save render to `output/v1.mp4` or specified target
- update `STATUS.md`
- record technical deviations
