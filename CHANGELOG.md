# Changelog

What changed in each release of the app, newest first. Internal engineering
notes stay in the private repository; this file is generated from it.

## [0.12.0] - 2026-10-07

### Added

- Clip Recipe has a Text tab: paste a recipe from a note, a message or an
  email and it is turned into a Cooklang recipe.
- Share selected text from another app to Cook and it is converted straight
  away. If you're not signed in and hit the import limit, the text is carried
  into the app so you can sign in and finish there.
- Getting started asks three more questions — allergies, how much time you
  have on a weeknight, and what you'd like Cook to help with — so your first
  recipes fit you better. Recipes with an allergen you pick are left out.
- When your starter recipes are ready, a summary shows how many were added,
  what they were matched to and what to try next. If you don't have a plan
  yet, you can look at the plans from there — or start a free trial, when one
  is available to you.

### Changed

- Meal plans are free for everyone: every day opens in full and Add all
  ingredients works, signed in or not.
- Hidden files and folders (names starting with a dot) no longer appear in
  your recipe list or in folder counts.

### Fixed

- Sharing a recipe link to Cook while signed out and hitting the import limit
  now offers to sign in: it opens Cook, which signs you in and imports the
  recipe.
- Opening a folder in a large recipe library no longer freezes the app. Cook
  now reads only the folder you're looking at, and loads each recipe's picture
  as its row appears.
- A folder is no longer hidden when a recipe next to it has the same name.
- Recipes and meal plans whose file extension isn't lowercase, like
  `Pancakes.COOK`, now show up.
- Two recipes in the same folder with the same title no longer collapse into
  one row.
- Cook opens again on iPhones and iPads running iOS 16. It crashed at launch
  while the crash reporter catalogued the app's screens.
- Turning sync on while your recipes live in a custom or iCloud folder no
  longer freezes the app while they are copied over.
- Starting to cook no longer freezes the app while step photos and the aisle
  list are read from a slow folder. Each step's photo appears as you reach it.
- Signing in from the plans screen at the end of getting started brings you
  back to your summary instead of jumping straight to your recipes.
- Tapping "Start cooking" while the plans screen was still opening could stop
  every later plans screen from opening until you relaunched the app. The
  summary now waits for the plans screen to close first.
- The one-time plans offer is no longer used up when the plans could not be
  loaded.
- A recipe with ".cook" in the middle of its name, like `Dr.Cook's Chili.cook`,
  now shows its full name.
- A recipe whose name ends in `.menu` or `.cook` before the extension, like
  `Sunday.Menu.cook`, is found again from the shopping list.
- Opening a recipe that iCloud hasn't downloaded yet no longer freezes the app
  while the file is fetched.

## [0.11.1] - 2026-10-02

### Added

- Siri: move between cooking steps and finish cooking by voice.
- "What's new" in Settings → About opens this changelog.
- Hit the import limit without an account? You can now sign in for free
  to keep importing, and the import picks up where it stopped.

### Changed

- The import gates (photo and social-link imports) use the same wording as the
  web converter.
- Signed-out users are asked to sign in at feature gates instead of being shown
  the purchase paywall.
- Sign-in and import prompts no longer suggest that an account alone
  brings sync, photo imports or meal plans: sync comes with Cook Basic, photo
  and social-link imports with a Cook Cloud plan.

### Fixed

- Changes in a recipe folder are picked up reliably again.
- Turning on sync no longer freezes the app while it checks a large recipe
  folder.
- Importing a recipe after your cook.md session expired no longer fails with a
  message about image clipping: you're asked to sign in again, and the import
  carries on.
- Importing too quickly now tells you how many seconds to wait.
- Importing a social media link while signed out asks you to sign in,
  instead of stopping after the spinner with nothing on screen.

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
