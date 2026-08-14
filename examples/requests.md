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

## Expected variable duration

Codex does not force every clip to six seconds. It calculates and sets a separate
manual duration for each fragment:

`max(5, ceil(spoken word count / 2.4) + 1)`

If a line is cut off, Codex adds one second only to that scene. If a ten-second
clip finishes speaking early, Codex keeps the good dialogue and trims the silent
tail on the timeline, leaving only 0.4-0.7 seconds after the final word.
