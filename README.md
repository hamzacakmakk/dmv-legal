# dmv-legal

Public support and legal pages for the **DMV Test** app, served by GitHub Pages
at `https://hamzacakmakk.github.io/dmv-legal/`.

| Page | Used as |
|---|---|
| `privacy.html` | Privacy policy URL — **required** by Google Play and App Store Connect |
| `terms.html` | Terms of use / EULA |
| `support.html` | Support URL — required by App Store Connect |
| `index.html` | Landing page linking to the other three |

These are the versions the stores point at. The app repository
(`dmv-practice-test`) keeps the same text inside the app itself, in
`src/app/legal/`. **If one changes, change both** — a privacy policy that
contradicts what the app shows is grounds for removal.

## No account-deletion page here

`KPSS-legal` carries one because that app has sign-in. This one does not: there
are no accounts, no sign-up and no server. Progress is stored on the device and
is gone when the app is deleted, so there is no account to delete and nothing
to request. Apple's guideline 5.1.1(v) applies to apps that create accounts, so
it does not bite here.

## app-ads.txt is not in this repo

It lives at the root of `hamzacakmakk.github.io`, because the AdMob crawler
discards the path and only ever reads `<domain>/app-ads.txt`. A copy here would
sit at `/dmv-legal/app-ads.txt` and never be read. The existing line already
covers this app — same AdMob account, one line per account.
