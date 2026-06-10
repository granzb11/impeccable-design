<!-- SEED: re-run /impeccable document once there's code to capture the actual tokens and components. -->

---
name: Impeccable Design
description: A personal design system for warm, precise, developer-native apps
---

# Design System: Impeccable Design

## 1. Overview

**Creative North Star: "The Botanical Workbench"**

A personal design system built on the tension between organic warmth and precise craft. The surface stays clean and almost austere — but the color palette is alive with deep botanical tones and amber warmth, and the type system refuses the obvious choice. Display headings speak loudly; everything else is monospace. The result is an interface that feels like it belongs to someone who makes things with care: not a startup template, not a developer's spartan terminal, but a well-equipped personal workshop with character.

The three reference points define the register. Craft supplies the restraint: nothing decorative that doesn't earn its place, generous whitespace, quality felt in the details rather than announced by them. Raycast supplies the confidence: deliberate dark-on-light contrast, interactive states that respond precisely, no apologetic design decisions. Fey supplies the palette courage: warmth expressed through specific hues, not by tinting the background beige. Combined, the system feels like a tool made by someone with taste, for daily personal use — with the secondary audience of prospective employers always in mind.

This system explicitly rejects the corporate enterprise register: no dense data tables as default, no navy-blue-on-white confidence signaling, no UI that performs seriousness at the expense of pleasure. It also rejects the generic SaaS scaffold: no hero metric grids, no glassmorphism, no gradient text. And it rejects the over-designed portfolio that mistakes motion for craft. What remains is a system that earns its elegance through precision.

**Key Characteristics:**
- Warm full palette: four named color roles, each used deliberately and sparingly
- Display + mono type system: no sans-serif intermediary — expression at the headline, precision everywhere else
- Flat surfaces at rest, responsive feedback on interaction
- Personal without being precious: functional, clear, made for real daily use

## 2. Colors

A full palette of four deliberate roles anchored in deep botanical moss, counterpointed by warm amber. The warmth lives in the brand colors, not the background.

### Primary
- **Botanical Moss** `[oklch — to be resolved during implementation; anchor hue ~140°, L ~0.30–0.40, C ~0.09–0.13]`: The brand anchor. A deep olive-green that reads as precise and organic simultaneously. Used on primary interactive elements (buttons, active states, key links), focused UI controls, and deliberate highlights. Never used decoratively — only where interaction or emphasis demands it.

### Secondary
- **Warm Amber** `[oklch — to be resolved during implementation; hue ~50–70°, L ~0.58–0.68, C ~0.12–0.18]`: The palette's warmth made explicit. Used for badges, status indicators, secondary highlights, and accent rules. Complementary to Moss without competing with it — the amber comes from a different part of the hue wheel and sits at a clearly different luminance.

### Neutral
- **Ink** `[oklch — near-black with whisper of brand hue; L ~0.10–0.15, C ~0.010–0.020, H ~140°]`: All body text, headings, and primary foreground. Must achieve ≥7:1 contrast against the bg surface.
- **Surface** `[oklch(1.000 0.000 0) — pure white]`: The foundational background. The brand carries its warmth through Moss and Amber, not through a tinted surface. No hidden warmth baked into the bg.
- **Muted** `[oklch — ink pulled ~40% toward bg, keeping ink's hue; target ≥3.5:1 contrast vs bg]`: Secondary text: metadata, labels, placeholders, disabled states. Never used for body copy.

### Named Rules

**The Craft Rule.** Warmth lives in the brand colors, never in the background tint. The surface is near-pure-white or near-pure-black. Tinting a background to feel "warm" or "cozy" is the single most common AI design tell in 2026 — the whole cream/sand/parchment/linen band is prohibited regardless of token name. If a background reads warm, it must be because the brand colors around it are warm, not because the bg itself has chroma.

**The Four Roles Rule.** Moss, Amber, Ink, and Surface each have a defined role. No color is used outside its role. No fifth color is added without a named, defined purpose. Full palette means deliberate, not abundant.

## 3. Typography

**Display Font:** `[warm-leaning serif or expressive geometric display — to be chosen at implementation; candidates: Fraunces, DM Serif Display, Canela, Playfair Display]`
**Body / UI Font:** `[clean monospace — to be chosen at implementation; candidates: Geist Mono, Commit Mono, JetBrains Mono, IBM Plex Mono]`

**Character:** Two voices, maximum contrast between them. The display face brings the warmth and editorial personality; the monospace brings precision, structure, and a developer-native honesty. There is no sans-serif intermediary — that's the deliberate choice that defines this system's character.

### Hierarchy
- **Display** (variable or heavy weight, `clamp(2.5rem, 6vw, 4.5rem)`, line-height ~1.05): Hero headings and primary section titles. The display face lives here. Use `text-wrap: balance`. Letter-spacing: ≥ -0.03em, never tighter.
- **Headline** (medium weight, `clamp(1.5rem, 3vw, 2.25rem)`, line-height ~1.2): Secondary headings, card titles, important labels. Display face if available at this size; otherwise the mono face in a heavier weight.
- **Title** (regular or medium, `1.125rem–1.25rem`, line-height 1.35): Tertiary labels, section eyebrows (used sparingly), navigation items. Mono face.
- **Body** (regular weight, `1rem`, line-height 1.65): All prose and UI copy. Mono face. Max line length: 65–75ch. Use `text-wrap: pretty` to reduce orphans.
- **Label** (medium weight, `0.75rem–0.875rem`, line-height 1.4, `letter-spacing: 0.01em`): Metadata, timestamps, form labels, badge text, status indicators. Mono face. No all-caps except for very short labels (≤4 chars) where uppercase genuinely aids scannability.

### Named Rules

**The Two-Voice Rule.** Only two typefaces touch this interface: a display face for editorial headings and a monospace for all other text. No sans-serif intermediary. The contrast between expression and precision is the system's typographic identity. Adding a third family is prohibited — if a new context demands it, solve it within the existing two voices.

**The Mono Body Rule.** Body copy is monospace. This is the deliberate choice. Do not introduce a "more readable" sans-serif at the body level — the mono is the body. Choose a mono face with open apertures and comfortable x-height for this reason; it will be readable.

## 4. Elevation

This system is flat by default. Surfaces carry no drop shadows in their resting state; depth is communicated through tonal layering — Surface (bg) versus a slightly deeper panel, and Ink-on-Surface for text. Shadows appear only as a response to state: a dialog lifting above the page, a dropdown escaping its container, a tooltip positioned above other content.

Motion energy (Responsive) means interactive states communicate through smooth transitions — color shifts, subtle transforms, focus rings — not through shadow changes. A button doesn't grow a shadow on hover; it changes color.

### Named Rules

**The Flat Rest Rule.** Surfaces are flat at rest. No drop shadows on cards, panels, sidebars, or buttons in their default state. State changes earn elevation (hover, focus, dialogs, tooltips); idle UI does not.

**The Tonal Depth Rule.** Where layering is needed (panels within a page, sidebar within a layout), use Surface (bg + slight tonal step toward Ink) rather than a drop shadow. The depth is coloristic, not cast.

## 5. Components

*Components are omitted in seed mode — no implementation exists yet. Re-run `/impeccable document` once there's code to extract real component patterns.*

## 6. Do's and Don'ts

### Do:
- **Do** use Botanical Moss on interactive elements precisely: primary buttons, active nav states, focused controls, key highlights. Its rarity makes it meaningful.
- **Do** use monospace everywhere that is not a display heading — body copy included. Lean into the choice rather than hedging it.
- **Do** animate state changes responsively: hover, focus, and active transitions should be smooth (ease-out, ~150–200ms). The interface must feel alive at the interaction level even when nothing choreographs at the page level.
- **Do** keep Surface pure white. Let Moss and Amber carry the warmth.
- **Do** pair the display face and mono face intentionally: display at large scale, mono for everything at body size and below. The hierarchy is the system.
- **Do** include `@media (prefers-reduced-motion: reduce)` alternatives for every transition — instant swaps rather than removed feedback.
- **Do** cap body line length at 65–75ch. Monospace at full container width is illegible.

### Don't:
- **Don't** tint the background. The cream/sand/beige/parchment band is prohibited. If the surface has any visible warmth baked in, it is wrong — warmth comes from the brand palette, not the bg.
- **Don't** use gradient text (`background-clip: text`). Never. Not for headings, not for the primary accent, not "just in the hero." Single solid color only.
- **Don't** use side-stripe borders as accents on cards, callouts, or alerts. Rewrite with full borders, background tints, leading icons, or nothing.
- **Don't** build the corporate enterprise register: dense data tables as default, navy-blue-on-white confidence signaling, or UI that performs seriousness at the expense of pleasure. The anti-reference is SAP, Salesforce, and old Google's product design.
- **Don't** build the generic SaaS scaffold: hero metric grids, glassmorphism cards, gradient UI surfaces, eyebrows on every section, numbered section markers as default scaffolding.
- **Don't** over-design the portfolio layer: motion louder than content, cursor trails, scroll-jacking, effects that perform sophistication rather than demonstrating it.
- **Don't** add a third typeface. Two voices, maximum. Every new context is solved within Display + Mono.
- **Don't** use drop shadows on resting surfaces. Elevation is earned by state, not applied by default.
- **Don't** use all-caps body copy. Reserve uppercase for badges and very short labels (≤4 chars) where it genuinely aids scannability.
