# Example — 90 second short drama scene

Six shots for a single scene in a laundromat. The scene ends on the room, not the face.

Source data: [`short-drama-90s.csv`](short-drama-90s.csv).

| # | Shot | Len | Move | What changes |
| --- | --- | --- | --- | --- |
| S01 | WS, empty laundromat | 4s | static | machines running, nobody there |
| S02 | MCU, she enters | 3s | handheld follow | she stops at a machine |
| S03 | ECU, hands | 3s | static | a folded letter comes out of a pocket |
| S04 | OTS, she reads | 4s | slow push in | her jaw tightens |
| S05 | MCU, her face | 3s | static | she looks up, blinks once |
| S06 | WS, crane up | 4s | slow crane | the room, the flickering light |

## The build

**S01 carries the whole scene.** Four seconds of a room with nobody in it tells the audience the
place is a routine, and that the character is late to it. If this shot is cut, S02 has to explain
the room and the entrance at once, and usually neither lands.

**S02 is handheld on purpose.** The only hand-held shot in the scene marks the entrance as an
interruption. Everything after it goes back to locked-off framing, which is what makes the
intrusion readable.

**S03 is where the prop arrives.** A letter in an extreme close-up, top-lit with hard falloff: the
object is lit separately from the room, so it feels handled rather than incidental.

**S04's push-in is one axis only.** No pan, no tilt. The focus pull to the face at the end of the
move is the acting beat, so the camera must not compete with it.

**S05 is a single blink.** One blink, one look up. Two blinks reads as a reaction shot; one blink
reads as a decision.

**S06 cranes up and leaves her in frame.** The room keeps running, the light flickers once, and the
scene does not resolve. This is the difference between a clip and a scene.

## Continuity notes

- Green fluorescents throughout; the sodium lamp outside stays visible in every wide.
- S02 and S04 must share the same machine in the same position, or the scene reads as two rooms.
- The letter is the only warm object in frame; do not let the render warm the room.
- Keep the flicker to S06. A flickering light earlier turns atmosphere into a horror cue.

## Licence

MIT.
