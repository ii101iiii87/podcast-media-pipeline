---
name: produce-and-publish
description: Produce and publish a podcast episode as approved audio, episode cover art, long-form video, and short-form clips with explicit quality and release gates. Use when Codex is asked to prepare podcast audio or episode artwork, generate podcast videos or social clips, review media deliverables, upload an episode, or schedule publication across podcast and video platforms.
---

# Produce and Publish Podcast Media

Run the episode as a gated pipeline. Adapt tools and formats to the project configuration, but never weaken an approval gate.

## Non-negotiable gates

1. Treat the podcast package as two required deliverables: the exported audio master and episode-specific cover art.
2. Do not start long-form or short-form video production until the user has listened to and approved the audio master, inspected and approved the episode cover, and identified the exact approved files.
3. Treat automated audio and image checks as evidence, not human approval.
4. Do not upload or schedule anything until all requested media passes QA and the user approves the exact release plan.
5. Preview public titles, descriptions, cover art, thumbnails, platforms, visibility, dates, times, and time zones before performing external writes.
6. Never overwrite source media. Preserve reproducible masters and record the inputs used.

## Start the episode

1. Look for `podcast-pipeline.yaml` in the project root.
2. If it is absent, copy `assets/podcast-pipeline.example.yaml` into the project as `podcast-pipeline.yaml`, then replace example values using user instructions and discovered project files. Ask only for settings that materially affect the deliverables.
3. Read [project-configuration.md](references/project-configuration.md) when creating or interpreting the configuration.
4. Inventory source audio, scripts, images, music, fonts, logos, prior episode examples, publishing targets, and available tools.
5. Report missing or ambiguous inputs before beginning an expensive render.

## Run the pipeline

### 1. Build and inspect the podcast package

- Preserve the raw recording and create a separate editable intermediate.
- Apply only the cleanup, edit, mix, loudness, intro, outro, chapter, and metadata rules defined by the project.
- Create episode-specific cover art using [episode-cover.md](references/episode-cover.md) and the configured brand formula. Do not silently reuse generic show art when an episode cover is required.
- Export the designated listening master.
- Perform the audio and episode-cover checks in [quality-gates.md](references/quality-gates.md).
- Present the master path, duration, cover path and preview, technical findings, and any known compromises.
- Stop and request explicit confirmation that the user listened to the master and visually approved the episode cover.

Accept the gate only when the user clearly confirms that they listened to the exported master and that it is acceptable, and separately confirms that the displayed episode cover is acceptable. Record both exact file identities. Audio changes invalidate audio approval; cover or visible metadata changes invalidate cover approval.

### 2. Build long-form and short-form video

Proceed only after both podcast-package approvals pass.

- Create the long-form video according to the configured aspect ratio, resolution, frame rate, visual system, captions, chapters, and audio-master rules.
- Select short clips for a clear hook and a complete idea. Do not manufacture misleading context.
- Create platform variants only when their specifications differ.
- Use the approved podcast master as the audio source unless the project explicitly defines another mix.
- Perform the video checks in [quality-gates.md](references/quality-gates.md).
- Present a deliverables table with file paths, durations, dimensions, and QA status.
- Stop for approval when the user asked to review videos before upload or when any creative choice remains unresolved.

### 3. Preview and perform publishing

- Read [publishing.md](references/publishing.md) before any upload or scheduling action.
- Build one release manifest containing every platform, audio or video asset, approved episode cover, thumbnail, title, description, tags, visibility, date, local time, and time zone.
- Show the release manifest to the user and request approval of that exact plan.
- Use an available authenticated connector, browser, or platform tool only after approval.
- Pause for login, CAPTCHA, MFA, channel selection, rights declarations, or changed platform terms that require the user.
- After the write, verify the remote asset, visibility, processing state, and scheduled time. Report platform URLs or identifiers when available.

## Handle partial requests

- If asked only to prepare the podcast, deliver the audio master, episode cover, and QA report, then stop for both approvals.
- If given an already approved podcast master, confirm which exact audio file and episode-cover file were approved and record both pieces of evidence before creating video.
- If asked only to upload existing media, validate that the files and release manifest satisfy the relevant gates. Do not infer missing approval from the existence of files.
- If the environment lacks a required production or upload tool, deliver the completed plan and exact blocker without pretending the external action occurred.

## Finish with an episode record

Copy `assets/episode-record.example.md` as the episode record and fill in:

- source and master file paths
- checksum or other stable file identity when available
- episode-cover source, output, formula version, and QA result
- audio listening and cover-art approval statements and times
- produced long-form and short-form deliverables
- QA findings and accepted exceptions
- approved release manifest
- upload and scheduling verification

Keep credentials, cookies, private tokens, and recovery codes out of all records.
