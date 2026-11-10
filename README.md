# apps

Public privacy policy and support pages for my iOS apps, served by GitHub Pages at https://pvhung1403.github.io/apps/.

## Layout
- `index.md` — list of all apps.
- `<slug>/` — one folder per app; `<slug>` = the bundle ID suffix (`com.hungpv.debtpayoff` → `debtpayoff`), so URLs stay
  valid if the App Store name changes. Each has `index.md` (about), `privacy.md`, `support.md`.
- `_template/` — copy for a new app (not published: folders starting with `_` are skipped by Jekyll).

| App | Slug | Source docs |
|---|---|---|
| Unowed: Debt Payoff Planner | `debtpayoff` | `debt-payoff-ios/Docs/` |

## Add a new app
1. `cp -R _template <slug>` and replace `APP_NAME`, `APP_SLUG`, `ONE_PARAGRAPH_DESCRIPTION`.
2. Paste the app's `Docs/PrivacyPolicy.md` and `Docs/Support.md` into `privacy.md` / `support.md` (keep the front matter).
3. Add a row to `index.md`, commit, push. Live in ~1 minute at `https://pvhung1403.github.io/apps/<slug>/privacy/`.
4. Put those two URLs in the app (`AppConfiguration`) and in App Store Connect.

## Update a page
Edit the app's `Docs/*.md` (source of truth), copy the body here below the front matter, commit, push.
