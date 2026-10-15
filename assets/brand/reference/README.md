# Reference UI

`layout.json` records pixel bounds measured directly from the supplied mockup.
`ui.webp` and `ui.json` are a lossless atlas of its individual ribbons, buttons,
icons and fixed lettering. Assets preserve their original aspect ratio.

Rebuild with `python3 tools/extract_reference_ui.py`. The source is retained in
`../mockup/reference.png`; no generative substitutions are used.

`src/objects/referencePanels.js` converts measured positions once into the
540×960 game design space. It draws clean panel surfaces at 3× density and
binds the new controls to the existing reward, payment, navigation and save
controllers. Currency totals, toggle states and action feedback remain live.

Development previews support `?uiReview=home|game|store|settings|how|stars|hearts|time|reset|three|five|chapter`.
These fixtures use a displayed balance of 125 and pause the puzzle timer;
they do not grant stars. The review route is disabled in production builds.
