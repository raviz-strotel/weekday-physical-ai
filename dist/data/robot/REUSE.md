# Public reference sample: BridgeData V2 spoon transfer

## Ready for the viewer
- `episode_000000.mp4`: H.264 video, 28 frames, 5 Hz, 256 × 256, 5.6 seconds.
- `episode.json`: all 28 source records, complete unrounded values and viewer metadata.
- `poster.jpg`: first frame. `inspection.png`: first/middle/last montage used for visual QA.
- Source AV1 video and Parquet retained alongside metadata and SHA-256 manifest.

Use the dataset's instruction, **put small spoon from basket to tray**. A visitor can scrub the actual video, see the corresponding recorded observation/state and action vector, and download/inspect one real sample. This makes the difference between a video and a robotics training record tangible. Do not invent grasp labels, bounding boxes, success scores, object poses or forces. Do not call the action values positions, joint angles or normalized commands. Metadata names dimensions x, y, z, roll, pitch, yaw, gripper but does not document units or absolute/delta convention.

Show timestamp as episode-relative seconds and choose the nearest frame using frame index / 5. Timestamps are stored as float32 and retain normal floating-point representation. Video duration 5.6 seconds includes 28 frame display intervals; the final frame timestamp is approximately 5.4 seconds. Camera-presence flags describe upstream streams, not additional fetched videos.

## Attribution to keep visible near the player
BridgeData V2, Walke et al. (CoRL 2023), CC BY 4.0. Community LeRobot conversion: jesbu1 (repository declares Apache-2.0). Video transcoded; records exported to JSON. Public reference sample, not collected by Weekday. No endorsement implied.

Project: https://rail-berkeley.github.io/bridgedata/
Original data license: https://creativecommons.org/licenses/by/4.0/
License legal code: https://creativecommons.org/licenses/by/4.0/legalcode.en
Conversion: https://huggingface.co/datasets/jesbu1/bridge_v2_lerobot/tree/3899a5d24770fa593ad09f6f6e22cd417a227431
Conversion-declared license: https://www.apache.org/licenses/LICENSE-2.0

The official project page explicitly says all data is CC BY 4.0. That license permits commercial redistribution and adaptations with attribution, license link and changes indicated. The conversion's permissive Apache declaration does not remove upstream attribution. Retain both notices. Do not add licensing terms that restrict the source material beyond its license.

## What this is not
This is a household manipulation reference, not manufacturing proof, a Weekday-owned collection, customer work or evidence of production service capacity. Original raw Bridge trajectory identifier is absent from inspected conversion metadata. No camera calibration, independently verified success annotation, precise action convention or upstream collection subtype is asserted for this individual episode. Resolve these gaps before any training use. Camera view and data dimensions are visible actual data, not synthetic animation.

## Reproducibility
See manifest.json for exact revision, source URLs, local sizes/hashes, transformations and validation. Only a tiny single episode was retrieved. No downloaded code was executed or pickle data loaded. The source task-index file was read with a 1 MB bound and only its complete first row was retained. All episode rows link task_index 0 to that instruction.
