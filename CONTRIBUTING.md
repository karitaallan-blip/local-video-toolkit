# Contributing to Local video toolkit

Thank you for helping improve ClipTrace's public tools. Small contributions are valuable; you do not need access to the private ClipTrace application.

## Project scope

This repository is a standalone MIT-licensed browser tool. The hosted ClipTrace service was restored to its prior application on September 21, 2026. These public tools remain available independently; the earlier integrated toolkit experiment is preserved in a private archive. This repository does not contain the proprietary tracing engine, and contributing here does not guarantee a change to the hosted service.

Local file selection is welcome: it reads a video on the user's device. Uploading that video to a server is outside this project's scope.

## Welcome contributions

- Reproducible bug fixes and clearer error handling.
- Accessibility, documentation and usability improvements.
- Mobile layout and browser compatibility fixes.
- Small synthetic test cases and clearly explained limitations.
- Local, optional visual overlays that keep the original pixels and the offline network boundary intact.

Do not add accounts, analytics, tracking, server uploads or external API calls. Keep runtime code dependency-free using plain HTML, CSS, JavaScript and native browser APIs. Discuss new dependencies, large refactors and changed scope in an Issue before starting. Do not add identity, deepfake or authenticity verdicts unsupported by these tools.

## Before opening a pull request

1. Read the README and check existing Issues and pull requests for related work. For a substantial change, open an Issue with the problem, proposed behavior and tradeoffs first. Small fixes can go straight to a pull request.
2. Fork this repository and create a focused branch, for example `git checkout -b fix/clear-file-error`.
3. Make the smallest useful change. Include a regression test when behavior changes and update relevant documentation.
4. Run the checks below. Record the commands, results and any checks you could not run. Do not claim untested browsers or platforms work.
5. Open a pull request against `main` with the problem, solution, linked Issue (if any), test evidence and limitations. Use synthetic screenshots when a visual change needs explanation.
6. Respond to review and keep follow-up commits focused. A maintainer reviews and merges accepted changes; opening a pull request does not promise acceptance or a response deadline.

## Checks

Open `index.html` directly in a modern browser; no installation or backend is required. Test with synthetic media you created:

- A normal H.264 MP4 (a four-second 320 × 180 clip is a useful baseline).
- A very short video, an empty file and malformed or unsupported input.
- Eight visible previews for the normal clip, JPEG download, JSON export and print preview/PDF.
- Night-vision and false-color preview styles on synthetic frames; confirm the source JPEG and exported JSON remain unchanged and a WebGL failure reports clearly.
- Cancellation, then selecting another file; a rejected file must not leave the tool stuck.
- Desktop and approximately 390px mobile widths; keyboard operation, focus and readable errors.
- Offline operation after download, no application network requests and no unexpected console errors.

Do not add map tiles, Cesium CDN scripts, OCR model downloads or weather requests to this offline single-file tool without a separately reviewed change to its public privacy and network contract.

Report browser and operating-system versions. Codec support and seek precision vary; requested seek positions are not guaranteed decoded frame timestamps. Include a generator command rather than a large binary fixture where possible.

## Privacy, security and rights

Never include real user media, private videos, personal data, credentials, production logs or proprietary ClipTrace code in Issues, commits, screenshots or pull requests. Review staged files and commit history before pushing; deleting a secret in a later commit does not remove it from history.

For a sensitive vulnerability, use GitHub's private vulnerability reporting option if available. Otherwise contact the maintainer privately through the contact route on [ClipTrace](https://tracemyclip.com), asking for a secure reporting channel before sending details. Do not post exploit details or sensitive samples in a public Issue.

Submit only work you have the right to contribute. Contributions to this repository are under its existing [MIT license](LICENSE); retain copyright and permission notices. Identify any third-party material and its license for review. These contribution rules describe what maintainers accept upstream; they do not add restrictions to the MIT license.

## Questions and collaboration

Open a GitHub Issue for a nonsensitive question, bug or proposal. Use Discussions only if the repository has that feature enabled. Be respectful, explain reproducible behavior and distinguish measured results from assumptions. Documentation, testing and constructive review are welcome even if you cannot contribute code. Volunteer contributions do not imply payment, employment or equity.
