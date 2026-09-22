# Local video toolkit

## Current position

As of September 22, 2026, this is an independent public tool maintained alongside [ClipTrace](https://tracemyclip.com), a worldwide hosted video investigation service. The hosted application was restored to its prior version on September 21; this standalone toolkit remains available. The earlier integrated toolkit experiment is preserved privately and is not the current hosted application. The proprietary ClipTrace tracing engine is not included or licensed by this repository.

Help is welcome with browser compatibility, accessibility, documentation and synthetic tests. See [CONTRIBUTING.md](CONTRIBUTING.md) for how to propose and verify a change. The companion [evidence-utils](https://github.com/karitaallan-blip/evidence-utils) repository provides local hashing and observation-report helpers.

Open `index.html` in a modern browser. No installation, account, backend, API keys, analytics or upload. You can disconnect from the internet after downloading the file.

Features: eight evenly spaced JPEG previews, browser-reported duration/dimensions, JSON observation export, and browser print-to-PDF. It does not search for sources, detect AI generation, identify people or verify authenticity. Requested seek positions are not guaranteed exact decoded frame timestamps.

Limits: 100 MiB, five minutes, 3840 × 2160 pixel count, one video at a time. Codec support depends on the browser and operating system. Try H.264 MP4 if a file cannot be decoded. Mobile devices may still reject large videos under these limits.

There is no daily/monthly quota: computation stays on the user's device and there is no shared compute service to exhaust. Client-side quotas would be bypassable and would offer no server-cost protection. The CSP blocks fetch/XHR and other network resources.

## Verify a change

Use a synthetic four-second 320 × 180 MP4. Check eight visible previews; download and inspect the JSON; download a JPEG; print to PDF; test cancellation; test an empty/malformed file; verify at 390px and desktop widths; confirm no network requests or JavaScript errors. Do not contribute private media. The release candidate passed automated Chromium desktop/mobile sampling, JSON export, malformed-file recovery and zero-network checks in the source project.

## Contribute

Read [CONTRIBUTING.md](CONTRIBUTING.md). Local file selection is supported; server uploads, telemetry, accounts and external API calls are outside this project's scope. Please use synthetic media and report the browsers you tested.

## Publish

Licensed under [MIT](LICENSE). Retain its copyright and permission notices when redistributing. The license covers the code and documentation in this repository; it does not license the separate private ClipTrace service or grant rights to third-party media you process. This is a public source release, not a promise of forensic accuracy or support response times.

For a hosted demo, publish this static file only. Direct HTML downloads work offline. Hosting providers can receive ordinary page-request metadata; the downloaded offline tool processes selected media on your device.
