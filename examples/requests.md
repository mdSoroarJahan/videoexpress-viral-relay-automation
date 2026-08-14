# Example user requests

Both required values supplied:

```text
Topic: Why tree shadows become crescents during an eclipse
Aspect ratio: 16:9
```

```text
Topic: Three habits that make a phone battery drain faster
Aspect ratio: 9:16
```

Codex chooses a current topic:

```text
Topic: Choose a safe viral science topic today
Aspect ratio: 9:16
```

Missing input behavior:

```text
Topic: Why cats slow-blink at people
```

Expected response: ask only for the aspect ratio.

## Expected automatic recovery

If a generated speaker completes the dialogue but performs a transition prop
action differently than planned—for example, lifting a phone instead of turning
it face-down—Codex keeps the usable speaking clip, uses a clean cut to the next
speaker, and completes the six-scene project. It must not stop production or
leave the timeline empty for a transition-only mismatch.

## Expected duration selection

Codex uses a 6-second manual duration for normal dialogue. If a line is too long
to finish naturally in 6 seconds, Codex uses 8 seconds for that scene.

Codex never selects 10 seconds and never cuts, trims, splits, or shortens an
accepted clip. If a generated clip has a long pause after the dialogue, Codex
regenerates that scene at the same 6- or 8-second duration with immediate,
continuous natural delivery.
