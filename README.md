# Podcast Media Pipeline

Podcast Media Pipeline is a skills-only Codex plugin for moving one podcast episode through audio and episode-cover production, mandatory listening and visual approval, long-form video, short-form clips, media QA, upload preview, and scheduled publishing.

The central rule is deliberate: **Codex must not start video production until the creator confirms they listened to and approved the exported podcast master and visually approved the exact episode cover.** Uploading and scheduling require another exact approval of the release manifest.

## What is included

- A reusable `produce-and-publish` skill.
- Project-level configuration for brand, media, and schedule standards.
- Audio, long-video, and short-video QA checklists.
- A configurable episode-cover formula, visual QA checklist, and approval record.
- Safe upload and scheduling instructions.
- An episode record template for approvals and verification.
- A repository marketplace file for Codex installation.

This package contains workflow instructions and templates. It does not bundle FFmpeg, editing software, platform credentials, or an upload service. Codex adapts to the tools available in each user's environment.

## Install from GitHub

Add the public GitHub repository as a Codex marketplace source:

```bash
codex plugin marketplace add ii101iiii87/podcast-media-pipeline --ref main
codex plugin add podcast-media-pipeline@podcast-media-tools
```

Restart the ChatGPT desktop app, start a new Codex task, and invoke:

```text
Use $podcast-media-pipeline:produce-and-publish to prepare this episode.
```

## Install from a downloaded ZIP

1. Extract the ZIP to a stable local folder.
2. Add the extracted repository root as a marketplace:

```bash
codex plugin marketplace add /absolute/path/to/podcast-media-pipeline-public
codex plugin add podcast-media-pipeline@podcast-media-tools
```

3. Restart the ChatGPT desktop app and start a new Codex task.

## Configure a project

Copy this file into the podcast project root:

```text
plugins/podcast-media-pipeline/skills/produce-and-publish/assets/podcast-pipeline.example.yaml
```

Rename it to `podcast-pipeline.yaml`, then customize paths, brand rules, media targets, platforms, and release time zone. Do not put passwords, cookies, tokens, or MFA recovery codes in the file.

Example requests:

- "Prepare the podcast master and episode cover for episode 12, then stop for both approvals."
- "I listened to the exported master and visually approve the displayed episode cover. Create one long video and three shorts."
- "Preview the YouTube and podcast-host release manifest for next Friday; do not upload yet."
- "Upload and schedule the exact release manifest I just approved, then verify it."

## Public distribution

The simplest public distribution is a public GitHub repository with this file tree and tagged Releases. Codex users can add the repository as a marketplace source using the command above.

For inclusion in the official Plugins Directory, submit it as a **Skills only** plugin through the OpenAI plugin submission portal. The publisher must provide a verified developer or business identity, public listing and policy URLs, five positive tests, three negative tests, and the final skill bundle.

See [SUBMISSION.md](SUBMISSION.md) for a prepared checklist and test cases.

## License

MIT. See [LICENSE](LICENSE).
