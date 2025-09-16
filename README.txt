VOICE BLAST — Local or GitHub Pages (no Netlify)
Updated: 2025-09-16

Files:
- index.html  — recorder page that POSTs audio to your Make webhook.

The Make webhook is already inserted:
(Web hook here)

SECURITY: Change SECRET in index.html, then add a Make Filter right after the webhook:
  If {secret} equals your chosen string → continue, else stop.

A) RUN LOCALLY (no hosting)
1) Download and unzip this folder.
2) Start a local server:
   - macOS:   python3 -m http.server 8000
   - Windows: py -m http.server 8000
3) Visit http://localhost:8000
4) Allow mic → Record → Stop → Send.
5) In Make, click 'Run once' on your scenario to see the webhook fire.

B) PUBLISH ON GITHUB PAGES (free)
1) Create a GitHub account (if needed).
2) New public repo named: voice-blast
3) Upload index.html at the repo root.
4) Settings → Pages → Source: Deploy from a branch; Branch: main; Folder: /(root) → Save.
5) Open https://YOUR_USERNAME.github.io/voice-blast/
