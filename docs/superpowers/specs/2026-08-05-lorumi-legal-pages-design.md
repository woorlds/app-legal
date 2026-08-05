# Lorumi Legal and Support Pages Design

## Goal

Add public privacy-policy and app-support pages for Lorumi to the existing
`app-legal` GitHub Pages site. Preserve Putly's directory structure, HTML
layout, shared stylesheet, navigation pattern, and English-language tone while
making the content accurately describe Lorumi.

## Pages and Navigation

- Add `lorumi/privacy/index.html`.
- Add `lorumi/support/index.html`.
- Add Lorumi links to the root `index.html` app list.
- Add both public URLs to `README.md`.
- Reuse `shared/style.css` without modification.

## Privacy Policy Content

The policy will explain that Lorumi handles learner-written answers, saved
review state, voice recordings, raw/edited/confirmed transcripts, and generated
practice feedback. It will distinguish microphone capture, on-device Korean
speech transcription, and AI feedback generated with Apple's on-device
Foundation Models framework.

The policy will state that the reviewed implementation has no Lorumi account,
advertising or analytics SDK, developer-operated data server, or sale of user
data. Practice data is stored locally, protected by iOS file protection, and
excluded from device backup. Users can delete recordings, transcripts, and
feedback individually or delete all practice data in the app. Deleting the app
also removes its local container.

The page will describe Apple platform services as dependencies without claiming
that Woorlds controls Apple's separate platform-level processing. AI feedback
will be identified as reference-only practice assistance, not an official
assessment or guaranteed result.

## Support Page Content

The support page will retain Putly's contact and response-time format and add
Lorumi-specific guidance for:

- microphone permission and recording;
- saved recording playback;
- Korean transcription availability and installed language assets;
- Apple Intelligence and supported-device requirements for AI feedback;
- individual and complete practice-data deletion; and
- access to Lorumi's privacy policy.

The contact address remains `woorlds@gmail.com`.

## Verification

Verify that all four new links in the root page and README resolve to the two
new files, titles and app names consistently use `Lorumi`, relative stylesheet
paths match existing pages, external links use HTTPS, and the working tree does
not include unrelated changes.
