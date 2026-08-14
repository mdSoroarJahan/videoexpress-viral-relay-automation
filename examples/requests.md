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

Codex does not force every clip to six seconds. It first leaves Manual Video
Length disabled so VideoExpress can choose the duration from the dialogue. For
planning and truncation recovery it calculates:

`max(6, ceil(spoken word count / 2.2) + 2)`

If a line is cut off, Codex regenerates only that scene at the calculated manual
duration, adding another two seconds if the ending is still truncated.
