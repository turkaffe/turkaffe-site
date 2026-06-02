# turkaffe.com — ARIRANG Tour Refresh

A mobile-first refresh of a fan site, built to support a freebie giveaway at the BTS ARIRANG World Tour (Gillette Stadium, Foxborough · Aug 5–6, 2026).

## Overview

turkaffe.com needed a quick, focused redesign timed to a concert. The site's job was simple but specific: a fan hands out business cards with a QR code alongside handmade freebies — pouches, stickers, and vinyl cutouts — and the card points here. That meant the page had to read fast on a phone, capture the tour's visual identity, and give recipients everything they needed in one scroll.

## Approach

**Design direction.** I anchored the refresh in the tour's ARIRANG aesthetic — the tour logo and lineup, carried through into Arirang red accents and ARMY purple throughout. The copy stayed warm and personal ("I hope you have a great concert!"). The layout was designed mobile-first, since nearly all traffic arrives by QR scan.

**Information architecture.** A single scroll: hero with tour dates → greeting → vinyl application instructions → a closing "take care of each other" note → social footer. Each section earns its place; nothing competes for the visitor's attention at the venue.

**Implementation.** The site runs on a Pixelarity "Fractal" theme. Rather than fight the framework, I extended it — merging new component styles into the existing stylesheet so the original reset, grid, and typography stayed intact and maintainable. New components (hero, numbered instruction steps, closing note) were namespaced to avoid collisions with the theme's existing selectors. The footer's Instagram and GitHub icons were centered, spaced, and recolored to brand purple with a matching red hover state.

## Highlights

- **Brand-driven palette** translated from tour visuals into a small, reusable token set.
- **Mobile-first single-scroll layout** optimized for QR-scan traffic.
- **Non-destructive theme extension** — new work layered cleanly onto a third-party template without breaking its framework.
- **Considered detail work** — footer alignment, spacing, and custom icon colors with matching hover states.

## Technical Notes

The stack is GitHub → AWS Amplify → CloudFront, with the domain registered at Hover and DNS via Route 53.

During the engagement I diagnosed a suspected DNS outage. Comparing local resolution against a public resolver confirmed the domain was resolving correctly to CloudFront at the authoritative level — the issue was stale caching mid-propagation, which cleared without intervention. I also resolved a deployment serving the wrong build via Amplify. Both were isolated and fixed without disrupting the live site.

## Color Palette

| Token        | Hex       | Usage                                        |
|--------------|-----------|----------------------------------------------|
| Arirang red  | `#A32D2D` | Section labels, greeting & closing note, icon hover |
| Deep purple  | `#3C3489` | Date bar, step numbers                       |
| Mid purple   | `#534AB7` | Footer icons, accents                        |
| Off-white    | `#f5f4f0` | Footer background                            |

## Outcome

Refreshed, deployed, and verified ahead of the event — on theme and on time.
