---
name: Financial Heritage RPN
colors:
  surface: '#061426'
  surface-dim: '#061426'
  surface-bright: '#2d3a4e'
  surface-container-lowest: '#020e21'
  surface-container-low: '#0e1c2f'
  surface-container: '#132033'
  surface-container-high: '#1d2a3e'
  surface-container-highest: '#28354a'
  on-surface: '#d6e3fe'
  on-surface-variant: '#bdcabf'
  inverse-surface: '#d6e3fe'
  inverse-on-surface: '#243145'
  outline: '#88948a'
  outline-variant: '#3e4941'
  surface-tint: '#77daa4'
  primary: '#77daa4'
  on-primary: '#003921'
  primary-container: '#3ea271'
  on-primary-container: '#00311c'
  inverse-primary: '#006d44'
  secondary: '#e9c349'
  on-secondary: '#3c2f00'
  secondary-container: '#af8d11'
  on-secondary-container: '#342800'
  tertiary: '#7bd0ff'
  on-tertiary: '#00354a'
  tertiary-container: '#009bd1'
  on-tertiary-container: '#002d40'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#93f7be'
  primary-fixed-dim: '#77daa4'
  on-primary-fixed: '#002111'
  on-primary-fixed-variant: '#005232'
  secondary-fixed: '#ffe088'
  secondary-fixed-dim: '#e9c349'
  on-secondary-fixed: '#241a00'
  on-secondary-fixed-variant: '#574500'
  tertiary-fixed: '#c4e7ff'
  tertiary-fixed-dim: '#7bd0ff'
  on-tertiary-fixed: '#001e2c'
  on-tertiary-fixed-variant: '#004c69'
  background: '#061426'
  on-background: '#d6e3fe'
  surface-variant: '#28354a'
  navy-deep: '#0B192C'
  navy-body: '#132743'
  navy-ops: '#1E3A5F'
  gold-shift-f: '#D4AF37'
  gold-stack: '#F3D98B'
  blue-shift-g: '#38BDF8'
  blue-shift-alt: '#5BA4E6'
  blue-shift-border: '#7DD3FC'
  green-enter: '#1F8A5B'
  green-enter-border: '#166944'
  lcd-background: '#E8EFEA'
  lcd-digits: '#0B192C'
  slate-border: '#E2E8F0'
  surface-light: '#FFFFFF'
  surface-muted: '#F8FAFC'
  text-muted: '#64748B'
  tab-inactive: '#94A3B8'
typography:
  display-lcd:
    fontFamily: JetBrains Mono
    fontSize: 30px
    fontWeight: '800'
    lineHeight: 38px
    letterSpacing: -0.5px
  display-lcd-mobile:
    fontFamily: JetBrains Mono
    fontSize: 26px
    fontWeight: '800'
    lineHeight: 32px
    letterSpacing: -0.5px
  headline-card:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '800'
    lineHeight: 22px
    letterSpacing: 0.3px
  headline-modal:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '700'
    lineHeight: 20px
  key-primary:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '700'
    lineHeight: 16px
  key-shift-f:
    fontFamily: Inter
    fontSize: 9px
    fontWeight: '800'
    lineHeight: 12px
    letterSpacing: 0.5px
  key-shift-g:
    fontFamily: Inter
    fontSize: 9px
    fontWeight: '700'
    lineHeight: 12px
    letterSpacing: 0.5px
  body-default:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '500'
    lineHeight: 18px
  body-tabular:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 18px
  data-table:
    fontFamily: JetBrains Mono
    fontSize: 11px
    fontWeight: '400'
    lineHeight: 16px
  meta-lcd:
    fontFamily: JetBrains Mono
    fontSize: 10px
    fontWeight: '700'
    lineHeight: 14px
    letterSpacing: 0.4px
  caption-label:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '600'
    lineHeight: 14px
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  gutter: 0.375rem
  gutter-desktop: 0.75rem
  margin: 0.75rem
  margin-mobile: 0.5rem
  space-xs: 0.25rem
  space-sm: 0.375rem
  space-md: 0.625rem
  space-lg: 0.875rem
  space-xl: 1.25rem
---

## Brand & Style

This design system translates the physical heritage and mathematical rigor of classical reverse polish notation (RPN) financial calculators into a modern, tactile, and institutional interface. It balances high-trust investment banking sobriety with the direct tactile ergonomics of physical financial hardware.

The design movement combines **Tactile Skeuomorphism** with **Modern Institutional Minimalism**:
- **Hardware-Informed Tactility:** Beveled keycaps with physical depress mechanics (`translateY(1px)` and elimination of bottom rim drop-shadows on active states), dual-level shift indicator labelling, and a high-contrast segmented LCD housing.
- **Institutional Sophistication:** Deep sovereign navy foundations anchored by brass-gold accentuation for structural divides and primary shift tiers (`f`), sky blue for secondary operations (`g`), and emerald green for transaction confirmation (`ENTER`).
- **Target Audience:** Fixed-income analysts, wealth managers, CFOs, actuarial auditors, and financial engineering students who require instant offline calculation velocity, auditable calculation logs, and publication-ready amortization schedules.
- **Emotional Intent:** Absolute computational trust, tactile speed, zero latency, and analytical prestige.

## Colors

The system uses a dark institutional architecture with specialized chromatic surfaces for hardware emulation and audit exports:

- **Deep Surfaces (`#0B192C`, `#132743`):** The app chassis, navigation headers, and base numeric keycaps use deep navy values rather than neutral black, preserving an authoritative banking environment.
- **Functional Shift Tiers:**
  - **Gold Shift (`#D4AF37` / `#F3D98B`):** Reserved strictly for primary `f` shift execution, top-tier keycap annotations (`PRICE`, `YTM`, `SL`, `SOYD`, `DB`, `AMORT`), stack inspection indicators, and corporate branding indicators.
  - **Sky Shift (`#38BDF8` / `#5BA4E6`):** Dedicated exclusively to secondary `g` shift execution and bottom-tier keycap annotations (`DATE`, `ΔDYS`, `D.MY`, `M.DY`, `BEG`, `END`).
- **Tactile Affirmation (`#1F8A5B`):** The `ENTER` key and export executions use emerald green, backed by an anchoring darker stroke (`#166944`) to convey closure and commitment.
- **Hardware LCD Core (`#E8EFEA` / `#D8E2DC`):** The display chamber uses a physical optic LCD green-tinted off-white with `#0B192C` high-density matrix digits, delivering over 10:1 contrast for rapid legibility under direct ambient lighting.
- **Export & Audit Documents:** Inversion to `#FFFFFF` and `#F8FAFC` slate cards for formal reporting, print, and WhatsApp/PDF compliance output.

## Typography

Typography governs the separation between interactive control surfaces and numerical computing pipelines:

- **Monospace Stack (`JetBrains Mono`):** Applied strictly to the LCD display screen, the 4-register RPN stack peek (`X`, `Y`, `Z`, `T`, `LSTx`), data tables (amortization and depreciation ledgers), and computation memory reasoning blocks. Tabular figures (`font-variant-numeric: tabular-nums`) must be enforced globally on all monospace instances to guarantee decimal point alignment across thousands of calculation rows.
- **Interface Stack (`Inter`):** Powers keycap physical labels, shift indicators, module headers, navigation tabs, and system forms. 
- **Scale Hierarchy:**
  - Shift functions (`key-shift-f` and `key-shift-g`) sit at an ultra-compact `9px` with bold weights and expanded tracking (`+0.5px`) to preserve optical legibility above and below primary key labels without crowding the touch target.
  - The LCD output utilizes an authoritative `30px` (reflowing to `26px` on compact screens) with minimum line-height to maximize vertical footprint inside the bezel.

## Layout & Spacing

The layout model is split into two primary view modes:

1. **Hardware Calculator Shell:** Strictly locked to a centered fixed width (`max-width: 480px` on mobile/portrait; up to `640px` in landscape) to replicate the hand-held balance of a physical 12C. Outer margins remain minimal (`0.5rem` to `0.75rem`).
2. **Analysis Panels & Schedules:** Inside secondary tabs (Cash Flow, Depreciation, Amortization), tabular structures stretch across full available containers with structured horizontally scrollable viewports.

Keypad spacing requires high-density micro-rhythms:
- **Key Matrix:** Organized on a continuous CSS Grid (typically 5 columns). Gaps between keys are fixed to `space-sm` (`6px` / `0.375rem`) with zero outer flex leakage, guaranteeing touch targets meet the Android standard minimum of `44px` height.
- **Component Padding Rhythm:** Form inputs use `space-md` (`10px`), card boundaries scale between `space-lg` (`14px`) and `space-xl` (`20px`), while internal register stack indicators use condensed `space-xs` padding.

## Elevation & Depth

Visual hierarchy is constructed through physical hardware mechanics rather than diffuse multi-layered lighting:

- **Chassis Level (0DP):** The baseline frame rests on `#0B192C` surrounded by an ambient viewport shadow of `0 12px 40px rgba(11, 25, 44, 0.28)` when placed against neutral desktop backgrounds.
- **Recessed LCD Well (-1DP):** The LCD bezel is inset using an interior bezel border of `2px solid #D4AF37` and an inner shadow simulation, isolating the pale `#E8EFEA` screen as a physically mounted component beneath the housing.
- **Tactile Keycaps (+1DP to +2DP):**
  - **Rest State:** Keys have a physical bottom ridge generated by a solid 2px drop-edge: `box-shadow: 0 2px 0 #050C17`. Borders are 1px solid `#1E3A5F` for neutral keys and `#166944` for the `ENTER` key.
  - **Depressed State (`:active`):** The bottom shadow is instantly collapsed (`box-shadow: 0 0 0 transparent`), and the key body translates down: `transform: translateY(2px)`. This micro-mechanic delivers zero-latency haptic visual feedback essential for RPN rapid data entry.
- **Modal Sheets (+3DP):** Calculations and audit memory dialogs utilize a high-density navy scrim `rgba(11, 25, 44, 0.85)` with a solid `#0B192C` dialog border of `2px solid #D4AF37`.

## Shapes

The shape system adopts a **Soft Geometric** profile (`roundedness: 1`), staying faithful to precision instruments:

- **Keycaps:** `border-radius: 0.375rem` (`6px`). Sharp enough to maintain rectangular visual discipline and maximize touchable surface area, yet micro-radiused to prevent visual hardness.
- **LCD Bezel & Panels:** `border-radius: 0.5rem` (`8px`). Distinguishes the optical display lens from the keys below.
- **Utility Action Pills:** `border-radius: 9999px` (Full Pill) for header tools like the Google Finance shortcut and fast export buttons, visually detaching quick-launcher actions from the functional calculator keys.
- **System Modals & Data Cards:** `border-radius: 0.75rem` (`12px`) for export memory containers and amortization data cards.

## Components

### 1. The RPN Keycap (`key-btn`)
- **Structure:** Vertical flex container containing three stacked rows:
  1. Top label: Gold (`#D4AF37`), `9px`, `font-weight: 800` (e.g., `PV`, `FV`, `AMORT`).
  2. Center label: Crisp White (`#FFFFFF`), `13px`–`14px`, `font-weight: 700` (Main keycap value or digit).
  3. Bottom label: Sky Blue (`#38BDF8`), `9px`, `font-weight: 700` (e.g., `BEGIN`, `DATE`, `ΔDYS`).
- **Variants:**
  - *Standard Numeric (0-9, .):* Background `#132743`, border `1px solid #1E3A5F`.
  - *Financial & Math Ops:* Background `#1E3A5F`, border `1px solid #2B4E7A`.
  - *Shift f:* Background `#D4AF37`, text `#0B192C`, border `1px solid #F3D98B`.
  - *Shift g:* Background `#38BDF8`, text `#0B192C`, border `1px solid #7DD3FC`.
  - *ENTER:* Double-height or double-width format, background `#1F8A5B`, text `#FFFFFF`, border `1px solid #166944`.
- **States:** `:active` must invoke `translateY(1px)` and remove bottom tactile shadow.

### 2. The LCD Display Unit
- **Chassis:** Background `#E8EFEA`, border `2px solid #D4AF37`, inner padding `10px 14px`.
- **Sub-elements:**
  - *Status Flags Row:* Monospace 10px `#0B192C` indicators: `f`, `g`, `BEGIN`, `RAD`, `D.MY`, `PRGM`. Active indicators are black; inactive indicators are rendered with 8% opacity to simulate idle LCD crystals.
  - *Numeric Readout:* Right-aligned, `JetBrains Mono` 30px bold, tabular numbers with distinct comma/decimal separation.
  - *RPN Stack Peek Bar:* Slim top drawer displaying `Y: 1,240.50 | Z: 0.00` in `#0B192C` with 60% opacity.

### 3. Data & Amortization Tables
- **Header:** Sticky `#0B192C` background, `#D4AF37` bold uppercase labels, height `36px`, border-bottom `2px solid #D4AF37`.
- **Cells:** Alternating rows (`#0B192C` and `#132743` in dark mode; `#FFFFFF` and `#F8FAFC` in exported sheets), padding `6px 8px`, `font-family: JetBrains Mono`, text right-aligned for currency and quantities, left-aligned for period numbers (`n`).

### 4. Audit & Calculation Memory Modal ("Fita de Auditoria")
- **Header:** Deep navy with gold brand text `@diarioc8` and clear dismiss trigger (`✕`).
- **Reasoning Box (`reasoning-box`):** Background `#F8FAFC`, border `1px solid #E2E8F0`, padding `12px`. Displays the sequential RPN execution pipeline (e.g., `10000 [ENTER] 12 [n] 1.5 [i] [PMT]`).
- **Export Toolbar:** Four-button distribution containing Native Android Share, Download PDF/PNG, Download CSV/TXT, and Copy Formatted Text to clipboard. Primary export action highlighted in `#1F8A5B`.

### 5. Input Groups & Selectors
- **Form Fields:** Dark navy inputs (`#132743`) with `1.5px solid #1E3A5F` borders, active focus ring `1.5px solid #D4AF37`. Label text placed above in `#94A3B8`, `11px` bold.