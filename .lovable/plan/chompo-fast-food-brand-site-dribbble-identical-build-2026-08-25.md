# CHOMPO — Fast Food Brand Site (Dribbble-identical build)

Build a single-page, pixel-faithful recreation of the "CHOMPO" restaurant & food delivery site from the referenced shot: bold red/cream/black poster aesthetic, heavy condensed display type, hand-drawn line illustrations, collage photography, and scalloped/dripping section edges.

## Visual system

- Colors: signal red `#E11B22`, cream `#FBF3DF`, near-black `#1A1A1A`, pure white for type highlights.
- Type: heavy condensed all-caps display (Anton / Archivo Black feel) for headlines, bold rounded-slab italic for the billboard slogan, condensed bold sans for body and nav.
- Shapes: fully rounded pill buttons, sharp poster edges, scalloped bottom edges on red blocks, drip edge into the black footer, zig-zag (ticket) edge on the red CTA card.
- Textures: repeating outlined food icons (burger, pizza, fries, sandwich, chicken leg) as background pattern and marquee content.

## Sections (top to bottom, matching the shot)

1. Black floating pill navbar: CHOMPO wordmark left, red-on-white MENU pill right.
2. Red hero: "THE" / giant "CHOMPO" / "THE AMAZING FOOD YOU EVER TASTED", centered line-art storefront illustration with burger sign, red "FIND LOCATION" pill, scalloped red-to-cream edge.
3. Cream marquee strip: "CRAVE, THE CHOMPO WAY. GET READY TO CHOMP" scrolling in heavy black caps.
4. Photo/word collage grid: four tiles mixing food photos with a black tile ("Turn Up The Flavor, Turn Up The Fun.") and a red tile ("Snack Like You Mean It").
5. Circular type spiral: repeating "CHOMPO" text ring around a line-art face, with red pill tags (Pizzuuuuuu, Sanguiss, Cheazzy).
6. Red zig-zag CTA card: "READY FOR A FLAVOR ADVENTURE", subcopy, black "DISCOVER NOW →" pill, faint food-icon pattern.
7. Warped double marquee "NEW MEAL IN TOWN" with cut-out collage photos overlapping it.
8. "REAL TALK FROM REAL FOODIES" — fanned/rotated stacked review cards alternating red and black with star rows.
9. Black icon marquee band (BURGER / SANDWICH / PIZZA / FRIES / CHICKEN LEG) on a tilted red underlay.
10. Billboard section: "JOIN THE FLAVOR REVOLUTION! FUEL UP WITH CHOMPO!" over a 3D red billboard reading "Khida Laglee Call De" with a 25% discount panel, app-store badges, ladder, hand-drawn clouds and arrow, and a "CHOMPO CALL" marquee-light pill.
11. Black footer with drip top edge: link columns (HOME/PRODUCT/RECIPES/SHOP, ABOUT US/TERMS OF USE/PRIVACY POLICY/THE TEAM), contact block, red social icons, oversized outlined "CHOMPO" wordmark with pizza/sandwich/chicken cutouts.

## Motion

Restrained and mechanical: CSS marquee loops (opposite directions on stacked rows), subtle hover lift on cards and pills, review-card fan straightening slightly on hover. No fade-in-everything.

## Technical notes

- Static frontend only, no backend. All content in a single route.
- Rewrite `src/routes/index.tsx` as the CHOMPO home page, composed of section components under `src/components/chompo/`.
- Add the red/cream/black palette, radii, and shadow tokens to `src/styles.css` as semantic tokens; load display + body fonts via a `<link>` in `src/routes/__root.tsx`.
- Illustrations (storefront, billboard, clouds, face, food icons, drip/scallop/zig-zag edges) built as inline SVG so they stay crisp and recolorable.
- Photography (burger/fries/chicken/people eating) generated as images into `src/assets/` and masked into the collage cut-out shapes.
- Route-level `head()` with CHOMPO-specific title, description, og/twitter meta.
