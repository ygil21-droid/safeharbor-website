# SafeHarbor Investors Group — Website Project

## Project Overview
This is the public-facing website for **SafeHarbor Investors Group**, a U.S.-based real estate investment fund focused on hotel-to-multifamily adaptive reuse and workforce housing. The site targets accredited investors (HNI, family offices) and capital brokers — it should communicate trust, sophistication, and institutional credibility.

**Built by:** Gil Cnaani-Yanushevsky (COO & Head of IR)
**Status:** HTML pages coded and designed, ready for refinement and deployment to Wix

## Company Context
- **Company:** SafeHarbor Investors Group (always one word: SafeHarbor)
- **Structure:** U.S. C-Corp real estate investment fund, co-owned equally by Gil, Amnon, and Nir
- **Focus:** Hotel-to-multifamily adaptive reuse, workforce housing
- **Operating Partner:** GoodHomes Communities
- **Investors:** Mix of Israeli HNI/family office LPs and U.S. LPs
- **Offices:**
  - US: 45 Rockefeller Plaza FL.20, New York, NY 10111
  - IL: Yad Harutzim 2, Netanya, Israel

## Design System

### Fonts
- **Headings:** Libre Baskerville (serif) — elegant, institutional
- **Body:** Barlow (sans-serif) — clean, modern
- **Labels/Tags:** Barlow Condensed — uppercase, letterspaced for section tags and nav

### Colors
| Token | Hex | Usage |
|-------|-----|-------|
| Navy (dark) | `#0F2244` | Hero overlays, dark sections, CTA backgrounds |
| Navy (brand) | `#1B3A6B` | Nav bar, headings, primary text |
| Gold | `#F2C849` | Accent, CTAs, section tags, gold lines |
| Gold (light) | `#F5D76E` | Italic headline accent |
| White | `#FFFFFF` | Page backgrounds, card backgrounds |
| Light gray | `#F7F8FA` | Alternating section backgrounds |
| Text body | `#4A4A4A` | Body paragraphs |
| Text dark | `#1A1A1A` | Strong body text |
| Muted | `rgba(255,255,255,0.45-0.62)` | Muted text on dark backgrounds |

### Design Patterns
- **Section tags:** Barlow Condensed, 11px, weight 600, letter-spacing 0.2em, uppercase, gold color
- **Gold accent line:** 40-48px wide, 1px height, `#F2C849`, used as divider below headings
- **Container:** `max-width: 960px` (or 1080px on portfolio/team), centered, 28px padding
- **Nav height:** 72px, fixed position, navy background on inner pages, transparent-to-navy on homepage
- **Nav links:** Barlow Condensed, 13px, uppercase, letterspaced — active page gets white text + gold underline
- **CTAs:** Gold background (`#F2C849`) with navy text, or transparent with white border
- **Footer:** Dark navy (`#0A1628`), compact, addresses + legal disclaimer + copyright

### Visual Style
- Clean, minimal, white space
- Understated elegance — investment fund aesthetic, not flashy
- No bullet points in presentation copy — small paragraphs
- Alternating white/dark navy sections for visual rhythm
- Subtle textures (diagonal lines on dark sections)
- No emojis anywhere on the site

## Site Structure

### Pages

#### 1. Home (`index.html`)
- **Hero:** Full-viewport, Groton interior background, gradient overlay, headline "Where Others Build New, *We Convert Smart.*"
- **Floating stat cards:** 4 cards overlapping hero/white seam — 20 Projects, 3,200+ Units, $400M+ Portfolio, 35%+ Avg IRR
- **Investment Approach section:** Strategy preview with gold accent line
- **Supply/Demand section:** Housing crisis stats (7M unit deficit, workforce housing need)
- **Portfolio preview:** Property thumbnails with CTA to portfolio page
- **CTA section + Footer**

#### 2. Strategy (`strategy.html`)
- **Hero:** Navy background, "Built on Basis. *Driven by Execution.*"
- **The Opportunity:** Two converging crises — housing deficit + distressed hotels (38% and 97% stats)
- **How We Invest:** 4-pillar grid (Acquire Below Basis, Entitle Before Closing, Convert Don't Build, Operate and Hold)
- **Why It Works:** Speed, Capital Efficiency, Demand Visibility, Regulatory Tailwind
- **CTA + Footer**

#### 3. Portfolio (`portfolio.html`)
- **Summary stats bar:** 19 Projects, 3,223 Total Units, $339M Total Capital, 35.5% Avg IRR
- **Project cards grid:** Each card shows property photo, project name, city/state, units, IRR, status badge
- **Status badges:** Refinanced (green), Stabilized (gold), Lease-Up (orange), Development (blue), Under Contract (gray)
- **Before/After section** (if applicable)
- **Interactive map embed** from: https://safeharbor-portfolio.vercel.app/

#### 4. Team (`team.html`)
- **Leadership bios:** Amnon Bar-Tur, Nir Yanushevsky, Gil Cnaani-Yanushevsky
- **Operating Principles/Values**
- **Partners/Execution Partners logo grid**
- Fade-in scroll animations

#### 5. Contact (`contact.html`)
- **Contact form:** First Name, Last Name, Email, Phone, Interest dropdown, Message
- **Office addresses** (NY + Israel)
- **Accredited investors only** note

#### 6. Investor Login (planned)
- Link to Agora Portal (external)
- "For accredited investors only"

## File Structure
```
website/
├── CLAUDE.md              ← this file
├── index.html             ← Home page
├── strategy.html          ← Strategy page
├── portfolio.html         ← Portfolio page
├── team.html              ← Team page
├── contact.html           ← Contact page
├── logos/                  ← Brand assets + property photos
│   ├── logo-white-cropped.png
│   ├── logo-color-cropped.png
│   ├── SAFEHARBOR INVESTOR GROUP LOGO COLOR.png
│   ├── SAFEHARBOR INVESTOR GROUP LOGO WHITE.png
│   ├── groton-interior.jpg
│   ├── dylan-aerial.png
│   ├── dylan-entrance.jpg
│   ├── bordeaux-interior.jpg
│   ├── groton-before.jpg
│   ├── groton-before-ext.jpg
│   ├── baltimore.jpg
│   ├── burlington.jpg
│   ├── detroit.jpg
│   ├── elpaso.jpg
│   ├── fayetteville.jpg
│   ├── sanantonio.webp
│   └── (base64 text files for logo embedding)
└── design-ideas/          ← Design exploration & iteration archive
    ├── SafeHarbor-Website-Project-Brief.md
    ├── safeharbor-mockup.html         ← original approved mockup
    ├── safeharbor-preview.html        ← full preview build
    ├── safeharbor-website.jsx         ← React reference (not used)
    ├── homepage-v2.html               ← homepage iteration
    ├── portfolio-v1.html              ← portfolio iteration
    ├── strategy-v1.html               ← strategy iteration
    ├── *-comparison.html              ← side-by-side design comparisons
    └── modal-*.html                   ← modal/panel design explorations
```

## Portfolio Data (19 Projects)

| Project | City | Units | IRR | Status |
|---|---|---|---|---|
| Burlington | Burlington, NC | 135 | 45.5% | Leasing Active |
| Chattanooga | Ringgold, GA | 104 | 43.1% | Leasing Active |
| Cedar Creek | Fayetteville, NC | 201 | 42.6% | Stabilized |
| Bordeaux | Fayetteville, NC | 255 | 42.6% | Leasing Active |
| Detroit | Detroit, MI | 128 | 42.6% | Leasing Active |
| Erie | Erie, PA | 197 | 40.0% | Leasing Active |
| Dallas I | Dallas, TX | 142 | 40.0% | In Renovation |
| Downtown San Antonio | San Antonio, TX | 220 | 39.4% | In Renovation |
| Silver Spring | Silver Spring, MD | 227 | 39.2% | In Renovation |
| Groton | Groton, CT | 112 | 36.0% | Stabilized |
| Dallas II | Dallas, TX | 103 | 35.2% | In Renovation |
| Warwick | Warwick, RI | 238 | 32.5% | Leasing Active |
| Columbia (The Dylan) | Columbia, SC | 146 | 31.8% | In Renovation |
| Lakewood | Lakewood, CO | 147 | 30.5% | Pre-Construction |
| Tucson (Escalante) | Tucson, AZ | 100 | 29.1% | In Renovation |
| Norfolk (Days Inn) | Norfolk, VA | 160 | 27.0% | Pre-Construction |
| Arlington (Court Suites) | Arlington, TX | 187 | 26.9% | Pre-Construction |
| Valor Hill | San Antonio, TX | 118 | 26.6% | Leasing Active |
| Baltimore | Baltimore, MD | 303 | 24.2% | In Renovation |

**Totals:** 19 Projects | 3,223 Units | $339M Total Capital | 35.5% Avg IRR
**Breakdown:** Stabilized: 2 | Leasing Active: 7 | In Renovation: 7 | Pre-Construction: 3

## Leadership

1. **Amnon Bar-Tur, Principal** — Co-founded BaseCamp Student (acquired for $1B by Xior in 2022). Extensive experience across acquisitions, asset management, value-driven strategies in international markets.

2. **Nir Yanushevsky, Principal** — CEO of Yanushevsky Group (est. 1946), 20+ years experience, 1,000+ residential units in Tel Aviv. Former VP & Chairman of Israeli Builders Association.

3. **Gil Cnaani-Yanushevsky, Principal & Head of Investor Relations** — BA Psychology & Communications, MA Marketing, MBA from Tel Aviv University (honors). Former Deloitte. Marketing, business development, brand positioning.

## Key Stats (used across pages)
- $400M+ Portfolio value
- 3,200+ Units (or 3,223 exact)
- 20 Projects (or 19 exact, depending on pipeline)
- $104M+ Equity Raised
- 35%+ Average IRR
- 17+ years combined experience

## Data Sources
- **Portfolio Dashboard:** https://safeharbor-portfolio.vercel.app/
- **Content Doc:** Google Doc ID: 15gK_eHCOsFzJFRjAL9bpsK9p7r226jLuEgEgdvNuZPU

## Deployment Plan
- **Target platform:** Wix (drag-and-drop or Wix Studio)
- **Alternative:** Static HTML hosted on Netlify/Vercel
- **Investor Login:** Links to external Agora Portal
- **Contact Form:** Wix form or Calendly integration
- **Interactive Map:** Embed from safeharbor-portfolio.vercel.app

## Style Rules
- Company name always: **SafeHarbor** (one word, this capitalization)
- No bullet points in presentation copy — small paragraphs
- Currency formatted as $400M+ / $104M+ / $339M
- No emojis on the site
- Tone: institutional, confident, understated — not salesy
- Legal disclaimer required in footer on every page
