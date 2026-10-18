# Choruswild - Update 1

Choruswild is an original single-player musical creature collection game built as a static GitHub Pages project. Update 1 is a save-compatible expansion focused on world variety, class breeding, alternate Rare/Epic progression, safer synthesis, offline progression, and a true bagpipe-led island.

## GitHub Pages setup

Upload every file in this package directly to the repository root. The package intentionally contains no folders.

1. Create or open a GitHub repository.
2. Upload all files from this ZIP directly to the repository root.
3. Commit the files.
4. Open Settings > Pages.
5. Deploy from the main branch and repository root.

The game has no CDN, external font, external image, or external audio dependency.

## Save compatibility

Update 1 upgrades save data to version 5 while continuing to read the existing `choruswild_save_v3` browser save key. Existing islands, performers, levels, currencies, Scratch cooldowns, 32-bed stage migration, and seasonal duplicate-protection progress are preserved.

The import/export save-code system remains available. Keep a backup code before replacing an older build.

## Update 1 headline content

- 11 playable worlds total.
- New island: **Piperock Highlands**.
- New islet: **Mythweaver Islet**.
- 84 species total with 84 unique base shape identifiers.
- One fresh performer added to every pre-Update-1 world/islet.
- New **Classes** system: Normal, Seasonal, Legendary, and Mythical.
- Common, Rare, and Epic remain forms, not classes. Legendary and Mythical performers can therefore also be Common, Rare, or Epic.
- New **Form Lab** gives a second targeted route to Rare and Epic forms without consuming the base performer.
- Fluxworks synthesis rebuilt around persistent reservations and non-consumed catalysts.
- Offline income and offline completion for attunement, synthesis, and Form Lab research.
- Seasonal Island success rates and waits improved.
- Duplicate-element Triple breeding fixed so alternate species with the same element combination are both obtainable.
- 22 Update-1 creatures use the expanded art/anatomy renderer.

## Piperock Highlands

Piperock Highlands is the new Highland Island and the replacement for the bagpipe concept that Thistledrone never fully delivered.

Its arrangement is explicitly pipe-led rather than merely highland-flavored:

- continuous bass drones;
- chanter melodies;
- marching snare;
- hand drums;
- dancing string counterlines;
- multiple pipe-specific performers;
- 384-step arrangement at 132 BPM.

The roster includes Dronetoad, Chanterram, Heatherpipe, Mistwhistle, Cairncap, Marchroot, Regalith, Highlandra, Clanpiper, Greatwyrm, and returning regional species.

Piperock has a level-6 Castle upgrade reaching 45 beds so its forms and class performers can coexist comfortably.

## Mythweaver Islet

Mythweaver Islet is a late-game Class-focused islet built around bells, choir, glass percussion, pulse strings, and woven harmonic textures.

Its progression centers on Legendary and Mythical bloodlines rather than being another ordinary breeding island. It introduces Threadfin, Runeshell, Loomhart, Veilbeast, Starlegend, and Mythloom alongside returning connected-world species.

Mythweaver has a level-6 Castle upgrade reaching 36 beds.

## Classes

Forms and Classes are separate systems.

### Normal

Natural Choruswild species. These use ordinary element-combination breeding, purchases for eligible singles, special awakenings, or world-specific progression.

### Seasonal

Holiday/event performers. Home-world breeding stays event-gated, while Seasonal Island keeps its festival tree permanently available and Scratch Tickets can still award home-world seasonals year-round.

### Legendary

Legendary is a class, not a rarity. Legendary recipes use a **3-element parent + 2-element parent**. The result can be Common, Rare, or Epic.

Update 1 Legendary bloodlines:

- Meadowreach: Hollowark
- Glassreef Basin: Tideprism
- Gearwake Islet: Clockwyrm
- Piperock Highlands: Clanpiper
- Mythweaver Islet: Starlegend

### Mythical

Mythical is also a class, not a rarity. Mythical recipes use a **4-element parent + 3-element parent**. The result can be Common, Rare, or Epic.

Update 1 Mythical bloodlines:

- Moonroot Hollow: Dreamwarden
- Stormforge Crag: Tempestitan
- Thistledrone Islet: Heathermaw
- Piperock Highlands: Greatwyrm
- Mythweaver Islet: Mythloom

Piperock mastery improves Legendary/Mythical breeding chance by 4 percentage points.

## One new performer on every existing world

Update 1 expands every pre-existing world rather than concentrating all new content in the two new locations.

- Meadowreach: Hollowark
- Glassreef Basin: Tideprism
- Moonroot Hollow: Dreamwarden
- Gearwake Islet: Clockwyrm
- Stormforge Crag: Tempestitan
- Thistledrone Islet: Heathermaw
- Fluxworks Islet: Vectorloom
- Crownfall Islet: Regalith
- Seasonal Island: Masquerowl

## New Rare/Epic route: Form Lab

The Form Lab is a second route to forms alongside breeding, Resonance Vaults, synthesis form rolls, and Scratch Tickets.

- Own the Common to research its Rare.
- Own the Rare to research its Epic.
- The original performer is never consumed.
- Rare research costs 90 Resonance + 1 Crest and takes 75 minutes.
- Epic research costs 240 Resonance + 3 Crests and takes 3.5 hours.
- Jobs keep progressing while the game is closed.
- Remaining time can be rushed with Gems using the normal scaled timer economy.
- Mythweaver mastery makes Form Lab research 15 percent faster.

## Fluxworks rebuild

Update 1 treats Fluxworks as a reliability rewrite rather than a cosmetic patch.

- Attunement jobs persist through panel changes, reloads, and offline time.
- Completed attunements are collected automatically.
- Five-Cycle is one persistent batch job.
- Synthesis Cores and Crests are reserved at start and refunded on abort.
- Triple/Quad catalyst monsters are checked but are **never consumed**.
- Reloading an active synthesis preserves both the job and its catalyst.
- Legacy version-4 saves receive a migration that restores catalyst performers implied by owned higher synthesis outputs or an active old synthesis job.
- Legacy over-cap Core inventories are preserved instead of truncated; the player simply cannot forge more Blank Cores until usage drops below capacity.
- Vectorloom adds another Triple synthesis path.

Fluxworks progression remains Triple -> Quad -> Pentaflux Quint, with late syntheses reaching the 10-hour timer cap.

## Duplicate Triple fix

Some element combinations intentionally map to more than one species. The old system selected only the first matching target, making the alternate Triple effectively impossible.

Update 1 now:

- displays every valid same-combination target in the Possible Monsters strip;
- divides the normal success share between those targets;
- prioritizes a missing Common target when the player already owns one of the alternatives.

Thistledrone's Thornchoir/Pipeglen combination is specifically covered by this system.

## Seasonal Island balance pass

Seasonal Island remains permanently open, but its permanent breeding tree is less punishing.

- starter-parent seasonal recipes now begin at 42 percent success;
- recipes using one previously bred seasonal begin at 32 percent;
- deeper recipes using two seasonal parents begin at 24 percent;
- mastery can improve these rates further;
- permanent-island breeding waits were shortened and capped below the normal 10-hour extreme;
- Seasonal Island receives a level-6 Festival Castle with **60 beds**, enough to display the full expanded holiday collection much more comfortably;
- Masquerowl joins the permanent Seasonal Island tree.

Home-island seasonal breeding still follows its actual event dates.

## Offline progression

Closing Choruswild no longer freezes the important long timers.

When the game resumes it processes:

- offline coin production;
- completed Core attunements;
- completed Five-Cycle batches;
- completed Fluxworks synthesis;
- completed Form Lab research;
- breeding and Nursery timers, which become ready to claim/hatch when their timestamps have elapsed.

Base offline coin production is capped at 18 hours. Mastering Gearwake doubles that cap to 36 hours.

## Existing systems retained

Update 1 keeps the systems built during the Transcendent balance patches:

- 32-bed level-5 Castles on standard worlds;
- dense-stage renderer with unique performer positions;
- 0-20,000 percent Master/Music/SFX controls;
- iOS rapid-tap/double-tap zoom protection;
- Standard, Grand, Supreme, Ultimate, and Transcendent Scratch Tickets;
- free-when-ready cooldown tickets with paid early cooldown skips;
- year-round Scratch seasonal access while breeding remains event-gated;
- seasonal Epic duplicate protection when the Common form is still missing;
- Resonance Wheel;
- Resonance Vaults;
- local autosave plus save-code export/import;
- Common/Rare/Epic anatomical form changes;
- species-specific performance animations;
- long-form island songs.

## App icon

Because Update 1 is a genuine non-seasonal expansion, the app icon temporarily follows the Update 1 content rather than the active Halloween seasonal. The icon is rendered from the same in-game SVG art system used by the shipped game rather than unrelated promotional art.
