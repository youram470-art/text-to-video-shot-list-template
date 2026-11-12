# Example — 30 second product launch

Five shots, 18 seconds of picture in a 30-second slot. The remaining time is a title card and a
second of silence, because a launch video with no gap reads as an ad that never breathes.

Source data: [`product-launch-30s.csv`](product-launch-30s.csv).

| # | Shot | Len | Move | Light | Lens |
| --- | --- | --- | --- | --- | --- |
| S01 | ECU lid unscrewing | 3s | static | hard key, right | 100mm f/8 |
| S02 | MS orbit on the bottle | 4s | orbit 45° | soft box overhead | 85mm f/8 |
| S03 | MCU hand lifting it | 3s | static | warm practical, left | 50mm f/2.8 |
| S04 | CU liquid pour | 4s | slow tilt down | backlit, black | 100mm f/5.6 @120fps |
| S05 | WS pull back from the table | 4s | slow pull back | window light, long shadows | 35mm f/5.6 |

## The build

**S01 opens on texture, not the product.** An extreme close-up of the lid turning is the cheapest
way to say "this is a physical object". Starting on the whole bottle gives the viewer nothing to
look at for the first second.

**S02 answers the question S01 raises.** The orbit at constant radius shows the silhouette without
asking the viewer to track anything. Constant speed and no vertical drift matter here — an orbit
that also rises will read as a handheld mistake.

**S03 puts a hand on it.** Scale is the thing a photo cannot settle, so the hand is doing a job,
not holding a prop.

**S04 is the only shot with real motion.** It is placed after three still-ish shots so the cut has
somewhere to go up to. Rendered at 120 fps and played at quarter speed, the pour holds for four
seconds from about one second of real action.

**S05 pulls back and stops.** Ending wide with the object small in frame gives the editor a place
to put a title. Never end a product video on a close-up; there is no room for type.

## Continuity notes

- Same table, same slab, same warm lamp across S02–S05.
- The bottle must stay matte. If a render gives it gloss, the material drifts and the shots stop
  cutting together.
- Keep the liquid darker than the bottle; identical values make S04 read as a blur.

## Licence

MIT.
