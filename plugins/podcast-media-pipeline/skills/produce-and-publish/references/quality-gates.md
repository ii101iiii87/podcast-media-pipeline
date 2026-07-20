# Quality gates

Use checks appropriate to the configured tools and formats. Record commands, reports, or visual inspections when possible.

## Podcast master gate

Confirm:

- the expected episode and source takes were used
- speech is intelligible and edits do not cut words or create obvious discontinuities
- long unintended silence, clipping, clicks, hum, and abrupt transitions were addressed
- intro, outro, music, ads, and chapter positions match the project rules
- duration, sample rate, channels, codec, loudness, true peak, and metadata match the configured targets
- music and third-party assets have usable license evidence
- the exported master plays from beginning to end

Then give the user the exact listening-master path. The only passing condition for the audio half of the human gate is explicit confirmation that the user listened to that master and accepts it.

## Episode cover gate

Confirm:

- the cover is specific to the episode unless the configuration explicitly permits reusable show art
- the episode title, series, episode number, creator or brand, and content label match the approved metadata
- the source artwork and fonts have usable license evidence
- canvas size, aspect ratio, format, color mode, file size, and safe area match each target platform
- the title hierarchy remains readable at the configured small-preview size
- text, faces, logos, and focal subjects are not unintentionally cropped
- contrast, spelling, punctuation, branding, and content representation are accurate
- derived platform files came from the approved cover master without stretching or unapproved redesign
- the exported files decode correctly and the exact paths are recorded

Show the cover or a rendered preview to the user. The cover half of the human gate passes only after explicit visual approval of the exact file. A cover or visible-metadata change invalidates this approval.

## Long-form video gate

Confirm:

- the video uses the approved podcast master
- duration and audio sync are correct from start to finish
- resolution, aspect ratio, frame rate, codec, and audio stream match the configured target
- titles, names, logos, colors, typography, waveform, artwork, chapters, and captions are correct
- text stays readable and inside safe areas
- no missing frames, black gaps, frozen unintended sections, or corrupted output are visible
- the thumbnail represents the episode accurately and remains legible at small size
- representative frames from the beginning, middle, and end were inspected

## Short-form video gate

Confirm each clip separately:

- the hook arrives quickly and the clip presents a complete, non-misleading idea
- the in/out points do not clip speech
- captions match the spoken words and remain within platform-safe areas
- aspect ratio, resolution, duration, frame rate, codec, and audio level match the target
- branding does not obstruct faces, captions, or platform UI zones
- the final frame and call to action are intentional
- the entire clip was viewed with sound

## Failure behavior

- Do not mark a gate as passed when a required check was skipped.
- Separate warnings from failures and explain the practical impact.
- Re-run affected checks after every revision or re-encode.
- Invalidate downstream approval when the approved master or release asset changes.
- Keep audio approval and cover approval separate so an unrelated change invalidates only the affected half, while video production still requires both halves to be current.
