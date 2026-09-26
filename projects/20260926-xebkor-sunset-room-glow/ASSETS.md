# Asset Plan

All output paths are local-only and remain untracked.

| ID | Role | Provider | Duration | Inputs | Local output | Status |
|---|---|---|---:|---|---|---|
| I01 | Cast/room/astronaut-lamp continuity still | Jimeng | n/a | supplied astronaut-lamp images | `assets/image/identity-room-lamp.png` | READY |
| I02 | Loop-opening still | Jimeng | n/a | I01 + supplied astronaut-lamp images | `assets/image/opening-frame.png` | BLOCKED_REFERENCE |
| S01 | Lift astronaut lamp | Google Flow | 1.2 s | I01/I02 | `assets/video/shot_001.mp4` | BLOCKED_FLOW |
| S02 | Place, aim, switch | Google Flow | 2.0 s | S01 end + supplied astronaut-lamp images | `assets/video/shot_002.mp4` | BLOCKED_FLOW |
| S03 | Circle to sunset glow | Google Flow | 2.0 s | S02 final frame | `assets/video/shot_003.mp4` | BLOCKED_FLOW |
| S04 | Room-glow payoff | Google Flow | 6.6 s | S03 final frame | `assets/video/shot_004.mp4` | BLOCKED_FLOW |
| S05 | Retract and loop | Google Flow | 2.2 s | S04 end + I02 | `assets/video/shot_005.mp4` | BLOCKED_FLOW |

The supplied product images are the factual product references. Do not commit raw media to Git.
