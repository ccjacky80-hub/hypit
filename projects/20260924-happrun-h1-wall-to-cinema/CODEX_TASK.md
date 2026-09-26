# Codex Task — Execute HAPPRUN H1 Production

## Source of truth

Read `STATUS.md`, then `direction.md`, `script.md`, `shots.md`, `ASSETS.md`, and the prompt files.

## Current authorized scope

- Maintain this text production package.
- When the required reference inputs and generation authority are available, generate only the asset IDs marked `READY` in `ASSETS.md`.
- Do not change any LOCKED decision.

## Prohibited

- Do not generate before product reference images are present.
- Do not add generated MP4 files, raw media, credentials, caches, or runtime results to Git.
- Do not substitute a model for Google Flow without an explicit instruction.
- Do not make unsupported product or personal-use claims.

## After an authorized generation pass

1. Save clips under `assets/video/shot_XXX.mp4` and stills under `assets/image/` locally.
2. Update `STATUS.md` with the exact generated assets and any technical deviation.
3. Render locally to `output/v1.mp4`; keep output excluded from Git.
4. Request visual QC before publishing.
