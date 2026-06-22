# Privacy Policy — Cozylingo

_Last updated: June 21, 2026_

Cozylingo is a browser extension that explains the contextual meaning and
translation of a word or phrase you select — on web pages, in PDFs you open in
its built-in reader, and in images you capture on screen. This policy explains
exactly what data the extension handles and where it goes.

**Short version:** Cozylingo does not collect, track, or sell your data. It has
no analytics and no ads. The only information that leaves your device is the text
you explicitly look up, which is sent to Groq to generate the explanation.

---

## What data Cozylingo handles

**1. Your API key**
Your Groq API key is stored locally in your browser via `chrome.storage.sync`
and is used only by the extension's background service worker to authenticate
requests to Groq. It is never injected into web pages and never sent anywhere
except, as the standard `Authorization` header, to the API endpoint you have
configured (Groq by default).

> Note: `chrome.storage.sync` is your browser's built-in setting-sync mechanism.
> If you have Chrome Sync enabled, your settings — including the API key — may be
> synced by the browser across the Chrome profiles where you are signed in. This
> is handled by your browser, not by Cozylingo.

**2. Your settings**
Target language, result mode, interface language, and model are stored locally in
the same way. They never leave your device except as part of an API request you
trigger (e.g., the chosen model).

**3. Text you look up**
When you choose "Show meaning & translation," the extension sends the following
to your configured provider (Groq by default):

- the selected word or phrase,
- the surrounding sentence (capped at roughly 400 characters), and
- a page-language hint.

This is the minimum needed to produce a context-aware explanation. The full page,
document, or browsing activity is **not** sent.

**4. PDFs you open in the reader**
PDF files you open in Cozylingo's built-in reader are read and rendered
**entirely on your device** using the bundled PDF.js library. The file itself is
**never uploaded** anywhere. Only a selected word and its surrounding sentence
(as in #3) are sent for a lookup.

**5. Text in images (OCR)**
When you capture a region of the screen to read text inside an image (a photo,
screenshot, meme, or scanned page), that image is processed **entirely on your
device** using the bundled Tesseract.js engine (WebAssembly). The captured image
is **never uploaded** anywhere. As with everything else, only the word or phrase
you then select for a look-up — and its surrounding sentence (as in #3) — is sent
to your configured provider.

---

## Third-party services

To generate explanations, the look-up text described above is sent to **Groq**
(`api.groq.com`) by default. Groq's handling of that data is governed by its own
privacy policy: <https://groq.com/privacy-policy/>.

If you configure a different OpenAI-compatible provider, the same look-up text is
sent to that provider instead, under that provider's policy.

Cozylingo uses no other third-party services. The PDF.js library is bundled
locally and makes no network requests.

---

## What Cozylingo does NOT do

- No analytics, telemetry, or usage tracking.
- No advertising and no ad networks.
- No selling, renting, or sharing of personal data.
- No collection of browsing history, and no reading of page content beyond the
  text you explicitly select for a look-up.
- No remote code: all extension code, including PDF.js and the Tesseract.js OCR
  engine, ships in the package and runs locally.

---

## Data retention and deletion

Cozylingo stores no data on any server it controls — it has none. Your API key
and settings live only in your browser. To remove them, clear the fields in the
extension's options or uninstall the extension. Text sent to Groq (or another
provider) is subject to that provider's retention policy, linked above.

---

## Children

Cozylingo is a general-purpose study tool and is not directed at children under
13, and it does not knowingly collect personal information from them.

---

## Changes to this policy

If this policy changes, the "Last updated" date above will be revised and the new
version will accompany the corresponding release.

---

## Contact

Questions about this policy? Contact the developer at:
**<fraglinkpro@gmail.com>**
