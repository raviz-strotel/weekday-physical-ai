# Weekday Physical AI: frontend handoff

Version: v12, 23 October 2026
Source commit: 42a72e352faf8d5cfe4cbe0d393b5f927bd86e3a
Live: https://weekday-physical-ai-cad-lab.raviz-crossinghurdle.chatgpt.site/

## Run locally
Unzip the source package. From its root run `python3 -m http.server 8000 --directory dist`, then visit http://localhost:8000/ and http://localhost:8000/cad/ . Use an HTTP server rather than opening files directly, because examples load JSON/media with fetch. No npm installation or build is required.

## Files and routes
- `dist/index.html`: physical AI overview.
- `dist/cad/index.html`: CAD example/detail page.
- `dist/style.css`: shared Weekday-inspired styling.
- `dist/app.js`: CAD/robot/inspection interactions, package explorer and scheduler preview.
- `dist/previews.js`: reference artifact previews.
- `dist/data/`: actual reference files, images/video, metadata, licenses and attribution.

## Activate Calendly
Set `CALENDLY_URL` in `dist/app.js` to the approved founders' Calendly event URL. Both navigation and closing CTAs then navigate directly to that URL. Until configured, clicking opens an accessible notice that scheduling is not live. Configure actual weekly availability, meeting duration, timezone, buffers and routing in Calendly itself; no availability is configured or claimed here. No calendar account or backend has been created. No personal data is collected by the preview.

## Hosting
Deploy the contents of `dist/` as the web root on a static host. Preserve `/cad/` directory routing. Asset links are root-relative, so deployment under a subdirectory requires adjusting the base paths. Google Fonts and the official Weekday wordmark are external dependencies; assess font/asset hosting for production.

## Data and claims
This is a concept frontend, not evidence that Weekday collected or owns the public examples. Keep the included provenance/license notices. BridgeData V2, VisA and the authored CadQuery demonstrator have different source terms and limitations, documented beside each specimen and in `dist/data/`. CAD validity checks are not manufacturing/safety certification. Public sample display does not imply white-label rights to future purchased datasets. Replace public examples only after inspecting actual licensed files and their permissions.

## Before production launch
- Supply and test the approved Calendly URL and configured availability.
- Review actual company service claims and approved brand assets.
- Test desktop and mobile layouts, keyboard navigation, all downloads and media loads on the production host.
- Decide analytics/privacy requirements separately; none is introduced by this update.
- Review public repository contents before committing future changes. Never commit secrets, private client data or enquiry records.

No credentials, Git history, personal enquiry records or backend prototype are included.
