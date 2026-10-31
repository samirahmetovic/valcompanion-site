# Val Companion – website

Support, legal and data-deletion pages for the Val Companion app, served with
GitHub Pages at <https://samirahmetovic.github.io/valcompanion-site/>.

Plain HTML + one stylesheet: no build step, no JavaScript, no cookies, no
external fonts (so the privacy policy's "this website" section stays true).

| Page | English | German |
|---|---|---|
| Home | `index.html` | `de/index.html` |
| Support | `support.html` | `de/support.html` |
| Privacy policy | `privacy.html` | `de/datenschutz.html` |
| Terms of use | `terms.html` | `de/nutzungsbedingungen.html` |
| Delete your data | `delete-data.html` | `de/daten-loeschen.html` |

No imprint and no postal address on purpose (removed 31 Oct 2026). Selling
subscriptions from Germany normally requires an Impressum (§ 5 DDG) with an
address where you can be reached – once there is a business address (e.g. an
Impressum service), add `imprint.html` / `de/impressum.html` again and put the
address into privacy and terms.

## Publishing

1. Create a **public** repository `valcompanion-site` on GitHub and push this folder.
2. Repository → Settings → Pages → *Deploy from a branch* → `main` / `/ (root)` → Save.
3. After a minute the site is live at the URL above.

## Where the links are used

Base URL: `https://samirahmetovic.github.io/valcompanion-site/`

| Where | Field | Page |
|---|---|---|
| App Store Connect | App Information → Privacy Policy URL | `privacy.html` (German localization: `de/datenschutz.html`) |
| App Store Connect | Version → Support URL / Marketing URL | `support.html` / start page |
| App Store Connect | App description, last line (required for subscriptions) | `Terms of Use: …/terms.html` (+ optionally Apple's standard EULA) |
| Play Console | App content → Privacy policy | `privacy.html` |
| Play Console | Store settings → Contact details → Website | `support.html` |
| Play Console | Data safety → data deletion link | `delete-data.html` |
| RevenueCat | Paywall → Terms / Privacy links | `terms.html` / `privacy.html` |

**Privacy forms** (must match the privacy policy):

- App Store → App Privacy: *Purchases → Purchase History*, used for App
  Functionality, not linked to identity, no tracking.
- Play → Data safety: *Financial info → Purchase history*, collected, not
  shared, encrypted in transit, deletion on request; no account creation
  (sign-in is Riot's).

## Open points

- [ ] Accept RevenueCat's data processing agreement (the privacy policy refers to it).
- [ ] Impressum with a business address (see above). Note: the App Store's EU
      trader status shows an address and phone number in the store anyway.
- [ ] VAT ID, if there is one → into the Impressum once it exists.
- [ ] `support.html` / `delete-data.html` explain the hidden Support ID
      (hold *Restore purchases* 5 s) – remove that if it should stay private.
- [ ] Optional: have the texts checked (e.g. eRecht24, IT-Recht Kanzlei) –
      they are written for this app but are no legal advice.

## Editing

Every page exists twice – change the English and the German version together,
and update the "Last updated / Stand" date in privacy and terms. When the app
starts sending data somewhere new (analytics, a server, another API), the
privacy policy and both stores' privacy forms must be updated **before** that
release.
