# Shot list template

| shot_id | duration_s | shot_size | camera_move | subject | action | lighting | lens | prompt | audio | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| S01 | 3 | WS | static | a fishing boat at dawn | idles in flat water | blue hour, single warm lamp on deck | 24mm | Wide static shot of a small fishing boat at dawn, blue hour light, one warm lamp on the deck, flat water, 24mm, f/8, camera locked off, 24 fps | engine idle, water slap | establish location |
| S02 | 4 | MCU | slow push in | the skipper | checks a rope, looks up | soft side light from the east | 50mm | Medium close-up of a skipper checking a rope, slow push in, soft side light, 50mm, f/2.8, 24 fps | rope creak, gull | first human beat |

## Column guide

| Column | Fill with | Bad fill | Good fill |
| --- | --- | --- | --- |
| `shot_id` | `S01`, `S02` … | `final`, `good one` | `S03_v2` |
| `duration_s` | integer seconds | `short` | `4` |
| `shot_size` | one of ECU, CU, MCU, MS, WS | `close` | `MCU` |
| `camera_move` | one move, with its end state | `dynamic` | `slow push in, ends on the eyes` |
| `subject` | noun phrase | `mood` | `a man in his 40s, grey stubble` |
| `action` | a change over time | `standing` | `turns to the window` |
| `lighting` | direction + quality + colour | `nice light` | `hard key from camera right, 3200K` |
| `lens` | focal length + aperture | `wide` | `35mm, f/2.8` |
| `prompt` | composed sentence, ready to paste | — | see examples |
| `audio` | what is heard | — | `machine hum, door chime` |
| `notes` | continuity and failure modes | — | `focus pull at 2s; face drifts after 3s` |

## Filling order

1. `shot_size` — decide the frame.
2. `camera_move` — decide if anything moves, and where it ends.
3. `lighting` — decide direction, quality, colour.
4. `lens` — pick focal length to match the size you chose.
5. `action` — write the change, not the state.
6. `prompt` — compose in this order: subject + action, framing, lighting, lens, motion, texture.
7. `duration_s` — the shortest length that contains the action.
8. `audio` and `notes` — last, while you still remember what you were thinking.

## Rules that save re-renders

- One move per shot. A push and a pan in one prompt produces a drift in neither.
- Never write `{slot}` into a prompt you intend to render; replace it or delete it.
- If a shot fails twice, change the framing before you change the words.
- Keep approved rows frozen. Revisions get a new row with `_v2`, `_v3`.

## Licence

MIT — copy the table, the columns and the examples.
