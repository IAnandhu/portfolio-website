# Brand Identity — Anandu Sivan
**Concept Direction: Dark Editorial**
"Dark editorial with monumental type and cinematic negative space. The page feels like a magazine spread, not a portfolio template."

---

## Color System

| Token | Hex | Usage |
|---|---|---|
| `--bg` | `#080808` | Page background |
| `--bg-elevated` | `#111111` | Section alternates |
| `--bg-card` | `#141414` | Cards, surfaces |
| `--bg-card-hover` | `#1A1A1A` | Card hover state |
| `--text-primary` | `#F2F2F2` | Headlines, body |
| `--text-secondary` | `#888888` | Labels, captions, muted |
| `--text-tertiary` | `#444444` | Dividers, placeholder |
| `--accent` | `#E8000D` | Primary accent — red |
| `--accent-dark` | `#A80009` | Hover on accent elements |
| `--border` | `#1C1C1C` | Subtle borders |
| `--border-accent` | `#E8000D` | Accent borders / indicators |

---

## Typography

**Google Fonts import:**
```
https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Syne:wght@600;700;800&family=Outfit:wght@300;400;500;600&display=swap
```

| Role | Font | Size | Weight | Case | Notes |
|---|---|---|---|---|---|
| Display (hero) | Bebas Neue | 14–18vw | 400 | Uppercase | Hero headline only |
| Headline | Syne | 40–64px | 800 | Title | Section headers |
| Subheadline | Syne | 20–28px | 600 | Title | Sub-sections |
| Body | Outfit | 16–18px | 400 | Sentence | Paragraphs |
| Body emphasis | Outfit | 16–18px | 600 | Sentence | Bold within body |
| Label/caption | Outfit | 11–13px | 500 | Uppercase + tracked | Section labels, stats |
| Nav | Outfit | 14px | 500 | Title | Navigation items |
| Button | Outfit | 14–15px | 600 | Uppercase + tracked | CTAs |
| Stat number | Bebas Neue | 48–64px | 400 | Uppercase | Social proof bar |

---

## Spacing Scale (8px grid)

```
4px   — micro gap
8px   — xs
16px  — sm
24px  — md
32px  — lg
48px  — xl
64px  — 2xl
96px  — 3xl
128px — 4xl
```

Section padding: `96px` top/bottom (desktop), `64px` (mobile)

---

## Border Radius

| Element | Radius |
|---|---|
| Cards | `2px` (sharp — editorial aesthetic) |
| Buttons | `2px` |
| Inputs | `2px` |
| Avatar/photo (round) | `50%` |
| Tags/chips | `2px` |

No rounded corners. The reference aesthetic is angular and editorial.

---

## Shadows & Effects

**Accent glow (CTA buttons):**
```css
box-shadow: 0 0 24px rgba(232, 0, 13, 0.35), 0 0 48px rgba(232, 0, 13, 0.15);
```

**Card hover lift:**
```css
box-shadow: 0 20px 60px rgba(0, 0, 0, 0.6);
transform: translateY(-4px);
```

**Hero gradient overlay:**
```css
background: linear-gradient(to right, #080808 40%, transparent 70%);
```

**Noise texture:** Applied via SVG filter or CSS noise pattern at 3–5% opacity on hero.

**Red accent bar:** 3px solid `#E8000D` — used as left-border indicator on active states, section markers, logo mark.

---

## Button Styles

**Primary CTA:**
```css
background: #E8000D;
color: #F2F2F2;
padding: 14px 32px;
letter-spacing: 0.12em;
text-transform: uppercase;
font: 600 14px 'Outfit';
border: none;
box-shadow: 0 0 24px rgba(232, 0, 13, 0.35);
transition: all 0.25s ease;
```
Hover: background → #A80009, glow intensifies.

**Ghost/Secondary:**
```css
background: transparent;
color: #F2F2F2;
border: 1px solid #1C1C1C;
padding: 13px 31px;
```
Hover: border-color → #E8000D, color stays white.

---

## Animation Principles

- **Page load**: Staggered reveal — nav (0ms) → hero text (200ms) → hero image (400ms) → bottom links (600ms)
- **Scroll reveals**: `IntersectionObserver`, fade-up (translateY 30px → 0, opacity 0 → 1), 0.6s ease-out, 100ms stagger between children
- **Hover transitions**: 0.25s ease — fast enough to feel responsive, slow enough to feel considered
- **Smooth scroll**: `scroll-behavior: smooth` on `html`
- **Reduced motion**: All animations disabled when `prefers-reduced-motion: reduce`

---

## Layout Grid

- Max width: `1400px`
- Gutter: `80px` (desktop), `40px` (tablet), `24px` (mobile)
- Column system: 12-column
- Hero: Full bleed (no max-width constraint)
- Works section: 1-column stacked cards (full width)
- Process: 4-column grid (desktop), 2-column (tablet), 1-column (mobile)
- Testimonials: 3-column (desktop), 1-column (mobile)

---

## Image Treatment

- **Hero**: Full-height portrait, right-aligned, desaturated or high-contrast B&W
- **Case study thumbnails**: 16:9 ratio, dark overlay on hover, slight desaturation
- **Testimonial avatars**: 48px circle, grayscale filter (matches editorial palette)
- **All images**: `object-fit: cover`, no borders, no rounded corners
