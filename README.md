# Local video toolkit

Open `index.html` in a modern browser. No installation, account, backend, API keys, analytics or upload. You can disconnect from the internet after downloading the file.

Features: eight evenly spaced JPEG previews, browser-reported duration/dimensions, JSON observation export, and browser print-to-PDF. It does not search for sources, detect AI generation, identify people or verify authenticity. Requested seek positions are not guaranteed exact decoded frame timestamps.

Limits: 100 MiB, five minutes, 3840 × 2160 pixel count, one video at a time. Codec support depends on the browser and operating system. Try H.264 MP4 if a file cannot be decoded. Mobile devices may still reject large videos under these limits.

There is no daily/monthly quota: computation stays on the user's device and there is no shared compute service to exhaust. Client-side quotas would be bypassable and would offer no server-cost protection. The CSP blocks fetch/XHR and other network resources.

## Verify a change

Use a synthetic four-second 320 × 180 MP4. Check eight visible previews; download and inspect the JSON; download a JPEG; print to PDF; test cancellation; test an empty/malformed file; verify at 390px and desktop widths; confirm no network requests or JavaScript errors. Do not contribute private media. The release candidate passed automated Chromium desktop/mobile sampling, JSON export, malformed-file recovery and zero-network checks in the source project.

## Contribute

Small accessibility improvements, browser compatibility fixes and synthetic codec fixtures are welcome. Keep the page dependency-free. Do not add telemetry, uploads, API calls or authenticity scores. Explain your change and the browsers you tested.

## Publish

Licensed under MIT; see `LICENSE`. This toolkit was authored for ClipTrace using native browser APIs and includes no copied third-party implementation or private tracing engine. Publish this directory alone with a clean history. No license to the private ClipTrace engine is implied. For a hosted demo, publish this static file only; do not deploy the application backend. A hosted demo is optional: direct HTML downloads work offline.
