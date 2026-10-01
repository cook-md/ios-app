# Changelog

What changed in each release of the app, newest first. Internal engineering
notes stay in the private repository; this file is generated from it.

## [0.11.0] - 2026-09-23

### Added

- Quick Look preview for `.cook` files.
- One `cook://` URL scheme: `https://cook.md` recipe links open in the app, and
  `.cook` files open from anywhere (Files, Mail, Messages).
- The onboarding paywall is shown once, on a later day, instead of right after
  the recipe pack.

### Fixed

- Freezes while recipes were being read, and a crash when swiping between
  recipes.
- The shopping list follows recipe references all the way down.

## [0.10.4] - 2026-09-17

### Fixed

- The directory watcher no longer overflows the stack on large libraries.
- A launch crash on iOS 16 caused by Sentry's network swizzling.
- The sync banner's editor links stay on one line.
- The recipe title sits in the same place with and without an image, and the
  recipe page scrolls from anywhere in the header.

## [0.10.3] - 2026-09-14

### Fixed

- A folder's recipe count includes the recipes in its subfolders.

## [0.10.2] - 2026-09-07

### Added

- Cook Cloud paywalls: Cook Pro purchasable in the app, "On this device" and
  "On desktop" cards, two import meters; descriptive bullets with the rationale
  on top.
- Meal plans: display menus and list upcoming meals.
- Shopping list update.
- Persistent log collection with an export in Settings.

### Fixed

- A sync 402 goes to the paywall, not to sign-out.
- Kickstart install failures are shown instead of an empty recipe list.
- Subscription state refreshes when Settings opens, and the cached snapshot
  stays on screen while the refresh is in flight.
- A plan upgrade is re-linked instead of being skipped as a renewal, and the
  receipt-minted session is linked rather than trusted.
