# Codex Task

Do not redesign the video.

Before execution read:
1. repository `AGENTS.md`
2. project `STATUS.md`
3. project `PRODUCTION.md`
4. project `ASSETS.md`

## Goal
Execute the production plan and render the requested output.

## Rules
- Do not rewrite locked creative decisions.
- Do not rewrite prompts unless required for a technical compatibility fix.
- Prefer the provider specified in ASSETS.md.
- For Google Flow assets requiring manual generation, mark `BLOCKED_FLOW`.
- Update STATUS.md after material progress or blockers.

## Default execution sequence
1. Verify dependencies.
2. Verify required source assets.
3. Generate Jimeng assets from `prompts/jimeng/`.
4. Check whether Flow assets are present.
5. Run Hypit validation/build.
6. Fix technical/runtime errors only.
7. Render output.
8. Save to the path defined in STATUS.md.
9. Update STATUS.md.
