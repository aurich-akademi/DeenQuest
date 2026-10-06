---
name: UPKK Adventure
colors:
  surface: '#f8f9ff'
  surface-dim: '#ccdbf4'
  surface-bright: '#f8f9ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#eff4ff'
  surface-container: '#e6eeff'
  surface-container-high: '#dde9ff'
  surface-container-highest: '#d5e3fd'
  on-surface: '#0d1c2f'
  on-surface-variant: '#3c4a42'
  inverse-surface: '#233144'
  inverse-on-surface: '#ebf1ff'
  outline: '#6c7a71'
  outline-variant: '#bbcabf'
  surface-tint: '#006c49'
  primary: '#006c49'
  on-primary: '#ffffff'
  primary-container: '#10b981'
  on-primary-container: '#00422b'
  inverse-primary: '#4edea3'
  secondary: '#855300'
  on-secondary: '#ffffff'
  secondary-container: '#fea619'
  on-secondary-container: '#684000'
  tertiary: '#006591'
  on-tertiary: '#ffffff'
  tertiary-container: '#23acf1'
  on-tertiary-container: '#003d59'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#6ffbbe'
  primary-fixed-dim: '#4edea3'
  on-primary-fixed: '#002113'
  on-primary-fixed-variant: '#005236'
  secondary-fixed: '#ffddb8'
  secondary-fixed-dim: '#ffb95f'
  on-secondary-fixed: '#2a1700'
  on-secondary-fixed-variant: '#653e00'
  tertiary-fixed: '#c9e6ff'
  tertiary-fixed-dim: '#89ceff'
  on-tertiary-fixed: '#001e2f'
  on-tertiary-fixed-variant: '#004c6e'
  background: '#f8f9ff'
  on-background: '#0d1c2f'
  surface-variant: '#d5e3fd'
typography:
  headline-xl:
    fontFamily: Plus Jakarta Sans
    fontSize: 40px
    fontWeight: '800'
    lineHeight: 48px
    letterSpacing: -0.02em
  headline-xl-mobile:
    fontFamily: Plus Jakarta Sans
    fontSize: 30px
    fontWeight: '800'
    lineHeight: 36px
    letterSpacing: -0.01em
  headline-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 32px
    fontWeight: '800'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-lg-mobile:
    fontFamily: Plus Jakarta Sans
    fontSize: 24px
    fontWeight: '800'
    lineHeight: 32px
  headline-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 22px
    fontWeight: '700'
    lineHeight: 28px
  headline-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 18px
    fontWeight: '700'
    lineHeight: 24px
  body-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 18px
    fontWeight: '500'
    lineHeight: 28px
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '500'
    lineHeight: 24px
  body-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '500'
    lineHeight: 20px
  label-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '700'
    lineHeight: 22px
    letterSpacing: 0.02em
  label-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 13px
    fontWeight: '700'
    lineHeight: 18px
    letterSpacing: 0.03em
  label-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 11px
    fontWeight: '800'
    lineHeight: 14px
    letterSpacing: 0.05em
rounded:
  sm: 0.5rem
  DEFAULT: 1rem
  md: 1.5rem
  lg: 2rem
  xl: 3rem
  full: 9999px
spacing:
  gutter: 1rem
  gutter-tablet: 1.5rem
  gutter-desktop: 2rem
  margin: 1rem
  margin-tablet: 2rem
  margin-desktop: 3rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2rem
---

## Brand & Style
The design system channels an exuberant, welcoming, and gamified tactile aesthetic built specifically for young Malaysian learners (ages 8–9). It blends playful game UI tropes—extruded "pressable" buttons, chunky floating badges, and high-visibility rewards—with clear visual hierarchy to make learning primary Islamic subjects (Sirah, Adab, Ibadah, Akidah, Jawi, and Lughah Arabiah) feel like an epic quest.

The visual style is **Tactile & Gamified**:
- **Affordance & Tangibility:** Interactive components feature dimensional bottom borders (isometric 3D bevels) that compress on click/press, offering immediate physical gratification.
- **Warmth & Optimism:** Soft pillowed shapes, rounded card corners, and buoyant elevation give the UI an inviting, approachable toy-box quality.
- **Motivating Clarity:** Clear progress indicators, glowing star badges, and vibrant streak banners celebrate small victories without overwhelming cognitive load.

## Colors
The palette balances natural Islamic heritage green with joyful arcade tones, grounded against warm, non-stark neutrals:

- **Primary (`#10B981` Adventure Emerald / Mint):** Core actions, primary quest paths, completed mastery states, and active navigation. Bottom bevel shadow: `#059669`.
- **Secondary (`#F59E0B` Cheerful Sun Amber):** XP counters, star currency, streak flames, and celebration alerts. Bottom bevel shadow: `#D97706`.
- **Tertiary (`#0EA5E9` Playful Sky Blue):** Energy/mana bars, trivia bubbles, secondary activities, and audio playback cues. Bottom bevel shadow: `#0284C7`.
- **Accent Coral Pink (`#F43F5E`):** Heart/life counts, bonus challenge tags, and urgent revision reminders. Bottom bevel shadow: `#E11D48`.
- **Background & Canvas:** Soft Cloud Cream (`#FDFBF7`) for the global canvas, with pure white (`#FFFFFF`) for elevated cards and modules.
- **Neutral Foreground (`#334155` Slate):** Soft, deep slate for ultra-legible typography without the harshness of pure black. Muted text sits at `#64748B`.

## Typography
Plus Jakarta Sans was selected for its open counters, playful circular geometries, and supreme legibility for early readers. 

- **Weight Strategy:** Headlines consistently use ExtraBold (800) and Bold (700) to convey a cartoonish, punchy rhythm that captures children's attention instantly. Body copy sits comfortably at Medium (500) to ensure high readability even on small mobile screens.
- **Bi-Directional Harmony:** Arabic and Jawi scripts (vital for UPKK modules) scale up by 15-20% relative to the Latin base size to ensure complex diacritics (tashkeel/harakat) remain crystal clear for 8-year-old eyes.

## Layout & Spacing
The layout model employs a fluid, mobile-first grid prioritizing generous touch zones (minimum tap target of 48px, ideally 56px for chunky buttons). 

- **Mobile (<768px):** Single-column quest map and exercise flow, with 16px lateral canvas margins (`margin`) and 16px component gutters (`gutter`). Navigation is anchored to a persistent bottom dock.
- **Tablet (768px - 1023px):** Two-column split layout (e.g., Quest Map on left, Live Stats & Current Mission on right) with 32px canvas margins (`margin-tablet`) and 24px column gutters (`gutter-tablet`).
- **Desktop (≥1024px):** Constrained 1200px max-width container, flanked by safe zones, utilizing a 12-column layout to host expansive stage boards, subject category cards, and side-panel companions.

## Elevation & Depth
Depth in this design system avoids photorealistic blur in favor of a tactile, game-cartridge feel:

- **The Duolingo-Style Bevel:** Action elements (buttons, selectable answer cards) feature a 0px blur, solid bottom edge offset (typically 4px to 6px) in a 20% darker shade of the element’s fill color.
- **Layer 0 (Canvas):** Soft Cloud Cream (`#FDFBF7`) without shadows.
- **Layer 1 (Cards & Islands):** Pure White (`#FFFFFF`) with a 2px solid perimeter outline (`#E2E8F0`) paired with a 4px solid bottom drop rim (`#CBD5E1`).
- **Layer 2 (Floating Badges & Dialogs):** Chunky white popups featuring a 6px bottom drop rim (`#94A3B8`) accompanied by a diffuse ambient glow (`0 12px 24px -4px rgba(15, 23, 42, 0.08)`).
- **Pressed State:** On interaction (`:active`), the top surface shifts down by 4px, compressing the bottom border to 0-1px, mimicking an authentic mechanical arcade push-button.

## Shapes
The shape language uses hyper-rounded forms (pill-shaped and extra-curved containers) to instill a friendly, secure, and playful environment:
- **Buttons, Badges, & Chips:** Full pill radii (`border-radius: 9999px`) creating candy-like interactive modules.
- **Cards & Content Blocks:** Generously rounded at 1.5rem (`24px`) to 2rem (`32px`), softening the visual interface and framing subject artwork like collectible adventure cards.
- **Interactive Exercise Bubbles:** Irregular, organic speech bubbles and curved dialogue boxes that visually mimic children’s comic strips.

## Components

### 1. 3D Tactile Buttons
- **Structure:** Pill-shaped (`border-radius: 9999px`) with an upper gradient sheen and a heavy bottom border (4px on desktop/tablet, 3px on mobile).
- **Primary (Green Quest):** Fill `#10B981`, bottom border `#059669`, text white.
- **Secondary (Golden Star):** Fill `#F59E0B`, bottom border `#D97706`, text white.
- **Tertiary (Sky Action):** Fill `#0EA5E9`, bottom border `#0284C7`, text white.
- **Behavior:** On tap/click, the button translates down (`transform: translateY(3px)`), flattening the bottom edge to produce an energetic click feel.

### 2. Achievement Cards & Subject Tiles
- **Structure:** White background cards with 24px border radii, wrapped in a 2px border (`#E2E8F0`) with a 4px flat bottom rim.
- **Subject Indicators:** Each UPKK subject (e.g., Sirah, Jawi) receives a playful thematic badge at the top-left with an illustrative icon and a themed mini-tag.
- **Progress Track:** Integrated pill-shaped progress bars with candy-striped animatable fill indicators.

### 3. Gamification Badges & Counters
- **Streak Flame Pill:** High-visibility pill badge with an animated amber flame icon, bold counter, and subtle yellow highlight outline.
- **Star & Diamond Currency Counters:** Floating pill widgets featuring 3D coin or star glyphs, showing live counts with bouncy number ticker animations.
- **Level/Mastery Shield:** Polygon shield badge with a thick white border, placed prominently at quest nodal intersections.

### 4. Interactive Multiple Choice & Drag-and-Drop Chips
- **Neutral State:** White pill or rounded rectangle with a 2px border (`#E2E8F0`) and 3px bottom edge (`#CBD5E1`).
- **Selected State:** Sky Blue or Mint tint with matching border and bottom rim.
- **Correct State:** Mint green background (`#DCFCE7`), border and shadow `#10B981`, accompanied by a cheerful bounce animation.
- **Incorrect State:** Coral pink background (`#FFE4E6`), border and shadow `#F43F5E`, paired with a gentle horizontal wobble animation.

### 5. Input Fields
- **Style:** Pill-shaped or 20px rounded containers with an extra-generous interior padding (16px 20px), bold placeholder text, and a 2px outline that shifts from `#E2E8F0` to `#10B981` with an inner glow when focused.