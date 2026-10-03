---
name: Clinical Integrity
colors:
  surface: '#f2fbff'
  surface-dim: '#c6dee8'
  surface-bright: '#f2fbff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#e4f7ff'
  surface-container: '#d9f2fd'
  surface-container-high: '#d4ecf7'
  surface-container-highest: '#cee6f1'
  on-surface: '#061e26'
  on-surface-variant: '#3e4946'
  inverse-surface: '#1d333c'
  inverse-on-surface: '#ddf5ff'
  outline: '#6e7a75'
  outline-variant: '#bdc9c4'
  surface-tint: '#006b5b'
  primary: '#006051'
  on-primary: '#ffffff'
  primary-container: '#0b7b69'
  on-primary-container: '#b3ffeb'
  inverse-primary: '#7bd7c1'
  secondary: '#47626e'
  on-secondary: '#ffffff'
  secondary-container: '#c7e4f2'
  on-secondary-container: '#4b6772'
  tertiary: '#005a89'
  on-tertiary: '#ffffff'
  tertiary-container: '#0073ae'
  on-tertiary-container: '#e7f2ff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#98f4dd'
  primary-fixed-dim: '#7bd7c1'
  on-primary-fixed: '#00201a'
  on-primary-fixed-variant: '#005144'
  secondary-fixed: '#c9e7f4'
  secondary-fixed-dim: '#aecbd8'
  on-secondary-fixed: '#001f28'
  on-secondary-fixed-variant: '#2f4b55'
  tertiary-fixed: '#cce5ff'
  tertiary-fixed-dim: '#93ccff'
  on-tertiary-fixed: '#001d31'
  on-tertiary-fixed-variant: '#004b73'
  background: '#f2fbff'
  on-background: '#061e26'
  surface-variant: '#cee6f1'
typography:
  display-lg:
    fontFamily: Noto Sans
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: Noto Sans
    fontSize: 26px
    fontWeight: '700'
    lineHeight: 34px
    letterSpacing: -0.01em
  headline-lg:
    fontFamily: Noto Sans
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Noto Sans
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 28px
  headline-sm:
    fontFamily: Noto Sans
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 26px
  body-lg:
    fontFamily: Noto Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 26px
  body-md:
    fontFamily: Noto Sans
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 22px
  body-sm:
    fontFamily: Noto Sans
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 18px
  label-lg:
    fontFamily: Noto Sans
    fontSize: 14px
    fontWeight: '600'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-md:
    fontFamily: Noto Sans
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.02em
  label-sm:
    fontFamily: Noto Sans
    fontSize: 11px
    fontWeight: '700'
    lineHeight: 14px
    letterSpacing: 0.04em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  gutter: 1rem
  gutter-desktop: 1.5rem
  margin: 1rem
  margin-desktop: 2rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2rem
---

## Brand & Style

The design system establishes a high-reliability visual architecture engineered for mission-critical public health logistics, cold-chain monitoring, and multi-tier medical supply distribution. The audience encompasses district healthcare officers, dispensary pharmacists, and community health frontline workers operating across diverse environmental conditions and connectivity constraints.

The visual narrative pairs institutional authority with immediate human reassurance. It blends purposeful modern minimalism with high-density data legibility:
- **Clinical Precision**: Unambiguous visual status cues, high-contrast borders, and structured information layouts mitigate operational error under pressure.
- **Civic Trust**: Deep medical emerald and structural slate convey government-grade operational rigor, while soft mint field surfaces diminish optical fatigue during extended field shifts.
- **Cross-Script Parity**: Native Devanagari (Hindi and Marathi) and Latin scripts receive equal typographic weight, optical alignment, and vertical breathing room, avoiding translation-induced layout breakage.

## Colors

The palette enforces strict WCAG 2.1 AAA compliance for standard informational typography and AA for heavy operational badges against clinical backdrops.

### Foundational Palette
- **Primary (`#0B7B69`)**: Core medical emerald. Designates primary operational actions, active navigation states, verified batch statuses, and institutional accents.
- **Secondary (`#0F2D37`)**: Deep slate dark blue. Anchors persistent app bars, high-level logistical containers, table headers, and structural chrome.
- **Neutral Foreground (`#132A32`)**: Deepest slate-carbon. Applied to all high-contrast primary text, critical iconography, and high-priority data points.
- **Neutral Background (`#F4F9F8`)**: Calming ice-mint tint. Forms the persistent root application surface, neutralizing harsh glare in outdoors field environments while differentiating from card containers.
- **Surface Elevation (`#FFFFFF`)**: Pure clinical crisp white for interactive cards, sheets, modal dialogues, and input fields.
- **Border Subtle (`#D1E5E1`)**: Balanced soft mint-slate for structural hairline dividers and card boundaries.

### Diagnostic & Status Roles
- **Verified / Compliant (`#16A34A`)**: Cold-chain stable, stock verified, batch cleared.
- **Attention / Low Stock (`#D97706`)**: Approaching expiration, threshold warning, buffer stock compromised.
- **Critical / Excursion (`#DC2626`)**: Temperature breach, stock exhausted, transit anomaly.
- **Informational / Transit (`#0284C7`)**: Dispatch en route, synchronization in progress, audit log entry.

## Typography

Noto Sans serves as the universal typographic engine across Latin and native Devanagari script matrices (Hindi and Marathi). The typeface ensures structural harmony between varying glyph heights, conjunct consonants, and matra accent marks, preventing vertical clipping and baseline shifts during on-the-fly language switching.

### Script-Specific Optimization Rules
- **Devanagari Vertical Rhythm**: Devanagari glyphs with top horizontal lines (*shirorekha*) and descending vowels require an intentional minimum line-height of 1.5x in body text and 1.3x in headings to eliminate optical collisions.
- **Multilingual Density**: In bilingual layouts where Marathi/Hindi runs alongside English, label text maintains equivalent point size with relaxed padding (+2px top/bottom) to preserve balanced visual baselines.
- **Tabular Data Points**: All numeric data sets (inventory counts, temperatures, timestamps, and transit serials) must use monospaced numeric figures (`font-variant-numeric: tabular-nums`) to ensure strict vertical column alignment in logistics logs.

## Layout & Spacing

The layout philosophy relies on a strict, fluid grid aligned to an 8-point base module, optimized mobile-first to accommodate low-resolution field tablets and ruggedized handheld devices before expanding to multi-column desktop dispatch consoles.

### Breakpoint Structure
- **Mobile Handheld (`< 640px`)**: Single-column layout. Margin token set to `margin` (16px), inner gutter at 16px. Touch targets enforce a 48px baseline (never below 44px). Bottom navigation persists for thumb-zone priority.
- **Tablet Dispatch (`640px - 1024px`)**: Dual-column split layout (e.g., active inventory roster beside detail pane). Margin shifts to 24px with 16px gutters.
- **Desktop Logistics Hub (`> 1024px`)**: 12-column responsive fluid grid max-capped at 1440px wide. Outer margin expands to `margin-desktop` (32px), column gutters expand to `gutter-desktop` (24px). Sidebar persists in an anchored state.

### Information Spacing Rhythm
Form containers and verification tables maintain high internal density (`space-sm` to `space-md` gaps) to expose maximum actionable data above the fold without requiring excessive vertical scrolling during stock checkouts.

## Elevation & Depth

This system avoids heavy drop shadows and decorative blurs, adopting low-elevation structural planes designed for high readability in high-ambient-light field situations. 

### Elevation Hierarchy
- **Level 0 (Base canvas)**: `#F4F9F8` tint. Completely flat.
- **Level 1 (Clinical Cards & Data Rows)**: Crisp `#FFFFFF` surface bordered with a structural 1px solid hairline (`#D1E5E1`) and an ambient, low-opacity shadow: `0 1px 3px rgba(15, 45, 55, 0.05)`.
- **Level 2 (Interactive Floating Bar, Dropdowns, Segmented Controls)**: `#FFFFFF` surface with `0 4px 12px rgba(15, 45, 55, 0.08)` and border `#B9DBD4`.
- **Level 3 (Modal Dialogues, Emergency Override Drawers)**: `#FFFFFF` surface accompanied by a 40% opacity secondary-tint backdrop (`rgba(15, 45, 55, 0.5)`), casting a directional elevation shadow of `0 12px 28px rgba(15, 45, 55, 0.16)`.

Borders work in tandem with elevation to deliver reliable contrast when viewed on screens with reduced brightness or suboptimal panel calibration.

## Shapes

The design uses a restrained, professional corner curvature (`roundedness: 1`). Structural elements avoid both toy-like hyper-roundedness and stark, hostile sharp corners, striking a balance of administrative authority and operational ergonomics.

- **Base Radius (0.25rem / 4px)**: Checkboxes, status tag indicators, compact data tables, and input step-counters.
- **Medium Radius (`rounded-lg`, 0.5rem / 8px)**: Primary operational buttons, text input fields, logistical metrics tiles, notification banners, and modal containers.
- **Large Radius (`rounded-xl`, 0.75rem / 12px)**: Standalone clinical cards, bottom action sheets, and inventory scanner viewfinder overlays.
- **Fully Rounded (Pill / 9999px)**: Reserved strictly for multilingual script toggles, dynamic live status badges (e.g., active temperature telemetry), and circular icon touch anchors.

## Components

### Buttons & Action Controls
- **Primary Operational Button**: Background `#0B7B69`, foreground `#FFFFFF`, minimum height 48px, horizontal padding `space-lg`, font `label-lg`. Active hover state shifts to `#085F51`. Minimum touch bounding box is 48px x 48px.
- **Secondary Authority Button**: Outlined 1.5px `#0F2D37`, background transparent, text `#0F2D37`. Transitions to `#0F2D37` background with `#FFFFFF` text under active interaction.
- **Critical Action Button**: Background `#DC2626`, text `#FFFFFF`. Reserved strictly for cold-chain excursions, quarantined lot rejections, or emergency dispatches.

### Input Fields & Selectors
- **Text Inputs**: Height 48px, `#FFFFFF` fill, 1px border `#B9DBD4`, 8px corner radius. Floating labels stay pinned at `label-md` (`#0F2D37`) on focus with an active primary accent ring: `0 0 0 3px rgba(11, 123, 105, 0.18)` and border `#0B7B69`.
- **Validation Messages**: Placed directly below the field in `body-sm`, accompanied by 16px status icons in `#DC2626` (error) or `#16A34A` (valid).

### Checkboxes & Radios
- Bounded touch targets are 44px minimum with visual controls sized at 20px x 20px. 
- Checked state uses `#0B7B69` background with a crisp white tick mark. Focus indicators display a high-contrast ring for accessible hardware navigation.

### Multilingual Badges & Script Selectors
- **Language Switcher**: Segmented pill control resting in `#E6F2F0` with options formatted as `English | मराठी | हिन्दी`. The selected state features a crisp white floating pill surface with bold `#0F2D37` text and subtle elevation.
- **Status Chips**: Height 26px, padding 4px 10px, border radius 9999px. Composed of a soft 12% opacity tint of the respective status color with high-contrast text (`#16A34A` for normal storage, `#D97706` for stock alert, `#DC2626` for compromised batch).

### Clinical Cards & Data Modules
- Pure white container with 1px border `#D1E5E1`, 12px radius, and internal padding of `space-md` (mobile) to `space-lg` (desktop).
- Header zones partition batch identification, local script translation, and real-time telemetry into distinct, non-overlapping visual clusters.

### Additional Logistics Components
- **Cold-Chain Telemetry Pill**: Compact status tracker displaying current temperature, sensor synchronization delta, and permissible threshold ranges.
- **Batch Verification Banner**: Top-anchored alert strip indicating batch verification integrity, chain-of-custody handoffs, and digital authority stamps.