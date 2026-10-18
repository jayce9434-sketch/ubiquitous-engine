# Choruswild Update 1 - QA Report

This report covers the final Update 1 package.

## Static validation

- `game.js`: JavaScript syntax PASS.
- `sw.js`: JavaScript syntax PASS.
- `manifest.webmanifest`: valid JSON PASS.
- Runtime HTML/CSS/JS/manifest/service-worker external HTTP/HTTPS dependencies: 0.
- Runtime emoji/pictograph scan: 0 characters in `index.html`, `style.css`, `game.js`, `sw.js`, and `manifest.webmanifest`.
- App icon: 512 x 512 PNG.
- Worlds: 11.
- Species: 84 total / 84 unique IDs.
- Base art shapes: 84 total / 84 unique shape IDs.
- Class distribution: 59 Normal, 14 Seasonal, 5 Legendary, 5 Mythical, plus the Festival starter performers which are Normal-class support species.
- Update-1 expanded-art flag: 22 species.
- Service-worker cache key: `choruswild-v5-update1`.

## Browser runtime method

Headless Chromium loaded the exact final `index.html`, `style.css`, and `game.js` through an in-memory test harness. The harness only substitutes an in-memory `localStorage` implementation so controlled save states can be injected; game rendering and logic are unchanged.

No page errors or console errors occurred in the regression flows below.

## Piperock / Mythweaver / Classes / Form Lab regression

Verified in-browser:

- Piperock Highlands renders as the current world.
- Play Song starts successfully on Piperock.
- Marchroot + Reedram predicts Clanpiper and labels the result Legendary.
- Highlandra + Marchroot predicts Greatwyrm and labels the result Mythical.
- Form Lab renders on Piperock.
- Starting Rare Form Lab research creates a persistent timed job without removing the base performer.
- Mythweaver Islet can be traveled to from the World Map with an unlocked save.

## Fluxworks old-save migration + offline regression

A synthetic version-4 save was loaded with:

- Phasekiln owned but its old Rivetwisp catalyst missing;
- an active Thornmotor synthesis with Drumflare missing;
- an already-finished Leaf attunement;
- an already-finished Meadowreach Form Lab Rare job;
- two hours of offline time.

Verified after Update-1 load:

- Rivetwisp is restored.
- Drumflare is restored.
- the completed Leaf attunement becomes a tuned Leaf Core.
- the finished Form Lab job adds the researched Rare form.
- offline coin production is credited.
- runtime errors: 0.

## Fluxworks catalyst-preservation regression

A Stability-2 Fluxworks state with Rivetwisp and enough Ember Cores started Phasekiln synthesis.

Verified:

- synthesis reserves the two Ember Cores;
- Rivetwisp remains owned;
- the active synthesis survives a complete reload;
- Rivetwisp remains owned after reload;
- Abort clears the job;
- Abort refunds the reserved Ember Cores exactly;
- Rivetwisp remains owned after abort;
- runtime errors: 0.

This directly covers the reported Fluxworks issue where synthesis could delete player-owned catalyst monsters or appear not to update safely.

## Seasonal Island balance regression

Lanternling + Ribbonram were selected in the permanent Seasonal Island breeding hall.

Verified:

- Petalbop appears in the Possible Monsters display.
- displayed recipe success is 42 percent for the starter-parent tier.
- runtime errors: 0.

## Duplicate Triple accessibility regression

Thistledrone was loaded with Glimmerbug + Reedram available, Thornchoir Common already owned, and Pipeglen Common missing.

Verified:

- Possible Monsters displays both Thornchoir and Pipeglen as alternate Triple outcomes.
- both outcomes are labeled as alternate Triples.
- on a deterministic successful breed, the missing Pipeglen is selected instead of repeatedly returning the already-owned Thornchoir.
- runtime errors: 0.

## Mobile regression

Piperock Highlands was loaded at 390 x 844.

Verified:

- island screen horizontal overflow: 0 pixels;
- Market modal horizontal overflow: 0 pixels;
- runtime errors: 0.

## Screenshot evidence

The package includes browser-rendered screenshots from the final Update 1 build:

- `screenshot-update1-piperock.png` - Piperock Highlands.
- `screenshot-update1-mythweaver.png` - Mythweaver Islet.
- `screenshot-update1-classes-formlab.png` - Classes and Form Lab presentation.
- `screenshot-update1-fluxworks.png` - rebuilt Fluxworks Attunement/Synthesis interface.
- `screenshot-update1-mobile.png` - 390 x 844 mobile layout.
- `qa-runtime-piperock.png` - final runtime Piperock capture.
- `qa-60-bed-seasonal.png` - Seasonal Island level-6 60-bed stress presentation.

## Scope statement

These tests verify the listed flows and invariants. They do not claim that every possible browser/device edge case is impossible. Save export remains recommended before replacing an older deployed build.
