# LoanMate Brand & Design System Guidelines

*Authoritative design tokens, typography, component specs, color palette, and interaction models for the LoanMate NBFC platform.*

---

## 🎨 1. Color Palette Tokens

| Token Name | Hex Code | Purpose | Usage Guidelines |
|---|---|---|---|
| `--accent` | `#ea580c` | Primary Dark Orange Accent | CTAs, active radio dots, progress step fill, primary links |
| `--accent-hover` | `#c2410c` | Dark Orange Hover State | Hover states on primary buttons & pills |
| `--accent-light` | `#fff7ed` | Warm Tint Background | Selected option cards, soft highlighted containers |
| `--surface` | `#ffffff` | Primary Surface Card | Main content cards, form inputs, active option cards |
| `--surface-subtle` | `#f6f4ef` | Sand/Beige Tint Surface | Left stepper sidebar, container backgrounds |
| `--text-primary` | `#1c1917` / `#0f172a` | Primary Heading Text | Headlines, titles, option card titles |
| `--text-secondary` | `#57534e` / `#475569` | Subtitles & Body | Explanatory hints, step labels, body text |
| `--text-muted` | `#78716c` / `#64748b` | Muted & Footnotes | Eyebrows, timestamps, disclaimers |
| `--border` | `#e7e5e4` | Standard Border | Unselected option card borders, field outlines |

> [!IMPORTANT]
> **No Green Option Badges / Banner Overlays**: The primary brand identity is **Dark Orange (`#ea580c`)**. Green is reserved strictly for subtle SSL security badges and must never override option card backgrounds or stepper circles.

---

## 🔤 2. Typography Hierarchy & System

To ensure 100% visual harmony across all screens, LoanMate uses a unified, modern typeface system powered by **Inter**:

### Typeface:
- **Primary Typeface**: `Inter` (weights: 400, 500, 600, 700, 800, 900)
- Used consistently for: Hero titles, section headings, question labels, body copy, navigation links, form controls, option titles & descriptions, stepper text, and CTA buttons.

### Typography Scale:
- **Hero Giant Title**: `font-family: 'Inter', sans-serif; font-size: clamp(42px, 5.2vw, 66px); font-weight: 900; letter-spacing: -2px; line-height: 1.05;`
- **Section Heading (H2)**: `font-family: 'Inter', sans-serif; font-size: 28px; font-weight: 800; color: #1c1917; letter-spacing: -0.5px;`
- **Sidebar Heading**: `font-family: 'Inter', sans-serif; font-size: 26px; font-weight: 800; color: #1c1917; letter-spacing: -0.5px;`
- **Eyebrow / Kicker**: `font-family: 'Inter', sans-serif; font-size: 11px-12px; font-weight: 700; letter-spacing: 1.2px - 1.4px; text-transform: uppercase; color: var(--accent);`
- **Option Card Title**: `font-family: 'Inter', sans-serif; font-size: 16px; font-weight: 700; color: #1c1917;`
- **Option Card Subtitle**: `font-family: 'Inter', sans-serif; font-size: 13.5px; font-weight: 400; color: #78716c;`
- **Body / Subtext**: `font-family: 'Inter', sans-serif; font-size: 15px; color: #78716c; line-height: 1.5;`

---

## 📋 3. Form & Wizard Interaction Guidelines

### Progressive Vertical Unfolding (No Back/Continue Buttons):
1. **Sequential Unveiling**:
   - Step 1 (`How much do you need to borrow?`) is unlocked initially.
   - Selecting an option in Step `Q` highlights the option card, updates the sidebar stepper, and **smoothly unveils Question `Q+1` below it**, automatically scrolling down to focus on `Q+1`.
   - All answered questions remain visible and selectable in the vertical stack.
2. **Option Card Styling**:
   - 2-column grid layout (`22px 24px` padding, `14px` border-radius).
   - Right-aligned radio circle (`20px`).
   - Active state: `border: 2px solid #ea580c; background: #fff7ed;` with filled orange dot inside radio circle.
3. **Hidden Loan Estimate Rule**:
   - Indicative loan range (`sidebar-total`) is **completely hidden (`display: none;`)** while answering questions 1 to 5.
   - It is calculated and displayed **ONLY after all 5 questions are answered and the user submits by clicking `"Check Eligibility →"`**.
4. **Sidebar Stepper**:
   - Active step: Filled dark orange circle with step number, title, and `"In progress"` tag.
   - Completed steps: Filled dark orange circle with crisp white SVG checkmark (`✓`) and selected value subtitle.

---

## 🛡️ 4. Trust & Security Strip
- Footer strip positioned below main workspace container.
- Divider pipe `|` separating trust points: `Secure & trusted | Backed by leading financial institutions | Your data is always safe with us`.
- Contact hotline link on right side: `Have questions? Contact Support`.
