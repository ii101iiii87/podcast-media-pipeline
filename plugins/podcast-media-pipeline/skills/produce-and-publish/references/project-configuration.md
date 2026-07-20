# Project configuration

Use `podcast-pipeline.yaml` as the project-specific source of truth. Keep creator-specific standards here instead of hard-coding them in the public skill.

## Resolution order

Resolve a setting in this order:

1. The user's current explicit instruction.
2. `podcast-pipeline.yaml`.
3. A clearly applicable existing project convention or approved prior episode.
4. The example configuration as a proposal, never as a hidden assumption.

Call out conflicts between these sources. Ask before changing an established brand, licensing, publishing, or approval rule.

## Required configuration areas

- Project identity: name, language, time zone, and paths.
- Source discovery: recordings, script, episode-specific hero art, show art, brand assets, fonts, licensed music, and prior examples.
- Audio: edit rules, intro/outro, loudness target, channel layout, sample rate, master format, metadata, and silence policy.
- Episode cover: required status, platform outputs, canvas sizes, safe areas, brand template, text hierarchy, source-art rules, small-preview check, output format, and approval evidence.
- Long-form video: aspect ratio, resolution, frame rate, visual layout, captions, chapters, thumbnail, and output format.
- Short-form video: clip count, duration range, aspect ratio, caption style, safe areas, branding, and platform variants.
- Publishing: platforms, channel or show identity, visibility, schedule, metadata templates, playlist or category, and disclosure requirements.
- Approval: the exact evidence required at the audio, video, and release gates.

## Safe configuration rules

- Store paths and creative standards, not passwords, cookies, access tokens, or recovery codes.
- Use relative paths when the project can remain portable.
- Record music and stock-asset license evidence, including where the source file came from.
- Treat schedule times as local to the configured IANA time zone unless a platform explicitly shows another zone.
- Leave unknown settings empty and surface them before production; do not invent channel identity or legal declarations.
- Distinguish generic show art from episode-specific cover art. Reuse show art only when the configuration explicitly allows it.
