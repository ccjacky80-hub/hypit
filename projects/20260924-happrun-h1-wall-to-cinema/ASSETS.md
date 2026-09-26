# Asset Plan

No assets have been generated. Paths below are local production paths and must remain untracked.

| ID | Role | Provider | Duration | Inputs required | Output path | Status |
|---|---|---|---:|---|---|---|
| I01 | Cast/room/device continuity still | Jimeng | n/a | product references | `assets/image/identity-room-projector.png` | BLOCKED_REFERENCE |
| I02 | Opening-frame composition still | Jimeng | n/a | I01 + product references | `assets/image/opening-frame.png` | BLOCKED_REFERENCE |
| S01 | Creator lifts projector | Google Flow | 1.2 s | I01/I02 | `assets/video/shot_001.mp4` | BLOCKED_FLOW |
| S02 | Place and power on | Google Flow | 2.0 s | S01 end + product references | `assets/video/shot_002.mp4` | BLOCKED_FLOW |
| S03 | Projection gains depth | Google Flow | 2.0 s | S02 final frame | `assets/video/shot_003.mp4` | BLOCKED_FLOW |
| S04 | Cross into cinema world | Google Flow | 6.6 s | S03 final frame | `assets/video/shot_004.mp4` | BLOCKED_FLOW |
| S05 | Lens-collapse loop return | Google Flow | 2.2 s | S04 end + I02 | `assets/video/shot_005.mp4` | BLOCKED_FLOW |

## Reference intake convention

Place factual product images under `assets/reference/product/` and any source video under `assets/reference/reference-video/`. Do not add those media files to Git; only this plan and prompt text are versioned.
