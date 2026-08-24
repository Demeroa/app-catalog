# app-catalog

Public assets for ArizelSoft apps. Deliberately separate from the app source,
which stays private — this repository holds only what has to be reachable from a
browser.

- `privacy.html` — privacy policy, linked from App Store Connect
- `catalog.v1.json` — the cross-promo list the apps read at most once a day

## Adding an app to the catalog

Both entries are `"enabled": false` until the app actually exists on the App
Store. A catalog entry with a placeholder id shows a row that links nowhere,
which is a guideline 2.1 rejection waiting to happen. Fill in the real
`iosUrl`, then flip `enabled` to `true`.

`excludeStorefronts` hides an entry in the storefronts listed — used for apps
that are not distributed in a given country. Removing an app from the list
entirely is fine too; the apps hide the whole section when nothing is left.
