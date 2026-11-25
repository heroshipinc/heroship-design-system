# Heroship — complete design guide for humans and AI
Release: 2026-11-25

## 1. Purpose and authority
Create consistent, polished work across web, email and social. This is a flexible system for the internal design team and their agents, not a collection of mandatory templates. The homepage is the primary visual reference; the brand bento is supporting reference.

The latest explicit owner decisions take precedence over older examples: horizontal gradients are allowed; readable text directly on gradients is allowed; body styles include every requested size and weight; desktop headings use the revised scale. Historical “don't” examples are not all current prohibitions.

Use exact tokens for existing decisions. Layout recommendations are starting defaults. If a new treatment is necessary, label it as proposed instead of claiming it is approved. A user's task brief may change content and composition without changing the underlying brand.

Visual source: https://www.figma.com/design/bGHnvjEt7U2dWNymGIvV8Q/Heroship-Design-System
Homepage reference: https://heroship.com

## 2. Before starting
Establish the audience, channel, goal, one main message, CTA, content, target dimensions, theme and available assets. Use reasonable assumptions for reversible layout choices and state them. Ask for missing approved logo/font/image assets when their absence prevents final delivery. Never invent proof points, claims or customer identities.

For a new composition:
1. Choose white, pale lavender or deep plum as the base.
2. Establish type hierarchy and generous spacing.
3. Use the primary family for brand expression.
4. If needed, choose one blue, green or gray supporting shade.
5. Reserve accent purple and signature effects for emphasis.
6. Validate readability at actual output size.
7. Review the finished composition, not only individual tokens.

## 3. Logo
Use the approved complete Heroship lockup, including its arrow. Preserve the original aspect ratio and vector geometry. Center the full visible lockup within its designated presentation area; account for the arrow, not just the wordmark. The bounding frame must contain all artwork. Do not crop or let nested frames hide parts of it.

Use the white logo on approved dark backgrounds and the dark logo on approved light backgrounds. Show it directly on approved colors; do not automatically add a white/plum panel. Check the entire lockup against the actual background. On a gradient, place it where contrast is consistently strong.

Do not stretch, rotate, recolor into accent colors, separate the arrow, retype the wordmark, add a glow/shadow, crowd it or position it off-center within its logo area. No numerical clear-space or minimum-size rule is asserted here because an authoritative value has not been confirmed. Preserve generous breathing room and inspect small-size legibility.

Logo files are deliberately excluded from this public kit. Ask the team for the approved asset. In an unfinished mockup use a labeled logo placeholder; never present reconstructed lettering as the real logo.

## 4. Color hierarchy
### Primary flat colors
| Name | Hex | Typical role |
|---|---|---|
| Plum | #10002B | Brand anchor, dark brand moments |
| Purple | #581F5A | Primary brand expression |
| Rose | #A24391 | Controlled expressive color |
| Pink | #FD87B3 | Accent within primary family |
| Blush | #FDB0B4 | Soft accent/surface moment |

The flat purple, rose and pink swatches were softened independently of the main brand gradient. Hex labels are rounded; paletteExactRGB in the token file and the CSS preserve the source precision. Both main and button gradients are unchanged by this flat-color revision.

These are the primary flat palette. Pink and blush are not default page backgrounds everywhere. The brand should still read predominantly purple/plum.

### Secondary palettes
| Family | Deep | Mid | Light |
|---|---|---|---|
| Blue | #0A88BD | #3CBAEF | #9CE5F6 |
| Green | #3A6F72 | #85A3A2 | #C1DFDE |
| Gray | #7A7A7A | #C0C0C0 | #EBEBEB |

Choose one supporting shade per composition. Repeat the same exact shade across slides in a carousel. Do not alternate light blue and mid blue merely for variety. Do not combine blue and green accents indiscriminately.

### Accent and neutral values
| Role | Hex |
|---|---|
| Accent purple | #9858FF |
| White | #FFFFFF |
| Deep canvas | #211C29 |
| Hero dark | #211C2B |
| Raised dark surface | #34283F |
| Primary ink | #2B2438 |
| Secondary ink | #3F385B |
| Muted text on dark | #BCB5C8 |
| Pale lavender surface | #F5F2FA |
| Rose tint | #F4E9EE |

Accent purple is for small emphasis, marks, focus indicators and selected brand moments. It is not an automatically approved small-text color on every background. Prefer the neutral approved text pairs.

### Background shortcuts and modes
Keep the background-role picker focused: canvas, surface, deep-plum and green-light. Blue-light and purple were intentionally removed from background shortcuts; they remain palette values for deliberate use.

| Role | Light mode | Dark mode |
|---|---|---|
| Canvas | #FFFFFF | #211C29 |
| Surface | #F5F2FA | #34283F |
| Primary text | #2B2438 | #FFFFFF |
| Secondary text | #3F385B | #BCB5C8 |
| Primary button fill | #211C29 | #FFFFFF |
| Primary button text | #FFFFFF | #211C29 |
| Explicit deep-plum | #211C29 | #211C29 |
| Explicit green-light | #C1DFDE | #C1DFDE |

Explicit color surfaces do not change color with theme. Select their text pair by the actual surface, not the surrounding page mode.

## 5. Gradients
Main brand gradient, all stops at 100% opacity (stop positions in Figma's gradient coordinates; hex values rounded for readability):
- 0%: #170234
- 22.27913%: #560A59
- 55.942392%: #A52D8F
- 88.29636%: #FD7AAB
- 100%: #FDB4B5

The saved gradient has a shortened, offset axis. Use the full-precision RGB and transform in tokens/design-tokens.json or the transform-adjusted CSS in tokens/foundations.css to reproduce it. Do not stretch these stop coordinates across the full frame and assume an exact match. Horizontal use rotates the same visual progression. The button gradient and its older effect-specific pink remain unchanged.

Do not replace these stops with the similar flat palette values. They are intentionally separate definitions.

Approved directions:
- Vertical: darkest at the top, lightest at the bottom.
- Horizontal: darkest at the left, lightest at the right.

The older blanket prohibition on horizontal gradients is superseded. Avoid reversed or arbitrary diagonal versions unless explicitly approved.

Surface gradients:
- Dark: #2B2534 to #393043.
- Light: #EEE8F6 to #F4E9EE.
The light gradient start remains distinct from the newer solid pale lavender #F5F2FA.

Text may sit directly on a gradient if every letter has adequate contrast against the area immediately behind it. Check responsive resizing and line wrapping, which can move text into lighter regions. White text over blush is not acceptable merely because white text over plum works. A solid panel is optional when needed for readability, not mandatory for every gradient.

Use the brand gradient deliberately: a hero, closing frame, branded feature or CTA moment. Do not apply it to every card, divider, button and text element simultaneously. The gradient button has its own inset-glow recipe; it is not simply the full page gradient reduced into a pill.

## 6. Approved text combinations
Use tokens/approved-pairings.json for computed ratios. Preferred pairs:
- Deep canvas text on white.
- White text on deep canvas.
- Primary ink on pale lavender or rose tint.
- White on primary flat plum or purple.
- Primary ink on blush, light green, light blue or light gray.
- White on the dark surface gradient.
- Primary ink on the light surface gradient.

This is a curated list, not all combinations that pass a contrast calculation. Blue or green text on purple is not approved. Avoid decorative rainbow text, low-contrast muted text, pink body text on purple and gray text chosen only because it almost passes.

For ordinary text require at least 4.5:1. Large text can meet 3:1 under accessibility criteria, but use the stronger 4.5:1 target for brand text wherever possible. Do not assume SemiBold automatically qualifies as bold for size exceptions. Check the actual font and rendered size. Disabled controls and decorative borders have different considerations; never use those exceptions to make essential content unreadable.

Gradient pairings must be checked locally across the whole text area, not only at gradient endpoints or the center of the heading. Brand approval and accessibility are separate checks; both matter.

## 7. Typography
Headlines: Big Issue Narrow, SemiBold.
Body and UI: Area Normal, Regular or SemiBold.
Eyebrow: Area Extended, Bold, where available.

### Web desktop headings
| Style | Size | Line height | Tracking |
|---|---:|---:|---:|
| H0 | 96px | 95% | -2% |
| H1 | 72px | 95% | -1.5% |
| H2 | 56px | 100% | -1% |
| H3 | 40px | 100% | -1% |
| H4 | 32px | 100% | -1% |
| H5 | 24px | 100% | -1% |

All six heading styles use Big Issue Narrow SemiBold. Older H4/H5 labels mentioning Area do not override this correction.

### Mobile headings
| Style | Size | Line height | Tracking |
|---|---:|---:|---:|
| H0 | 48px | 105% | -2% |
| H1 | 40px | 110% | -2% |
| H2 | 32px | 110% | -1% |
| H3 | 28px | 115% | -1% |
| H4 | 24px | 120% | -1% |
| H5 | 20px | 125% | -1% |

These are responsive starting styles. Choose a breakpoint according to content fit rather than inventing a brand-mandated breakpoint. Check long titles and narrow widths; do not reduce everything uniformly.

H0 is a visual style name, not an HTML element. Use meaningful HTML heading order (h1–h6) independently of visual size; never output an h0 tag.

### Web body: all sizes in both weights
| Size | Regular | SemiBold | Line height | Tracking |
|---|---|---|---:|---:|
| 20px | Yes | Yes | 30px | -1.5% |
| 18px | Yes | Yes | 27px | 0 |
| 16px | Yes | Yes | 24px | -1.5% |
| 14px | Yes | Yes | 21px | 0 |
| 12px | Yes | Yes | 18px | 0 |
| 10px | Yes | Yes | 15px | 0 |

Name styles clearly: Web / Body / 18px / Regular and Web / Body / 18px / SemiBold, for example. Do not hide them behind unexplained weight numbers or WIP labels.

Use 16–20px for ordinary readable content. 14px is supporting copy. 12px and 10px are available for compact annotations, not default paragraphs, key disclosures or mobile reading. Match hero supporting text to the headline's importance; do not pair a large display heading with tiny body text by default.

Button: Area Normal SemiBold, minimum 16px, 24px line height.
Eyebrow: 14px desktop / 12px mobile, 140% line height, 8% tracking.
Label: 14px SemiBold, 130% line height; this is not permission to use 14px button text.

### Font access and fallbacks
Font files are not included and this guide grants no font license. Obtain licensed files through the team and use them only where the license permits (desktop/web/email embedding are not interchangeable permissions).

Headline fallback stack: "Big Issue Narrow", "Arial Narrow", Impact, sans-serif.
Body fallback stack: "Area Normal", Arial, Helvetica, sans-serif.
Eyebrow fallback: Arial, Helvetica, sans-serif with appropriate bold weight.

These are functional fallbacks, not identical visual substitutes. Arial Narrow and Impact are not guaranteed to exist on every device. If a requested weight is unavailable, use a real available weight, declare the substitution and check the result. Never claim an unloaded brand font is in use. Check line breaks, button widths, clipping and hierarchy after substitution. Email must remain readable with system fonts.

## 8. Space, size and shape
Spacing scale: 4, 8, 12, 16, 24, 32, 48, 64, 96px.
Size scale: 16, 20, 24, 32, 40, 48, 64px.
Corner radii: square 0, small 12, card 24, pill 999px.

Practical starting defaults:
- Icon to label: 8px.
- Related elements: 12–16px.
- Separate content groups: 24px.
- Card padding: 24px; 32px for roomier compositions.
- Sections: 64–96px desktop, 24–48px mobile.
- Button height: at least 48px.
- Icons inside ordinary buttons: 20px.

Use padding and auto-layout rather than manually spacing each layer. Related content should read as a group. Distinct sections need more space than related text. Do not use random radii or shrink whitespace to fit excess copy.

## 9. Borders and focus
Card and divider borders can be subtle decorative separators. They should not compete with content.

| Background | Default card border | Hover border | Extra muted |
|---|---|---|---|
| White | #DDD8E3 | #D0C9D9 | #EBE8EF |
| Pale lavender | #D4CDDE | #C9C0D3 | #E7E1EE |
| Purple | #60348A | #704994 | #502278 |
| Deep plum | #46404E | #534D5D | #393340 |
| Black | #303030 | #3D3D3D | #222222 |

Use 1px borders at full opacity; the colors already encode their subtlety. Extra-muted strokes suit internal dividers and quiet card outlines. Do not stack multiple opacity reductions by accident. Use hover styling only for interactive cards.

These subtle borders are decorative. If a border is necessary to identify a form field or control, provide sufficient boundary contrast or another clear identifying treatment. Do not assume the decorative card value satisfies a control-boundary requirement.

Keyboard focus: a clearly visible 2px ring with a consistent 2px gap, aligned evenly around the control. Match corner geometry and avoid clipping. Accent purple can work on white; choose a tested contrasting indicator for other surfaces. Do not depend only on hover, color changes or a faint border to indicate focus, selection or error. New field/error states must be reviewed rather than inferred from card colors.

## 10. Effects and backgrounds
Effects support hierarchy and atmosphere. Use one focal signature glow per composition. Keep text on a readable surface and do not apply blur/glow to the glyphs.

- Glass / Subtle: background blur 8px.
- Glass / Standard: background blur 12px.
- Glass / Floating: background blur 24px plus shadow x0 y12 blur50 spread0, black 32%.
- Shadow / Soft: x0 y16 blur50 spread0, black 7%.
- Shadow / Overlay: x0 y4 blur14 spread0, black 32%.
- Inner / Vignette: inset x0 y0 blur80 spread0, black 20.8%.

Glass requires content behind it to demonstrate the blur. A blank white rectangle is not a convincing glass sample. A dark glass surface can use a 76% dark fill, 16% white border and 24px radius as a starting recipe. Test over actual content.

Signature glow recipe, colors and geometry:
1. Inset 0 0 18px #BC74D5.
2. Inset 14px 0 46px #9D51C2.
3. Inset -14px 0 46px #DB91AA.
4. Outer 0 0 16px #A463C8.
Base opacities: 55%, 24%, 25%, 15%.
Dark-mode variation: 72%, 36%, 38%, 22%.
Light-mode variation: 58%, 28%, 32%, 18%.
A 1.5px purple-to-blush rim is a separate treatment. Inspect both themes visually; do not merely change the page background. Figma and browser rendering can differ, so these recipes require visual comparison.

Dot-background starting recipe: 2px dots on a 24px grid, white at 14% over deep plum or deep plum at 12% over white. Treat these as adaptable implementation defaults, not a reason to crowd text. Keep the pattern decorative and exclude it from accessible content.

Provide solid fallbacks where blur/effects are unsupported, particularly email. Never encode essential information only in a glow.

## 11. Buttons and icons
Styles: Primary, Secondary, Tertiary and Gradient.
States: Default, Hover, Pressed and Disabled.
Optional icon placement: none, leading or trailing; default is none.
Standalone icon-only buttons are also required.

Common geometry: 48px minimum height, pill radius, 24px horizontal padding, 20px icon, 8px icon-label gap. Label is Area Normal SemiBold, at least 16px with 24px line height. A 160px minimum width is the standard label-button starting point; allow content to grow and check localization.

Primary: deep dark purple on light backgrounds with white text; white on dark backgrounds with deep-plum text.
Secondary: outlined treatment; test the outline and label on the actual background.
Tertiary: restrained text-led action.
Gradient: approved inset-glow pill with a dark central area, white label, purple upper glow and pink/blush lower glow.

The gradient button's base is #10002B. The established inset treatment uses pink #FE84AD (blur14, y-6), blush #FDB0B4 (blur5, y-2), and legacy effect purple #71477E (blur9, y7), at full effect opacity in the default sample. That legacy effect color is an effect-specific exception, not an additional flat primary palette color. Compare to the current Figma master before production; do not infer arbitrary hover/pressed recipes.

Keep icons optional and swappable. Provide accessible names for icon-only buttons (for example "Close dialog"), plus visible tooltips when useful. An arrow graphic alone is not an accessible name. Preserve the icon's proportions and consistent visual weight; do not mix unrelated icon families.

The existing Figma icon source is Simple Design System, including Arrow right and Plus. This public kit does not redistribute that library or assert a license. Use the team's approved icon assets/library; request access before adding a new family.

A disabled button is visibly inactive and actually disabled in implementation. Do not rely on opacity alone for semantics. Keyboard focus must remain visible and centered. Loading is not an existing published variant asserted by this kit; define and review it if required.

## 12. Layout foundations
These are flexible starting points, not mandatory templates.

### Web wireframe
Header / centered logo area and navigation
Hero / headline + supporting copy + primary CTA + optional approved image
Evidence / verified facts or approved proof
Feature sections / clear grouping and purposeful imagery
Secondary explanation / cards, comparison or FAQ
Closing CTA
Footer

Desktop content max: 1200px. On a 1440px viewport this gives 120px side margins. Start with 12 columns and 24px gutters. Narrow layouts use 16px gutters and stack content; a 4-column guide can help mobile alignment. Check the layout at intermediate sizes, not only two screenshots. Never invent proof to fill the evidence section.

### Email wireframe
Preheader
Logo
Headline
Short introduction
Primary content block
One clear primary CTA
Optional supporting details
Required footer information supplied by the team

Start with a 600px content width, 24px inner padding and 16px mobile padding. Use readable body text, system-font fallbacks and solid alternatives to effects. Keep critical content as text, not images. Test actual email-client rendering before claiming production readiness.

### Social wireframe
Centered logo area
Short headline or opening idea
One content/image focal point
Optional supporting line
Clear next step or small footer

A 1080×1350 portrait asset is a starting format, with 64px safe insets (952px usable width). Confirm the destination's current crop/safe-area requirements before delivery. A carousel should use a consistent grid, one supporting shade, recurring type hierarchy and a clear reading order. Do not change color on every slide just to create variety.

## 13. Imagery framework
Images are excluded from this public kit. Use approved imagery supplied by the team. Reserve placeholders with named roles such as Hero / Brand image, Product / Screenshot, People / Team, or Detail / Supporting crop.

For each placeholder record:
- Intended message and image role.
- Orientation and aspect ratio.
- Crop/focal point and protected area.
- Light/dark surrounding surface.
- Whether text overlays it and where.
- Source, usage permission and approval status.
- Appropriate alt text when the image is informative.

Do not fabricate product screens, clinician identities, customer endorsements or medical outcomes. Do not treat placeholder stock as approved brand photography. Preserve important subjects when cropping. Avoid generic imagery that distracts from the message. Final image selection belongs to the team; this section is a framework, not a completed art-direction library.

## 14. Accessibility and implementation
Use semantic structure, meaningful link/button labels, visible keyboard focus and a sensible reading order. Do not communicate meaning through color alone. Preserve text zoom/reflow and avoid fixed-height text containers that clip content. Respect reduced-motion preferences if motion is introduced.

For text use 4.5:1 as the default minimum. For large text exceptions and meaningful non-text UI, apply the relevant accessibility criteria and test the actual rendered component. Decorative borders may be lower contrast because they do not carry essential meaning. A subtle card outline is not an approved substitute for a necessary control boundary.

Validate contrast using the real foreground/background, including opacity, gradients, photography and overlays. Measure final combinations instead of trusting a color name. For email and social, inspect text at actual consumption size; a numerically passing tiny label can still be impractical.

## 15. Common mistakes
- Reverting to the old 48px H2 or 36px H3 desktop scale.
- Dropping 18px body or SemiBold variants.
- Using 14px labels on buttons.
- Treating H0 as semantic HTML.
- Using blue or green text on purple.
- Mixing different secondary shades across one carousel.
- Confusing flat primary colors with gradient stops.
- Treating all horizontal gradients or all text-on-gradient placements as forbidden.
- Using white text across the light end of a gradient without testing.
- Applying a bright signature glow to every component.
- Using decorative borders as the only field affordance.
- Drawing a fake logo or claiming fallback fonts are the brand fonts.
- Exporting screenshots, font files or images into this public kit.
- Deleting previous design iterations or removing unrelated cover/content.
- Claiming a Figma library publication happened because a GitHub commit succeeded.

## 16. Quality checklist before delivery
- Correct audience, message and CTA; no invented facts.
- Complete centered logo, correct aspect ratio and approved asset.
- Restrained palette; one exact supporting shade if used.
- Correct gradient stops and approved direction.
- Approved text pairs; actual gradient/image placement checked.
- All requested heading/body styles available; mobile treatment considered.
- Button text at least 16px; icon options and accessible names correct.
- Spacing/radii coherent; no clipping or accidental misalignment.
- Borders appropriate to surface and purpose; focus ring even and visible.
- Effects purposeful with functional fallbacks.
- Image placeholders clearly labeled; missing assets disclosed.
- Output checked at relevant desktop/mobile or channel dimensions.
- Delivery states which fonts were actually rendered, tests performed and unresolved decisions.

## 17. Working with an agent
Give a concise brief with the artifact, audience, objective, content, size, theme and assets. Ask for a finished artifact plus a short review against section 16. For code request semantic responsive output using tokens. For visual mockups request actual-size review. Do not accept a generic "on brand" statement without checking the artifact.

When the agent cannot load an asset or inspect Figma, it should say so, use this kit for documented decisions and ask only for essential missing material. It must not claim live synchronization. Download a new copy of the guide after updates.
