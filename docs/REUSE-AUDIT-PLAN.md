# LiveSync Video: Legacy Reuse Audit (2026-11-09)

This repository describes an earlier WordPress plugin combining livestream badge, embeddable live video and a video library. Treat its implementation as **unverified legacy code**, not as a clean or production-ready basis until it passes current project_frameworks WordPress security and release checklists.

## Proposed review
1. Inventory PHP/JS/CSS, current branch, bundled libraries, license, stored settings, OAuth/API credentials and update mechanism.
2. Audit nonce and user capability checks, settings sanitization, output escaping, REST/AJAX authorization, SSRF, data retention, cron behavior and API quota.
3. Verify compatibility with supported PHP/WordPress and cache/CDN settings.
4. Build isolated automated tests with mocked YouTube and Twitch responses, rate-limit and failure behavior.
5. Extract proven concepts or isolated components only after testing; otherwise reimplement narrowly.

## Target products
- HuiSocial Live Bar (first release, one-channel status bar)
- Hui Video Suite (later cached video gallery)
- Separate WordPress plugin repos and distribution from any optional Laravel marketing portal.

Do not automatically ship all LiveSync capabilities in one large plugin. Preserve history, license obligations and functional requirements.

[HuiSocial product plan](https://github.com/makingtheimpact/hui-social/blob/main/docs/PRODUCT-PLAN.md)
