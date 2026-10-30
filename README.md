# Syahmi's Digital Business Card

Live link (after deploy): https://syhsolar.github.io/card/
Repo: `syhsolar/card` on GitHub (public, GitHub Pages from `main`).

## Files
| File | What it is |
|---|---|
| `index.html` | The card page (all styles and code inside this one file) |
| `syahmi.vcf` | "Save my contact" file: name, Senior Sales, PC Image Sdn Bhd, 019-676 1077, syhsolar@outlook.com, logo as contact photo |
| `logo.jpg` | PC Image logo (copied from `pcbuild-generator/quotation-template/pcimage-logo.jpg`) |
| `contact-photo.jpg`, `icon.png`, `og.jpg` | Square logo for the contact photo, browser icon, and WhatsApp link preview image |
| `qr.png` / `qr-print.png` / `qr.svg` | QR code to the card link. Use `qr-print.png` (1480 px) or `qr.svg` for printing on stickers, the counter stand or receipts |

## Common changes
- **Promo banner:** in `index.html`, find the `PROMO` comment and change the text under "This month". Delete that whole `<div class="promo">` to hide it.
- **Socials / website:** in `index.html`, find `EDIT HERE` near the bottom and paste the full links (e.g. `"https://www.facebook.com/..."`). Empty `""` stays hidden; the whole "Find PC Image online" section stays hidden until at least one link is filled.
- **Services list:** edit the four `<li>` items under "What I can help with".
- **Phone or email change:** update `index.html` (WhatsApp, Call, Email links and `WA_NUMBER`) and `syahmi.vcf`. Easiest: ask Claude "update my business card phone to ...".

## Redeploy after a change
```bash
cd ~/Desktop/my-ai/business-card && git add -A && git commit -m "Update card" && git push
```
GitHub Pages updates in about a minute. The link and QR code never change, so printed QR codes and NFC cards keep working.

## NFC card
1. Buy a blank **NTAG215 or NTAG216 NFC PVC card** on Shopee (about RM3 to RM10 each; get 2 or 3 spares).
2. Install the free **NFC Tools** app (Android or iPhone).
3. Write → Add a record → URL/URI → `https://syhsolar.github.io/card/` → Write → hold the card to the back of the phone.
4. Test by tapping it on another phone. Once it works, you can lock it in NFC Tools (Other → Lock tag). Locking is permanent.
Works on Android with NFC turned on, and on iPhone XS or newer without any app.

## Later (phase 2)
Google Wallet pass first (free, most customers use Android). Apple Wallet needs a paid Apple Developer account (USD99/year).
