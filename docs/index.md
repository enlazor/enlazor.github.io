---
title: Enlazor — Smart URL Opener for macOS
description: Enlazor routes each link to the appropriate browser according to your rules. Configurable via JSON or from a simple UI. macOS 13+.
lang: en
image: /assets/images/og-image.png
permalink: /
---

<div align="center" style="margin-top:1rem;margin-bottom:2rem;">
  <img
    src="{{ '/assets/images/logo.png' | relative_url }}"
    alt="Enlazor logo"
    style="width:140px; height:auto; object-fit:contain;"
    decoding="async"
  />
  <p style="font-size:1.15rem;margin:0.2rem 0 1rem;opacity:.9;">
    One browser to route them all
  </p>

  <!-- Change the href to the real App Store link. -->
  <p>
    <a href="https://apps.apple.com/us/app/enlazor-link-router/id6754017771" class="btn btn-primary" style="padding:.6rem 1rem;border-radius:.6rem;">
      Get it on the Mac App Store
    </a>
  </p>
  <p style="font-size:.9rem;opacity:.75;margin-top:.5rem;">
    Free • macOS 13 or later • Swift &amp; SwiftUI • No data collection
  </p>
</div>

## What is Enlazor?

**Enlazor is a smart URL opener for macOS**. Set it as your default browser and define simple rules so every link opens in the most suitable browser (or profile).

Examples:
- Work domains → Chrome (work profile)
- Media and personal browsing → Safari
- Dev tools or local hosts → Firefox

## How it works (in 10 seconds)

1. Enlazor registers as your system default browser (HTTP/HTTPS).
2. When any app opens a link, Enlazor checks your rules locally.
3. It forwards the URL to the matching browser; otherwise uses your fallback.

## Key features

- 🧠 **Rule-based routing** by domain or pattern  
- 🧩 **UI or JSON** — configure it your way  
- ⚡️ **Zero overhead**: instant open, no windows if the app was closed  
- 🔒 **Privacy-first**: no data collection, on-device only  
- 🛠️ **Native**: Swift + SwiftUI, macOS 13+

## Quick start

1. **Set Enlazor as default browser**  
   `System Settings → Desktop & Dock → Default web browser → Enlazor`
2. **Pick a fallback browser** in Enlazor.
3. **Add rules** in the UI (top-to-bottom evaluation).

Prefer JSON?

`~/Library/Containers/com.enlazor.Enlazor/Data/Library/Application Support/Enlazor/config.json`

Example:

```json
{
  "defaultBrowserBundleID": "com.apple.Safari",
  "rules": [
    { "browserBundleID": "com.google.Chrome", "pattern": "youtube.com" },
    { "browserBundleID": "org.mozilla.firefox", "pattern": "localhost" }
  ]
}
```

> The first matching rule wins. If none matches, `defaultBrowserBundleID` is used.

## Support & docs
* 📄 [Privacy Policy](privacy.md)
* 🛟 [Support](support.md)
* ⚖️ [Website Terms of Use](terms-website.md)

---
<div style="font-size:.9rem;opacity:.7;"> © {{ site.time | date: "%Y" }} Julian Vilas Diaz. Enlazor is distributed via the Mac App Store under Apple’s Standard EULA. </div>
