# camroll-check

find the screenshots in your camera roll that you forgot about — right from your phone.

open **[cranefomo.github.io/camroll-check-web](https://cranefomo.github.io/camroll-check-web/)** on iPhone or any browser, tap "select photos", pick screenshots — done.

## what it detects

| kind | severity |
|---|---|
| seed phrases (12+ BIP39 words) | high |
| card numbers (Luhn-valid) | high |
| passport / ID (MRZ lines) | high |
| 2FA recovery codes | high |
| API keys (`sk-`, `ghp_`, `AKIA`, `xox`) | high |
| IBAN (mod-97 checksum) | medium |
| passwords (label: value) | medium |
| crypto addresses (BTC / ETH) | low |

## privacy

- **100% on-device** — photos never leave your browser
- OCR runs locally via [Tesseract.js](https://github.com/naptha/tesseract.js)
- no server, no uploads, no tracking
- report shows blurred thumbnails and masked values only

## after the scan

1. open each flagged photo on your phone and decide if it should exist
2. delete it: Photos → Recently Deleted → Delete All
3. seed phrase in a screenshot? **move funds to a new wallet**
4. card or IBAN visible? watch your statements, consider reissue if CVV was there
5. API keys? rotate them immediately

## CLI version

need to scan thousands of photos at once? use the [CLI tool](https://github.com/Cranefomo/camroll-check) — same detection, runs on Mac/Linux/Windows.

MIT license.
