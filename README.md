# Liwu — Releases

Signed & notarized release artifacts for **[Liwu](https://liwu.app)**, a Mac battery-care app.

This repository holds **build artifacts only**. Liwu's source is closed; see
[liwu.app](https://liwu.app) for the product, and the
[Releases](https://github.com/urfreespace/liwu-releases/releases) tab for downloads.

## Why a separate repository

Liwu's source repository is private, and **release assets on a private repository cannot be
downloaded anonymously**. This public repository exists solely so that download links work
for everyone — and so that binaries never enter the source repository's git history.

## Updates

Liwu updates itself via [Sparkle](https://sparkle-project.org). The appcast feed lives at
<https://liwu.app/appcast.xml>. Every build is signed with a Developer ID certificate,
notarized by Apple, and stapled.

---

© 2026 Li Li. All rights reserved. "Liwu" and the Liwu icon are trademarks of Li Li.
