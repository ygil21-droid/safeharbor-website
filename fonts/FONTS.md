# SafeHarbor Website — Typography System

Complete documentation of all fonts used across the SafeHarbor Investors Group website, including sizes, weights, usage, and CSS specifications.

---

## 📚 Font Stack Overview

| Font | Type | Source | Usage |
|------|------|--------|-------|
| **Libre Baskerville** | Serif | Google Fonts | Headings (h1–h4), elegant & institutional |
| **Barlow** | Sans-serif | Google Fonts | Body text, paragraphs, primary content |
| **Barlow Condensed** | Sans-serif | Google Fonts | Labels, tags, nav links, UI elements |

---

## 🔗 Font Import (CSS)

All fonts are imported from **Google Fonts CDN**. Include this in your HTML `<head>`:

```html
<link href="https://fonts.googleapis.com/css2?family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&family=Barlow:wght@300;400;500;600&family=Barlow+Condensed:wght@400;500;600&display=swap" rel="stylesheet">
```

Or via CSS `@import`:

```css
@import url('https://fonts.googleapis.com/css2?family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&family=Barlow:wght@300;400;500;600&family=Barlow+Condensed:wght@400;500;600&display=swap');
```

---

## 1️⃣ Libre Baskerville (Serif)

**Purpose:** Headings, institutional elegance, trust & sophistication

### Available Weights
- **400** — Regular
- **700** — Bold
- **400 Italic** — Italic (used for accent text in headlines)

### Font Sizes & Usage

| Element | Size | Weight | Line Height | Letter Spacing | Usage |
|---------|------|--------|-------------|----------------|-------|
| **H1 – Hero Heading** | 56px | 400 | 1.15 | -0.02em | Homepage hero, main section titles |
| **H1 – Mobile** | 32px | 400 | 1.15 | -0.02em | Hero heading on tablets & phones |
| **H2 – Section Heading** | 36px | 400 | 1.4 | -0.01em | Major section headings |
| **H2 – Mobile** | 28px | 400 | 1.4 | -0.01em | Mobile section headings |
| **H3 – Subsection** | 26px | 400 | 1.3 | normal | Subsection headings, card titles |
| **H4 – Label** | 20px | 700 | 1.4 | normal | Strong labels, step titles |
| **Italic Accent** | 28–48px | 400 | varies | normal | Italic text in headlines (e.g., "Where Others Build New. *We Convert Smart.*") |
| **Small Heading** | 18px | 700 | 1.5 | normal | Card titles, project names |

### CSS Classes & Examples

```css
h1, h2, h3, h4 { 
  font-family: 'Libre Baskerville', serif; 
}

/* Hero heading */
.hero-heading {
  font-size: 56px;
  font-weight: 400;
  line-height: 1.15;
  letter-spacing: -0.02em;
}

/* Italic accent (in headline) */
h1 em {
  font-style: italic;
  font-weight: 400;
}

/* Mobile adjustment */
@media (max-width: 768px) {
  .hero-heading { font-size: 32px; }
  h2 { font-size: 28px; }
}
```

### Visual Examples

```
We Convert Smart,
Where Others Build New.
↑ H1 + italic accent, 56px, gold accent color
```

---

## 2️⃣ Barlow (Sans-Serif)

**Purpose:** Body text, paragraphs, primary content, readable at all sizes

### Available Weights
- **300** — Light (rarely used, emphasis reduction)
- **400** — Regular (default body text)
- **500** — Medium (slightly stronger emphasis)
- **600** — Semibold (strong emphasis, call-outs)

### Font Sizes & Usage

| Element | Size | Weight | Line Height | Letter Spacing | Usage |
|---------|------|--------|-------------|----------------|-------|
| **Body Copy** | 16–18px | 400 | 1.55–1.6 | normal | Paragraphs, main content |
| **Body Copy Large** | 20px | 400 | 1.55 | normal | Featured paragraphs, introductions |
| **Body Copy Small** | 14–15px | 400 | 1.5–1.6 | normal | Secondary text, captions, footnotes |
| **Emphasis** | 18–20px | 500 | 1.55 | normal | Slightly bolder paragraphs |
| **Strong Emphasis** | 16–18px | 600 | 1.55 | normal | Call-outs, highlights, strong points |
| **Form Labels** | 14px | 600 | 1.5 | normal | Input labels, form text |
| **Stat Numbers (Desktop)** | 54px | 700 | 1 | normal | Large portfolio stats |
| **Stat Numbers (Mobile)** | 54px | 700 | 1 | normal | Same size on all screens |

### CSS Classes & Examples

```css
body {
  font-family: 'Barlow', sans-serif;
  font-weight: 400;
  font-size: 16px;
  line-height: 1.6;
  color: #4A4A4A;
}

/* Large body text */
p.intro {
  font-size: 20px;
  font-weight: 400;
  line-height: 1.55;
}

/* Emphasis */
strong, .emphasis {
  font-weight: 600;
}

/* Light text (de-emphasis) */
.muted {
  font-weight: 300;
  color: #888;
}

/* Form labels */
label {
  font-family: 'Barlow', sans-serif;
  font-size: 14px;
  font-weight: 600;
}

/* Mobile body text */
@media (max-width: 768px) {
  body { font-size: 15px; }
  p.intro { font-size: 18px; }
}
```

### Visual Examples

```
We acquire distressed hotels and convert them into 
modern, affordable apartments, creating value for 
investors and housing for America's workforce.
↑ Body text, 20px, 400 weight, 1.55 line-height
```

---

## 3️⃣ Barlow Condensed (Sans-Serif)

**Purpose:** Labels, tags, navigation, uppercase UI elements

### Available Weights
- **400** — Regular
- **500** — Medium
- **600** — Semibold (primary, most used)

### Font Sizes & Usage

| Element | Size | Weight | Letter Spacing | Text Transform | Usage |
|---------|------|--------|-----------------|-----------------|-------|
| **Section Tag** | 11–13px | 600 | 0.22em | uppercase | "Investment Strategy", "Our Portfolio" |
| **Nav Link** | 13–14px | 600 | 0.14em | uppercase | Navigation menu items |
| **Button Label** | 12–13px | 600 | 0.12em | uppercase | CTA buttons |
| **Badge Label** | 12px | 600 | 0.08em | uppercase | Status badges |
| **Form Label** | 11px | 600 | 0.16em | uppercase | Form field labels |
| **Footer Text** | 12px | 600 | normal | uppercase | Footer links & copyright |

### CSS Classes & Examples

```css
/* Section tag (above headings) */
.section-tag {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: #F2C849;
}

/* Nav links */
.nav-link {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 13px;
  font-weight: 600;
  letter-spacing: 0.14em;
  text-transform: uppercase;
}

/* Button labels */
.btn {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 13px;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
}

/* Badge */
.badge {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}
```

### Visual Examples

```
OUR INVESTMENT APPROACH
↑ Section tag, 11px, 600 weight, 0.22em letter-spacing

LEARN MORE →
↑ Button, 13px, 600 weight, 0.12em letter-spacing
```

---

## 🎯 Comprehensive Typography Hierarchy

### Desktop

```
H1 (Hero)         56px / Libre Baskerville / 400
├─ Italic Accent  48px / Libre Baskerville / 400 italic
│
H2 (Section)      36px / Libre Baskerville / 400
├─ Section Tag    11px / Barlow Condensed / 600
│
H3 (Subsection)   26px / Libre Baskerville / 400
│
Body Large        20px / Barlow / 400
├─ Body Normal    16px / Barlow / 400
└─ Body Small     14px / Barlow / 400
  │
  ├─ Emphasis     18px / Barlow / 600
  ├─ Muted        14px / Barlow / 300
  └─ Form Label   14px / Barlow / 600
│
Labels & Tags     11–13px / Barlow Condensed / 600
├─ Nav Links      13px / Barlow Condensed / 600
├─ Buttons        13px / Barlow Condensed / 600
└─ Badges         12px / Barlow Condensed / 600
```

### Mobile

```
H1 (Hero)         32px / Libre Baskerville / 400
H2 (Section)      28px / Libre Baskerville / 400
H3 (Subsection)   22px / Libre Baskerville / 400
Body              15px / Barlow / 400
Labels            11px / Barlow Condensed / 600
```

---

## 🔧 Implementation Checklist

- [ ] Import Google Fonts in HTML `<head>` or CSS
- [ ] Define base font sizes in `body` selector
- [ ] Set font-family for headings (h1–h4)
- [ ] Apply line-height consistently (1.4–1.6 for body, 1.15–1.3 for headings)
- [ ] Use letter-spacing for uppercase text (0.12em–0.22em)
- [ ] Test readability at all breakpoints (desktop, tablet, mobile)
- [ ] Verify contrast ratios meet WCAG AA standards
- [ ] Optimize font loading (system fonts first, then web fonts)

---

## 📱 Responsive Adjustments

### Tablet (768px and below)
- Reduce H1 from 56px to 32px
- Reduce H2 from 36px to 28px
- Reduce body from 16px to 15px
- Keep letter-spacing consistent

### Mobile (480px and below)
- Hero heading: 26px
- Section heading: 24px
- Body: 14–15px
- Nav font-size: 16px (touch-friendly)
- Stat numbers: Stay at 54px (full size, not reduced)

---

## 🎨 Font Pairing Summary

| Combination | Use Case | Effect |
|---|---|---|
| **Libre Baskerville + Barlow** | Headlines + body text | Elegant, professional, investment-grade |
| **Barlow + Barlow Condensed** | Body + labels | Modern, clean, scannable |
| **All Three Together** | Complete page | Sophisticated, institutional, readable |

---

## ⚙️ Performance Notes

- **Google Fonts CDN:** Fonts are cached globally, no performance penalty
- **Font Loading:** `display=swap` ensures text appears immediately while fonts load
- **Variable Fonts:** Barlow and Barlow Condensed have multiple weights, reducing file size vs. separate files
- **Subset:** Only Latin characters are loaded (default Google Fonts behavior)

---

## 🔄 Font Version & Updates

- **Libre Baskerville:** Latest from Google Fonts
- **Barlow:** Latest from Google Fonts (designed by Jeremy Tribby)
- **Barlow Condensed:** Latest from Google Fonts

To update fonts, modify the Google Fonts import URL in your HTML/CSS.

---

## 📋 Quick Reference Cards

### For Designers
- Serif (headings): **Libre Baskerville** — 400, 700, 400 italic
- Sans-serif (body): **Barlow** — 300, 400, 500, 600
- Sans-serif (labels): **Barlow Condensed** — 400, 500, 600

### For Developers
```html
<link href="https://fonts.googleapis.com/css2?family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&family=Barlow:wght@300;400;500;600&family=Barlow+Condensed:wght@400;500;600&display=swap" rel="stylesheet">
```

### For Copywriters
- **Headlines:** Use Libre Baskerville italic for emphasis (e.g., "Where Others Build New. *We Convert Smart.*")
- **Body:** Clear, scannable paragraphs with Barlow (16–20px)
- **Labels:** All caps with Barlow Condensed (11–13px)

---

**Last Updated:** 2026-05-21
**Maintained By:** Gil / Design Team
