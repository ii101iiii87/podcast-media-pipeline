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

Then give the user the exact listening-master path and stop. The only passing condition for the human gate is explicit confirmation that the user listened to that master and accepts it.

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
