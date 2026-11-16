WEBTOAPP DEMO WEBSITE
=====================

Purpose
-------
A small, static sample website for testing your WebToApp scanner and Android
TWA build workflow. It is not a real e-commerce website.

Files
-----
index.html                 Homepage with viewport and manifest reference
manifest.webmanifest       PWA manifest (standalone, same-origin start URL)
icons/icon-192.png         192 x 192 PNG icon
icons/icon-512.png         512 x 512 PNG icon
service-worker.js          Basic app-shell cache / offline fallback

IMPORTANT: WebToApp's server-side checks require a publicly reachable HTTPS
website. Opening index.html locally or using http://127.0.0.1 will not pass
the production HTTPS check.

Quick deployment with Netlify
-----------------------------
1. Extract this ZIP.
2. Open https://app.netlify.com/drop in your browser.
3. Sign in if prompted.
4. Drag the extracted webtoapp-test-website folder (or its contents) onto
   the drop area.
5. Wait for deployment. Netlify will provide an HTTPS URL.
6. Open that URL once to confirm the demo page loads.
7. Paste the HTTPS URL into WebToApp and click "Check my website".

Expected WebToApp checks
------------------------
- Public HTTPS homepage
- Manifest linked from the HTML
- Valid JSON manifest
- App name and short name
- Same-origin start URL and scope
- PNG icons including a 512 x 512 icon with purpose "any"
- Standalone display mode
- Mobile viewport
- Service worker (optional in WebToApp's scanner)

If your scanner reports an issue, share the exact result before changing files.
