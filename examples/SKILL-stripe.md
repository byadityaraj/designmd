---
name: Stripe
url: https://stripe.com
colors:
  primary: "#533afd"
  background: "#ffffff"
  text-primary: "#000000"
  surface: "#f8fafd"
  accent-blue: "#533afd"
  accent-light-blue: "#e5edf5"
  text-heading: "#061b31"
  text-secondary: "#50617a"
  text-muted: "#64748d"
  text-inverse: "#ffffff"
  border-default: "#061b31"
  border-accent: "#533afd"
  input-placeholder: "#7d8ba4"
elevation:
  card: "rgba(50, 50, 93, 0.12) 0px 16px 32px 0px, rgba(23, 23, 23, 0.08) 0px 15px 35px 0px, rgba(23, 23, 23, 0.06) 0px 3px 6px 0px"
typography:
  display:
    family: sohne-var
    size: 40
    weight: 700
    line-height: 1.03
  heading-lg:
    family: sohne-var
    size: 34
    weight: 700
    line-height: 1.2
  heading-md:
    family: sohne-var
    size: 26
    weight: 700
    line-height: 1.2
  heading-sm:
    family: sohne-var
    size: 22
    weight: 400
    line-height: 1.5
  body:
    family: sohne-var
    size: 16
    weight: 400
    line-height: 1.5
  caption:
    family: sohne-var
    size: 10
    weight: 400
    line-height: 1.3
spacing:
  base: 4px
  scale: [0, 4, 8, 12, 16, 20, 24, 32]
radius:
  sm: 3px
  md: 4px
  lg: 6px
  full: 100px
motion:
  duration-default: 0.2s
  duration-fast: 0.15s
  duration-slow: 0.8s
  ease-default: cubic-bezier(0.33, 1, 0.68, 1)
components:
  button-primary:
    bg: "{colors.accent-blue}"
    fg: "{colors.text-inverse}"
    radius: "{radius.md}"
    padding: "15.5px 24px 16.5px 24px"
    font-size: 16px
    font-weight: 400
  button-secondary:
    bg: null
    fg: "{colors.accent-blue}"
    border: "{colors.accent-blue}"
    radius: "{radius.md}"
    padding: "11.5px 20px 12.5px 20px"
    font-size: 14px
    font-weight: 400
  button-ghost:
    bg: null
    fg: "{colors.text-heading}"
    border: "{colors.text-heading}"
    radius: "{radius.md}"
    padding: "12px 0px 12px 0px"
    font-size: 14px
    font-weight: 400
---
# Stripe — Design System Skill

## 1. Mission
When building any interface for Stripe, the agent MUST follow the tokens and rules in this document exactly, and MUST NOT introduce values outside them. The agent's role is to construct user interfaces for Stripe's financial services platform marketing site, ensuring brand consistency and adherence to the established design system. The agent MUST preserve the vibrant, undulating gradient background, which serves as a signature visual element across key sections of the site.

## 2. Brand
*   **Brand Name**: Stripe
*   **URL**: https://stripe.com
*   **Product Category**: Financial services platform, payment processing, economic infrastructure.
*   **Voice/Positioning**: "Stripe est une plateforme de services financiers qui aide tous types d’entreprises à accepter des paiements, créer des modèles de facturation flexibles et gérer les mouvements de fonds."

## 3. Style Foundations
*   **Color**
    *   `primary`: `#533afd` (`var(--hds-color-accent-charm-bg)`) — MUST back all primary CTAs and active states.
    *   `background`: `#ffffff` (`var(--hds-color-util-bg-min)`) — MUST be used for main content areas.
    *   `background-quiet`: `#f8fafd` (`var(--hds-color-util-bg-quiet)`) — MUST be used for subtle background variations.
    *   `background-accent-light`: `#e5edf5` (`var(--hds-color-util-neutral-50)`) — MUST be used for secondary accent backgrounds.
    *   `text-primary`: `#000000` — MUST be used for main body text.
    *   `text-heading`: `#061b31` (`var(--hds-color-heading-solid)`) — MUST be used for all headings.
    *   `text-secondary`: `#50617a` — MUST be used for secondary textual content.
    *   `text-muted`: `#64748d` (`var(--hds-color-heading-subdued)`) — MUST be used for tertiary or less emphasized text.
    *   `text-inverse`: `#ffffff` (`var(--hds-color-action-text-onSolid)`) — MUST be used for text on dark or colored backgrounds.
    *   `text-accent`: `#533afd` — MUST be used for interactive text elements and accents.
    *   `border-default`: `#061b31` — MUST be used for dark borders.
    *   `border-accent`: `#533afd` (`var(--hds-color-accent-border-solid)`) — MUST be used for accent borders.
    *   `input-placeholder`: `#7d8ba4` (`var(--hds-color-input-text-placeholder)`) — MUST be used for input placeholder text.
*   **Typography**
    *   `Display`: `sohne-var 40px 700` · line-height `1.03` (`var(--hds-font-heading-xl-lineHeight)`) — MUST be used for hero headlines.
    *   `Heading 1`: `sohne-var 34px 700` · line-height `1.2` (inferred from extracted typography shape) — MUST be used for primary section titles.
    *   `Heading 2`: `sohne-var 26px 700` · line-height `1.2` (inferred from extracted typography shape) — MUST be used for major sub-section titles.
    *   `Heading 3`: `sohne-var 22px 400` · line-height `1.5` (inferred from extracted typography shape) — MUST be used for card titles or minor sub-headings.
    *   `Body`: `sohne-var 16px 400` · line-height `1.5` (inferred from extracted typography shape) — MUST be used for all standard paragraph text.
    *   `Caption`: `sohne-var 10px 400` · line-height `1.3` (`var(--hds-font-input-text-md-lineHeight)`) — MUST be used for small descriptive text.
*   **Spacing**
    *   `base`: `4px`.
    *   `scale`: `0px, 4px, 8px, 12px, 16px, 20px, 24px, 32px`. Agents MUST pick spacing ONLY from this scale.
*   **Radius**
    *   `sm`: `3px` — MUST be used for minor rounded elements.
    *   `md`: `4px` — MUST be used for buttons and cards.
    *   `lg`: `6px` — MUST be used for larger container elements.
    *   `full`: `100px` — MUST be used for fully rounded elements like pills or avatars.
*   **Elevation**
    *   `card`: `rgba(50, 50, 93, 0.12) 0px 16px 32px 0px, rgba(23, 23, 23, 0.08) 0px 15px 35px 0px, rgba(23, 23, 23, 0.06) 0px 3px 6px 0px` — MUST be applied to cards and elevated containers.
*   **Motion**
    *   `duration-default`: `0.2s` (inferred from `.bento-dialog-graphic--mobile-gradient-container` transition)
    *   `duration-fast`: `0.15s` (from `.navigation-hover-arrow svg` animation `nav-hover-arrow-out`)
    *   `duration-slow`: `0.8s` (from `.bento-overlay-gradient` animation `bento-overlay-gradient-opacity-animation`)
    *   `ease-default`: `cubic-bezier(0.33, 1, 0.68, 1)` (from `.bento-dialog-graphic--mobile-gradient-container` transition)

## 4. Accessibility (WCAG 2.2 AA gates)
*   `#061b31` on `#ffffff` → `17.37:1`, passes AAA.
*   `#50617a` on `#f8fafd` → `6.03:1`, passes AA.
*   `#50617a` on `#ffffff` → `6.3:1`, passes AA.
*   `#64748d` on `#ffffff` → `4.75:1`, passes AA.
*   `#533afd` on `#ffffff` → `6.19:1`, passes AA.
*   `#061b31` on `#ffe6f5` → `14.8:1`, passes AAA.
*   `#061b31` on `#f8fafd` → `16.61:1`, passes AAA.
*   `#1a2c44` on `#ffffff` → `14.12:1`, passes AAA.
*   Body text contrast MUST be ≥ 4.5:1; large text (≥24px or ≥18.66px bold) ≥ 3:1.
*   Non-text UI (icons, borders, focus rings) MUST be ≥ 3:1 against adjacent color.
*   Interactive target size MUST be ≥ 24×24px (WCAG 2.2 Target Size minimum).
*   Every interactive element MUST have a visible `:focus-visible` indicator, ≥ 3:1, not obscured (WCAG 2.2 Focus Not Obscured).
*   Color MUST NOT be the only means of conveying state (pair with icon/text).

## 5. Writing Tone
*   Button and heading text MUST use Sentence case (e.g., "Démarrer maintenant", "Contacter notre équipe").
*   Call-to-action (CTA) text MUST be direct and action-oriented (e.g., "Démarrer maintenant", "Se connecter").
*   Microcopy SHOULD be professional and empowering, reflecting Stripe's role as a financial infrastructure provider.
*   Numbers and currency SHOULD follow French conventions as observed in the source (e.g., "5,46 $US").

## 6. Rules: Do
*   ALWAYS use `{colors.primary}` (`#533afd`) for primary interactive elements.
*   ALWAYS use `{typography.body.family}` (`sohne-var`) for all textual content.
*   ALWAYS apply `{radius.md}` (`4px`) to buttons and cards.
*   ALWAYS use a spacing value from the `{spacing.scale}` (`0, 4, 8, 12, 16, 20, 24, 32`) for layout.
*   ALWAYS ensure text contrast meets WCAG AA standards, with `{colors.text-primary}` on `{colors.background}` measuring `17.37:1`.
*   ALWAYS include a visible `:focus-visible` indicator for all interactive elements.
*   ALWAYS use `{colors.text-heading}` (`#061b31`) for all heading elements.
*   ALWAYS apply `{elevation.card}` to elevated UI components like cards.

## 7. Rules: Don't
*   NEVER use a hex color outside the §3 palette.
*   NEVER introduce a font family not specified in `{typography.*}`.
*   NEVER use a font size or weight not defined in the §3 typography scale.
*   NEVER use a spacing value that is not a member of the §3 scale.
*   NEVER introduce a border-radius value not specified in the §3 radius scale.
*   NEVER make an interactive touch target smaller than `24×24px`.
*   NEVER rely solely on color to convey information or state.
*   NEVER use transitions that do not respect `prefers-reduced-motion`.

## 8. Expected Behavior
*   Interactive elements MUST use `0.2s cubic-bezier(0.33, 1, 0.68, 1)` for transitions unless a component explicitly overrides it.
*   On `:hover`, elements SHOULD apply a subtle visual change, such as a background color shift (e.g., primary buttons transition to `background-color: rgb(26, 58, 92)` (inferred)) or text color change (e.g., links transition to `color: var(--hds-color-text-solid)`).
*   On `:focus-visible`, interactive elements MUST display a `box-shadow: rgba(99, 91, 255, 0.1) 0px 0px 0px 3px` ring (from `.time-of-day-select__trigger:focus-visible`), ensuring a minimum 3:1 contrast against the adjacent background.
*   All transitions MUST respect the user's `prefers-reduced-motion` setting, disabling or simplifying animations when requested.

## 9. Component Rule Expectations
Every interactive element MUST define all applicable states; a component with only a default state is incomplete.

*   **Button Primary**
    *   default: `bg: {colors.accent-blue}` (`#533afd`) / `fg: {colors.text-inverse}` (`#ffffff`) / `border: transparent` / `radius: {radius.md}` (`4px`) / `padding: 15.5px 24px 16.5px 24px`
    *   hover: `background-color: rgb(26, 58, 92)` (inferred from `.UniversalChatCtaCard__cta:hover`)
    *   focus: `box-shadow: rgba(99, 91, 255, 0.1) 0px 0px 0px 3px` (from `.time-of-day-select__trigger:focus-visible`)
    *   active: `background-color: rgb(10, 37, 64)` (from `.CookieSettings_CookieSettings__Button__a91Gb:active`)
    *   disabled: `background-color: rgb(10, 37, 64)` (from `.CookieSettings_CookieSettings__Button__a91Gb:disabled`) / `color: rgb(255, 255, 255)` (from `.CookieSettings_CookieSettings__Button__a91Gb:disabled`) / `pointer-events: none` / `not focusable`
*   **Button Secondary**
    *   default: `bg: transparent` / `fg: {colors.accent-blue}` (`#533afd`) / `border: 1px solid {colors.accent-blue}` (`#533afd`) / `radius: {radius.md}` (`4px`) / `padding: 11.5px 20px 12.5px 20px`
    *   hover: `background-color: {colors.accent-blue}` (`#533afd`) (inferred) / `color: {colors.text-inverse}` (`#ffffff`) (inferred)
    *   focus: `box-shadow: rgba(99, 91, 255, 0.1) 0px 0px 0px 3px` (from `.time-of-day-select__trigger:focus-visible`)
    *   active: `background-color: rgb(10, 37, 64)` (inferred, similar to primary) / `color: {colors.text-inverse}` (`#ffffff`) (inferred)
    *   disabled: `opacity: 0.5` (inferred) / `pointer-events: none` / `not focusable`
*   **Button Ghost** (e.g., Nav Link)
    *   default: `bg: transparent` / `fg: {colors.text-heading}` (`#061b31`) / `border: transparent` / `radius: {radius.md}` (`4px`) / `padding: 12px 0px 12px 0px`
    *   hover: `color: var(--hds-color-action-text-solidHover)` (from `.case-study-card__link:hover`, resolves to a darker text color)
    *   focus: `box-shadow: rgba(99, 91, 255, 0.1) 0px 0px 0px 3px` (from `.time-of-day-select__trigger:focus-visible`)
    *   active: `color: rgb(66, 71, 112)` (from `.CookieSettings_CookieSettings__Link__QlCtd:active`)
    *   disabled: `color: rgb(66, 71, 112)` (from `.CookieSettings_CookieSettings__Link__QlCtd:disabled`) / `pointer-events: none` / `not focusable`
*   **Link**
    *   default: `fg: {colors.text-secondary}` (`#50617a`) (inferred from footer links) / `text-decoration: none` (inferred)
    *   hover: `color: var(--hds-color-text-solid)` (from `a.footer-links-block__item:hover`, resolves to `#000000` (inferred)) / `text-decoration: underline` (inferred)
    *   focus: `box-shadow: rgba(99, 91, 255, 0.1) 0px 0px 0px 3px` (inferred, as no specific link focus)
    *   active: `color: rgb(66, 71, 112)` (from `.CookieSettings_CookieSettings__Link__QlCtd:active`)
    *   disabled: `color: rgb(66, 71, 112)` (from `.CookieSettings_CookieSettings__Link__QlCtd:disabled`) / `pointer-events: none` / `not focusable`
*   **Card** (e.g., `.case-study-card`)
    *   default: `bg: {colors.background}` (`#ffffff`) / `radius: {radius.md}` (`4px`) / `shadow: {elevation.card}`
    *   hover: `shadow: rgba(50, 50, 93, 0.15) 0px 20px 40px 0px, rgba(23, 23, 23, 0.1) 0px 18px 40px 0px, rgba(23, 23, 23, 0.08) 0px 5px 8px 0px` (inferred, slightly more pronounced shadow)
    *   focus: `outline-color: initial` (from `.case-study-card:focus-visible`) / `outline-width: initial` (from `.case-study-card:focus-visible`) / `box-shadow: rgba(99, 91, 255, 0.1) 0px 0px 0px 3px` (inferred for a visible focus ring as extracted is `initial`)
    *   active: (none observed in source)
    *   disabled: (none observed in source)

## 10. Quality Gates (testable)
*   Every interactive text/background pair measures ≥ 4.5:1 (≥ 3:1 for large text).
*   Every interactive element exposes a visible `:focus-visible` ring ≥ 3:1.
*   No color appears that is not in the §3 palette.
*   Every font family used is a subset of `{typography.*}`.
*   Every spacing value used is a member of the §3 scale.
*   Every radius used is a member of the §3 radius scale.
*   Every interactive target is ≥ 24×24px.
*   Every component renders all of its applicable states (§9).
*   All animations and transitions respect `prefers-reduced-motion`.