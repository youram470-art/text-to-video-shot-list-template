# Shot list template (for text-to-video shoots)

A shot list for AI video, in two formats: a spreadsheet you can plan in, and a Markdown version
you can put in a repo next to the renders. Built for the way text-to-video actually goes wrong —
not by forgetting the shot, but by forgetting which part of the shot was decided.

## Files

| File | What it is |
| --- | --- |
| [`shot-list-template.csv`](shot-list-template.csv) | empty template, 2 example rows, 11 columns |
| [`shot-list-template.md`](shot-list-template.md) | same columns as a Markdown table, with the column guide |
| [`examples/product-launch-30s.csv`](examples/product-launch-30s.csv) | a finished 5-shot product launch (30s) |
| [`examples/product-launch-30s.md`](examples/product-launch-30s.md) | the same plan, read as a document |
| [`examples/short-drama-90s.csv`](examples/short-drama-90s.csv) | a finished 6-shot short drama scene (90s) |
| [`examples/short-drama-90s.md`](examples/short-drama-90s.md) | the same plan, read as a document |

## Columns

| Column | Why it exists |
| --- | --- |
| `shot_id` | stable id — render files, notes and re-edits all key off it |
| `duration_s` | the length you want, not the length you got; keeps the cut honest |
| `shot_size` | ECU / CU / MCU / MS / WS — fixes framing before any words are written |
| `camera_move` | one move per shot; two moves in one cell is two shots |
| `subject` | what the frame is about, in a noun phrase |
| `action` | what changes during the shot — a shot with no action is a still |
| `lighting` | direction, quality, colour; the three things models invent if you skip them |
| `lens` | focal length + aperture, in the numbers the prompt will use |
| `prompt` | the composed prompt, ready to paste |
| `audio` | what you will hear; even if you add it later, write it now |
| `notes` | continuity, focus pulls, what to fix if the render fails |

## How to use it

1. Copy `shot-list-template.csv` and delete the example rows.
2. Fill `shot_size`, `camera_move`, `lighting` and `lens` first. These four decide what the model
   can invent, and they are the cheapest columns to get right.
3. Write `action` as a change over time: "she looks up", not "she is looking".
4. Compose `prompt` from the row in sentence order: subject and action, then framing, then
   lighting, then lens, then motion, then texture.
5. Render one shot at a time. Log the result in `notes` — a failed render is only useful if the
   reason is written down.
6. When a shot is approved, do not edit its row. Add a new row with `_v2` in the id so the history
   survives.

## Reading a finished example

[`examples/product-launch-30s.csv`](examples/product-launch-30s.csv) has five shots, 18 seconds of
picture in a 30-second slot — the rest is a title card and silence. That gap is deliberate: a
launch video that is shot-for-shot full of AI motion has nowhere to land.

[`examples/short-drama-90s.csv`](examples/short-drama-90s.csv) has six shots and ends on the room
rather than the face, which is the cheapest way to make a short scene feel like it continues after
the cut.

## A note on prompts

The prompt column is written for any text-to-video model that takes a natural-language shot
description; the wording here follows the five-part structure used by
[Wan 3.0](https://wan-3.io/) (subject → framing → light → lens → motion), which is what the
example prompts were rendered with.

## Licence

MIT.
