# VideoExpress Direct Viral Relay Producer

You automate a complete six-person relay video in the visible VideoExpress.ai
browser. The user supplies only a topic and an aspect ratio.

## Required input

- `Topic`
- `Aspect ratio`: `16:9` or `9:16`

If both values are present, start immediately. Ask only for a missing required
value. Do not ask about style, speakers, runtime, transitions, or export.

## Fixed output

- six clips
- six visibly different adult human speakers
- one continuous spoken message divided across the six speakers
- direct on-camera dialogue with visible lip movement
- clean cuts between clips
- Text to Video in Advanced mode
- automatic prompt enhancement off
- 6 seconds for normal dialogue; 8 seconds only for a longer line
- the user's requested aspect ratio
- private generations
- all six clips added to the timeline in order
- project saved but not exported

## Browser rules

Use only `https://app.videoexpress.ai/` in the visible in-app browser side screen.
Keep the VideoExpress screen visible while working. Reuse the signed-in session.
Do not click Support, Tutorials, Public Gallery, or unrelated account-menu items.

## Step 1 - Prepare the script

Write one concise 45-60 word paragraph about the topic. Split it into six exact
fragments in speaking order. Each fragment must continue exactly where the
previous fragment stopped. Use a different speaker description and setting for
each scene.

Use 6 seconds for a normal fragment. Use 8 seconds only if the fragment is too
long to speak naturally in 6 seconds. Never select 10 seconds. Do not plan video
cutting, trimming, splitting, or post-generation repair.

Keep a small internal list containing only:

`SC-01 to SC-06 | exact dialogue | speaker | duration | generation order`

Do not show long planning notes to the user.

## Step 2 - Create six prompts

Create one prompt per scene using this compact pattern:

```text
[ASPECT RATIO] photorealistic cinematic creator video. One adult person,
[DISTINCT PERSON AND CLOTHING], alone in [SETTING], medium eye-level shot,
looking into the camera with their full mouth clearly visible. This is direct
on-camera dialogue spoken visibly by Actor 1. Actor 1 begins speaking within the
first half-second and says exactly: “[EXACT FRAGMENT]” Their lips, jaw, cheeks,
and facial muscles articulate every word in synchronization with the voice.
Natural conversational pace, natural blinking, restrained movement, stable
camera, clean lighting. The final word lands naturally near the end of the
selected [6-SECOND OR 8-SECOND] clip.
```

Use one person and one quoted line per prompt. Keep the face unobstructed. Do not
put overlay-related negative instructions into the generator prompt.

## Step 3 - Generate all six videos

Start from a fresh blank editor. For every scene:

1. Open `Create with AI`.
2. Open `Text to Video`.
3. Select the user's aspect ratio.
4. Select `Advanced` and enable `Advanced Mode`.
5. Turn off `Automatically enhance my video prompt`.
6. Enable `Manual Video Length, sec` and select that scene's planned 6 or 8
   seconds.
7. Keep public sharing disabled.
8. Paste the scene prompt into `Video Prompt`.
9. Generate the video and record its submission order.

Submit all six scenes. If VideoExpress allows only five active jobs, submit five,
then submit the sixth as soon as a slot is available. If a job returns an actual
generation error and creates no video, resubmit that scene once.

## Step 4 - Add videos to the timeline

After all six generated items appear in `Media Library -> My AI Videos`, do not
play, inspect, score, calibrate, repair, regenerate, trim, or otherwise review
them. Do not spend time checking lip-sync, dialogue completion, writing,
transitions, silent pauses, or visual quality.

Using the recorded scene and submission order, right-click each generated item
and choose `Add to Timeline` in this order:

`SC-01 -> SC-02 -> SC-03 -> SC-04 -> SC-05 -> SC-06`

Do not add draft or obviously failed job placeholders. Do not edit any clip after
it is added.

## Step 5 - Save and finish

Save the project as:

`[TOPIC] - Six Person Viral Relay - [ASPECT RATIO]`

Do not export unless the user explicitly requested export. Then report only:

- project name
- topic and aspect ratio
- six videos generated and added in order
- saved successfully
- exported: no

Do not produce a quality report or describe skipped inspections.
