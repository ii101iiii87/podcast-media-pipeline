# Publishing workflow

Uploading, scheduling, or publishing changes external state. Preview first, execute only after exact approval, and verify afterward.

## Release manifest

For every platform, show:

- account, channel, show, or workspace
- media file and thumbnail path
- title and description
- tags, hashtags, category, playlist, season, and episode number when applicable
- captions, chapters, transcript, links, and attribution
- audience, sponsorship, altered-content, rights, and other required declarations
- visibility state
- publication date, local time, and IANA time zone
- whether the action is upload-only, save-as-draft, schedule, or publish-now

Do not hide platform-specific differences behind one summary. The user must be able to see exactly what each service will receive.

## Approval boundary

Approval applies only to the displayed manifest and matching file identities. Re-preview when a media file, thumbnail, platform, account, title, description, visibility, date, time, time zone, or declaration changes.

Never treat these as release approval:

- approval of the podcast audio alone
- approval of a prior episode
- a general statement such as "publish these sometime"
- a file already present in an upload folder

## Execution

1. Confirm the authenticated destination before uploading.
2. Upload the approved media and supporting assets.
3. Allow the platform to finish required processing and validation.
4. Apply the approved metadata and schedule.
5. Do not bypass CAPTCHA, MFA, rights checks, or terms prompts.
6. Save only non-sensitive platform identifiers and URLs in the episode record.

## Verification

After scheduling or publishing, re-open the item and verify:

- correct media and thumbnail
- correct account and visibility
- successful processing with no platform error
- displayed date, time, and time zone
- captions, chapters, metadata, and declarations
- public or preview URL when available

If the platform cannot be verified, report the action as unverified rather than complete.
