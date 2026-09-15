<div align="center">

# ⚡ Prompt Forge

### Service Launch Studio

**Paste a service description. Tune your branding. Preview the cover. Generate every AI prompt you need to launch.**

A single-file, zero-dependency HTML studio that turns a rough freelance service description into a complete launch kit — cover image prompt, listing copy, pricing tiers, FAQ, SEO tags, order messages, proposals, and a full launch pack — all tuned for ChatGPT, Claude, Gemini, and any image generator.

[![Single File](https://img.shields.io/badge/build-single%20HTML%20file-00D68F?style=flat-square)](#-quick-start)
[![No Dependencies](https://img.shields.io/badge/dependencies-none-00D68F?style=flat-square)](#-quick-start)
[![Offline Ready](https://img.shields.io/badge/works-offline-00D68F?style=flat-square)](#-privacy--offline-use)
[![Accessible](https://img.shields.io/badge/a11y-WCAG%20minded-00D68F?style=flat-square)](#-accessibility)
[![License](https://img.shields.io/badge/license-free%20to%20remix-00D68F?style=flat-square)](#-license)

Built by [Yasir Shabbir](https://yasirshabbir.com)

</div>

---

## 📖 Table of Contents

- [What It Is](#-what-it-is)
- [Why It Exists](#-why-it-exists)
- [Feature Highlights](#-feature-highlights)
- [Quick Start](#-quick-start)
- [The Seven Tabs](#-the-seven-tabs)
- [Canvas & Platform Presets](#-canvas--platform-presets)
- [Branding & Design System](#-branding--design-system)
- [Service Setup & Freelancer Profile](#-service-setup--freelancer-profile)
- [Generated Prompts](#-generated-prompts)
- [The Launch Pack](#-the-launch-pack)
- [Privacy & Offline Use](#-privacy--offline-use)
- [Accessibility](#-accessibility)
- [Browser Support](#-browser-support)
- [Technical Architecture](#-technical-architecture)
- [Customization](#-customization)
- [File Structure](#-file-structure)
- [FAQ](#-faq)
- [License](#-license)

---

## 🎯 What It Is

**Prompt Forge** is a self-contained HTML application — one file, no build step, no server, no npm — that acts as a **launch studio for service providers**. Paste in a raw description of what you do (a gig description, portfolio blurb, job post, or your own notes), and Prompt Forge:

1. **Extracts** the headline, features, tools, trust line, and a visual direction hint from your text.
2. **Lets you tune** branding — colors, fonts, corner radius, or upload an entire design spec.
3. **Previews** a live, pixel-accurate cover composition at the correct canvas size for Fiverr, Upwork, Contra, or any custom dimension.
4. **Generates** a hardened, art-director-grade **image prompt** for your cover.
5. **Generates** every **text prompt** you need — listing copy, pricing tiers, FAQ, SEO tags, proposals, and more.
6. **Bundles** everything into a single **launch pack** you can paste into one AI chat.

It's designed for **any** service provider: designers, developers, marketers, writers, video editors, consultants, agencies, and solo freelancers.

---

## 💡 Why It Exists

Most AI prompt generators give you a vague blob of text and wish you luck. Prompt Forge is different:

| Problem | Prompt Forge's Answer |
| --- | --- |
| AI covers come out with cards, tiles, and borders you didn't ask for | An **11-rule "ABSOLUTE RULES" block** at the top of every image prompt forbids containers, borders, duplicates, and dimension annotations |
| AI renders "1280×800" and "safe area" *inside* the image | Explicit **"render nothing about this spec"** directive plus a final checklist |
| AI truncates your headline mid-word | **"Render the headline complete"** rule with two-line balanced break instruction |
| AI reuses one logo for two different tools | **"Distinct and accurate official logos"** enforcement |
| You re-type the same brand info into every prompt | A shared **Service Brief** is injected into every generated prompt |
| LinkedIn PDF exports parse as garbage | **PDF.js + a custom manual extractor + LinkedIn-aware repair** that fixes garbled date tokens like `pik` → `yr`, `micsuib` → `mos`, and strips `3. 3. 3.` section markers |
| You lose everything when you close the tab | **Auto-save to localStorage** on every keystroke |

---

## ✨ Feature Highlights

<table>
<tr>
<td width="50%" valign="top">

### 🧠 Smart Extraction
Paste a paragraph, click **Extract & Auto-fill**, and Prompt Forge heuristically parses:
- Main headline (with "I will…" stripping)
- Features from a 200+ keyword library
- Tools from a ~140-entry tool dictionary
- Trust line from the last pipe-separated line
- Visual direction hint from 16 service archetypes

</td>
<td width="50%" valign="top">

### 🎨 Live Cover Preview
A real **canvas-accurate** preview that scales to fit your viewport:
- Correct aspect ratio per platform
- Safe-area guides (toggle-free, always visible as a dashed outline)
- Tool icons rendered in their **official brand colors** (~140 mapped)
- Feature items as icon + text pairs, never cards
- Headline in your chosen heading font

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 📄 CV & LinkedIn Parsing
Drop a PDF, Markdown, or text résumé:
- **PDF.js** primary extractor with CMap support
- **Manual PDF parser** fallback (uses `DecompressionStream` when available)
- **LinkedIn-aware repair** for garbled exports
- **Garbage detection** so you never fill fields with nonsense
- Auto-fills 12+ profile fields

</td>
<td width="50%" valign="top">

### 📦 Eleven Prompt Types
Every text prompt you need, one checkbox each:
- Full listing copy
- 3 listing variations
- Pricing packages
- FAQ & objections
- Search tags & SEO
- Buyer requirements
- Order messages
- Proposal / cover letter
- Profile bio & headline
- Single-field rewrite
- Thumbnail layer spec (JSON)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🧩 Design Spec Mode
Switch from manual branding to **Upload / Paste Spec** and drop:
- Brand guide text
- CSS tokens
- JSON design tokens
- Figma descriptions
- Reference images (as named visual refs)

The spec becomes the **authoritative brief** inside every prompt.

</td>
<td width="50%" valign="top">

### 🔒 100% Client-Side
- No server
- No analytics
- No tracking
- No file uploads
- Works offline after first load
- State persists via `localStorage` under `prompt-forge-v1`

</td>
</tr>
</table>

---

## 🚀 Quick Start

### Option 1 — Just open it

```bash
# 1. Save the file
#    prompt-forge.html

# 2. Double-click it
#    (or drag it into any modern browser)
```

That's it. No install, no build, no dependencies.

### Option 2 — Serve locally (optional, for PDF.js CORS cleanliness)

```bash
# Python 3
python -m http.server 8080

# Node
npx serve .

# Then open:
# http://localhost:8080/prompt-forge.html
```

### Option 3 — Host it anywhere static

Drop the single HTML file onto GitHub Pages, Netlify, Vercel, Cloudflare Pages, S3, or any static host. It's a single file — there's nothing to configure.

---

## 🗂 The Seven Tabs

| # | Tab | What it does |
| :-: | --- | --- |
| **1** | **Paste Description** | Paste raw text, click **Extract & Auto-fill**, or pick one of six sample chips (Graphic Design, Web/App Dev, SEO/Marketing, Video/Motion, Copywriting, Social Media). |
| **2** | **Service Setup** | Per-service fields only: service topic, platform / canvas preset, headline structure, floating features, tool icons, visual direction, buyer positioning, packages & pricing, requirements & process, and SEO for **this** service. Every new launch starts here. |
| **3** | **Freelancer Profile** | Profile-wide fields that stay the same across every service you launch: identity & contact, branding & design system, bio / proof / differentiators, baseline rates, and overall skills & SEO. Optionally auto-filled from a CV / LinkedIn upload. |
| **4** | **Cover Preview** | Live composition preview at native canvas scale, with a dashed safe-area outline and meta chips for canvas + safe-area dimensions. |
| **5** | **Image Prompt** | The full, hardened markdown prompt for your cover image. Copy or download as `.md`. |
| **6** | **Text Prompts** | Tick the prompt types you want. One combined markdown document is generated below. Copy or download as `.md`. |
| **7** | **Launch Pack** | Everything in one document: freelancer profile, this service's brief, platform rules, image prompt, and every ticked text prompt. Copy or download as `.md`. |

Each tab is keyboard-navigable (`←` `→` `Home` `End` `Enter` `Space`) and honors `prefers-reduced-motion`.

---

## 🖼 Canvas & Platform Presets

| Platform | Canvas | Safe Area | Padding | Ratio | Style Direction |
| --- | :-: | :-: | :-: | :-: | --- |
| **Fiverr** | 1280 × 769 | 1130 × 619 | 75 px | 5:3 landscape | High-contrast, premium, bold geometric typography |
| **Upwork** | 1000 × 750 | 880 × 630 | 60 px | 4:3 landscape | Refined, modern, restrained, breathable |
| **Contra** | 1600 × 1200 | 1420 × 1020 | 90 px | 4:3 | Sophisticated, design-forward, premium |
| **Other / Generic** | 1280 × 800 | 1130 × 650 | 75 px | 16:10 landscape | Modern, premium, bold geometric |
| **Custom** | 200–8000 px | auto | auto | computed | Composition tuned for the computed ratio |

### Custom Sizes

Pick **Custom** and you get:

- Width & height inputs (clamped 200–8000 px)
- Auto-computed padding based on the shorter side
- Eight quick-size chips: `1280×800`, `1280×720`, `1920×1080`, `1080×1080`, `1080×1350`, `1200×628`, `1500×1000`, `2000×2000`
- A live safe-area readout (`customSafePreview`)

> **Platform rules** are also baked in for **Fiverr**, **Upwork**, **LinkedIn**, **Contra**, and **Other** — each platform injects its own title/description/tag/FAQ rules into every generated text prompt and launch pack.

---

## 🎨 Branding & Design System

> **Where it lives:** Branding is set on the **Freelancer Profile** tab (Tab 3) because it's your identity as a freelancer — it applies to every service cover you generate. Set it once and every future service inherits it automatically.

### Manual mode

Set four colors — each with a swatch picker **and** a hex input that stay in sync:

| Color | Default | Purpose |
| --- | :-: | --- |
| **Primary / Accent** | `#00D68F` | Ambient glow, checkmark icons, trust line, tool icon accents |
| **Secondary / Highlight** | `#00FFAA` | Secondary accent (used by prompt, not always previewed) |
| **Background** | `#0A100E` | Canvas base |
| **Primary Text** | `#F3F3F1` | Headline, secondary, supporting, feature labels |

Then choose:

- **Heading font** — Syne, Space Grotesk, Inter, Poppins, Montserrat, Manrope, Sora, Outfit, DM Sans, Plus Jakarta Sans, Bricolage Grotesque, Playfair Display
- **Body font** — same list minus display faces
- **Icon corner radius** — `0px` / `8px` / `12px` / `16px` / `20px` / `24px` / `9999px`

### Spec mode

Switch to **Upload / Paste Spec** and either:

- Paste brand guide text, CSS tokens, or JSON design tokens, **or**
- Drop text files (`.txt .md .json .css .html .svg .csv .yml .js`) **or**
- Drop image files (kept as named visual references)

The spec is inserted **verbatim** into every prompt and marked as the **authoritative brief** — it wins over any conflicting instruction.

> **File limits:** 40,000 chars per text file · 120,000 chars total · silent truncation with a marker.

---

## 🧾 Service Setup & Freelancer Profile

Prompt Forge deliberately splits your data into **two levels**:

- **Service Setup (Tab 2)** — describes **one service** you're launching right now. Change these every time you launch something new.
- **Freelancer Profile (Tab 3)** — describes **you** as a freelancer. Stays the same across every service.

Every generated prompt and the launch pack merge both levels together automatically.

### The Service Setup tab (Tab 2)

Seven sections, each with a sticky section nav:

1. **Service Basics** — service topic, platform / canvas preset, main headline, secondary tagline, supporting line
2. **Features & Tools** — floating feature items, tool / software icons, trust line
3. **Visual Direction — This Service** — composition notes, must-avoid, additional notes
4. **Buyer Positioning — This Service** — target buyer, main problem solved, promised outcome
5. **Packages & Pricing — This Service** — Basic / Standard / Premium (pipe-separated `name | price | days | revisions | what's included`) + add-ons + deliverables
6. **Requirements & Process — This Service** — what the buyer must provide, process steps, FAQ seeds
7. **SEO & Search Intent — This Service** — primary keywords, buyer search phrases, tone of voice for this listing

### The Freelancer Profile tab (Tab 3)

Five sections, each with a sticky section nav:

1. **Identity & Contact** — name / studio, professional title, headline, experience level & years, location, languages, availability, LinkedIn, website — plus the **CV / LinkedIn upload** block (see below)
2. **Branding & Design System** — manual color / font / radius **or** Upload / Paste Spec mode
3. **Bio, Proof & Differentiators** — short bio, proof & credibility bullets, why-you differentiators
4. **Rates & Pricing Preferences** — currency (20 options), minimum project budget, hourly rate range, rate notes
5. **Profile Skills & Overall Search Intent** — complete toolkit across all services, profile keywords, overall buyer search phrases

### CV / LinkedIn upload

Toggle **Upload CV / LinkedIn PDF** on the Freelancer Profile tab and drop a file. The parser:

| Step | What happens |
| --- | --- |
| **1. Extract** | PDF.js first (handles CMaps). If it fails or returns garbage, a **manual PDF parser** runs — it walks `stream…endstream` blocks, inflates them via `DecompressionStream`, and reads `BT`/`Tj`/`TJ` text operators. |
| **2. Detect type** | LinkedIn exports are recognized by `linkedin.com/in/`, `(LinkedIn)` markers, or the `3. 3. 3. 3.` section-numbering artifact. |
| **3. Repair** | Garbled LinkedIn date tokens are fixed: `pik→yr`, `pokib→yrs`, `micsuib→mos`, and HTML entities are decoded. |
| **4. Parse** | LinkedIn parser extracts name, headline, bio, location, experience years, proof points, skills, tools, differentiators, languages, availability, search intent, and tone. Generic parser handles everything else. |
| **5. Fill** | Only **empty** fields are filled — your manual edits are never overwritten. |

> **Garbage detection:** if the extracted text has &lt; 30% letters, &lt; 15 real words, or no recognizable CV/LinkedIn vocabulary, the file is kept as an **AI reference only** and no fields are touched.

Supported inputs: `.pdf .md .markdown .txt .rtf .json .html .htm .yml .yaml .csv .log .doc .docx`

---

## 🧾 Generated Prompts

### 🖼 Image Prompt (Tab 5)

The image prompt is the star of the show. It opens with a hard rules block:

```
## 🛑 ABSOLUTE RULES — READ BEFORE ANYTHING ELSE

1. RENDER NOTHING ABOUT THIS SPEC.
2. NO CONTAINERS. EVER.
3. NO BORDERS OR DIVIDERS.
4. NO DUPLICATES.
5. RENDER THE HEADLINE COMPLETE.
6. TOOL LOGOS MUST BE DISTINCT AND ACCURATE.
```

Then it layers in:

- **Canvas** — exact dimensions, margin rules, "no guides in the image"
- **Composition** — six numbered placement instructions (headline → secondary → supporting → tool logos → feature items → trust line)
- **Content** — your headline, secondary, supporting, features, tools, trust line
- **Branding** — or the full design spec, if spec mode is on
- **Visual direction** — your notes, or the extracted hint
- **Style** — platform-specific art direction
- **Must avoid** — a hardened negative list
- **Final checklist** — 15 verification items the model must confirm before returning

### 📝 Text Prompts (Tab 6)

Eleven prompt types, each carrying your **Service Brief** and **Platform Rules**:

| Prompt | What it produces |
| --- | --- |
| **Full listing copy** | Title (with platform prefix rules), one-line summary, full description |
| **Three listing variations** | Direct/results-led · story-led · bold/punchy |
| **Pricing packages** | Markdown table of tiers + add-ons + pricing advice |
| **FAQ & objections** | 5–7 Q&A pairs covering common questions and top objections |
| **Search tags & SEO** | Exactly 5 tags, 10 secondary keywords, placement advice |
| **Buyer requirements** | 6–8 onboarding questions with reasons |
| **Order messages** | Welcome · delivery · review request |
| **Proposal / cover letter** | Under 250 words + 3 per-job swap-in lines |
| **Profile bio & headline** | Headline, short bio, full bio, skills |
| **Single-field rewrite** | Rewritten version + 2 alternatives + change rationale |
| **Thumbnail layer spec** | A JSON layer array + layout rationale |

Prompts are joined with `---` separators so you can paste the whole thing or copy one block.

---

## 📦 The Launch Pack

The final tab bundles **everything** into one markdown document:

```
# <Service> — complete launch pack

Platform: <Fiverr | Upwork | ...>

---

## FREELANCER PROFILE
   ... identity, branding & design system, bio, rates,
   ... plus any attached CV / LinkedIn text

## THIS SERVICE (the one being launched now)
   ... every field from Service Setup

## PLATFORM RULES
   ... exact title/description/tag rules for the chosen platform

---

# 1 · COVER IMAGE PROMPT
   ... the full hardened image prompt

---

# 2 · FULL LISTING COPY
# 3 · THREE LISTING VARIATIONS
# 4 · PRICING PACKAGES
   ... and so on, one section per ticked prompt
```

Paste the whole thing into one AI chat and work through it top to bottom.

---

## 🔒 Privacy & Offline Use

| Concern | Answer |
| --- | --- |
| Do you send my data anywhere? | **No.** Everything runs in your browser. |
| Do you upload my CV? | **No.** Files are read with `FileReader` and parsed locally. |
| Do you track me? | **No.** Zero analytics, zero pixels, zero beacons. |
| What's stored? | Only your form state, in `localStorage` under `prompt-forge-v1`. |
| How do I wipe it? | Click the **reset** icon in the header, or clear site data. |
| Does it work offline? | **Yes**, after the first load. The only network calls are Google Fonts and (optionally) PDF.js from a CDN. |

> **Tip:** To make it *fully* offline, download `pdf.min.js` and `pdf.worker.min.js` from the pinned CDN version (`3.11.174`), drop them next to the HTML file, and edit the `PDFJS_BASE` constant to point at the local files.

---

## ♿ Accessibility

Prompt Forge is built with accessibility in mind:

- **Skip link** to jump straight into the generator
- **ARIA roles** — `tablist`, `tab`, `tabpanel`, `radiogroup`, `status`, `alert`
- **Keyboard navigation** — full arrow-key support on the tab bar, `Enter`/`Space` activation, roving `tabindex`
- **Focus-visible rings** on every interactive element via a shared `--focus-ring` token
- **`prefers-reduced-motion`** honored — all animations collapse to `0.01ms`
- **`forced-colors: active`** support for Windows High Contrast Mode
- **Live regions** for status and toast messages (`aria-live="polite"`)
- **Semantic labels** — every input has an associated `<label>`, `.sr-only` where visual labels aren't wanted
- **`text-wrap: balance` / `pretty`** for readable headlines and paragraphs
- **`aria-current="true"`** on active section-nav links

---

## 🌐 Browser Support

| Browser | Version | Status |
| --- | :-: | :-: |
| Chrome / Edge | 111+ | ✅ Full support (including `DecompressionStream` for the manual PDF fallback) |
| Safari | 16.4+ | ✅ Full support |
| Firefox | 113+ | ✅ Full support |
| Chrome / Edge | 90–110 | ✅ Works — manual PDF fallback degrades gracefully |
| Older browsers | — | ⚠️ Renders, but PDF parsing may fall back to PDF.js only |

The app uses CSS custom properties, `backdrop-filter`, `aspect-ratio`, `clamp()`, `text-wrap`, and CSS grid — all widely supported in modern browsers.

---

## 🏗 Technical Architecture

### Zero dependencies (except two optional CDNs)

| Dependency | Purpose | Loaded |
| --- | --- | --- |
| **Syne** + **Space Grotesk** (Google Fonts) | Typography | Eagerly via `<link>` |
| **pdf.js 3.11.174** | PDF text extraction | **Lazily**, only when a PDF is dropped |

### Design tokens

All theming flows from CSS custom properties at `:root`:

```css
--primary: 160 100% 42%;      /* #00D68F */
--accent:  160 100% 50%;      /* #00FFAA */
--background: 160 25% 5%;     /* #0A100E */
--fg: 60 10% 95%;             /* #F3F3F1 */
--card: 160 20% 8%;
--border: 160 15% 18%;
--arzokeys: 25 100% 50%;      /* #FF7A00 */
```

### JavaScript modules (all IIFEs, no bundler)

| Module | Responsibility |
| --- | --- |
| **Global utilities** | `showToast()` |
| **Tips ticker** | Rotating tips bar above the tab list |
| **Persistence** | `localStorage` collect / restore / debounced save |
| **Reset All** | Confirm + wipe + reload |
| **Main studio** | Canvas presets, color sync, mode switches, spec files, tabs, section nav, extraction, preview, image prompt, output actions |
| **Service data** | Platform rules, PDF.js loader, manual PDF extractor, garbage detection, LinkedIn parser, generic parser, brief builder, text-prompt builders, launch pack builder |

### State persistence

```js
// Storage key
prompt-forge-v1

// Shape
{
  "topic": "...",
  "mainHeadline": "...",
  "primaryHex": "#00D68F",
  "radio:designMode": "manual",
  "radio:profileMode": "upload",
  "kind-listing": true,
  "kind-pricing": false,
  ...
}
```

Every input/textarea/select and every radio group is collected and restored. Saves are debounced by 500 ms.

### PDF extraction pipeline

```
File dropped
   │
   ├─► PDF.js extractText
   │       │
   │       └─► cleanup → garbage check → ✅ use it
   │
   └─► (fallback) manual extractor
           │
           ├─► walk `stream…endstream` blocks
           ├─► inflate via DecompressionStream('deflate')
           ├─► read BT/Tj/TJ text operators
           └─► cleanup → garbage check → ✅ use it
```

---

## 🛠 Customization

### Change the theme colors

Edit the `:root` block at the top of the `<style>` tag:

```css
:root {
  --primary: 160 100% 42%;   /* → any HSL triplet */
  --accent:  160 100% 50%;
  /* ... */
}
```

All colors are HSL triplets without the `hsl()` wrapper, so they can be composed with `hsl(var(--primary) / 0.5)` anywhere.

### Add a platform preset

In the `CANVAS_PRESETS` object in the main script:

```js
const CANVAS_PRESETS = {
  // ...
  Behance: {
    w: 1400, h: 900,
    pad: 80,
    safeW: 1240, safeH: 740,
    ratio: '14:9 landscape',
    label: 'Behance project cover',
    style: 'Editorial, portfolio-grade composition. Confident negative space.'
  }
};
```

Then add an `<option>` to the `#platform` select. If you also want platform-specific title/tag/FAQ rules, add a matching key to `PLATFORM_RULES`.

### Add a tool to the brand color map

```js
const BRAND_COLORS = {
  // ...
  "my tool": "#123456"
};

const BRAND_INITIALS = {
  // ...
  "my tool": "Mt"
};
```

### Add a text-prompt type

1. Add a checkbox to the `.check-grid` in the Text Prompts panel:
   ```html
   <label class="check-option">
     <input class="sr-only" type="checkbox" id="kind-newthing" name="promptKind" value="newthing" />
     <span class="check-box">...</span>
     <span class="check-body">
       <span class="check-title">My new prompt</span>
       <span class="check-sub">Short description</span>
     </span>
   </label>
   ```
2. Add a builder to the `BUILDERS` object:
   ```js
   newthing: () => wrap(
     'My New Prompt',
     'The task description...',
     'The output format...'
   )
   ```
3. Add a label to `LABELS`:
   ```js
   const LABELS = { /* ... */ newthing: 'My new prompt' };
   ```

That's it — the checkbox, the generated prompt, the download filename, and the launch pack section all wire up automatically.

---

## 📁 File Structure

```
prompt-forge.html      ← the entire application (single file)

# Optional, for fully offline PDF parsing:
pdf.min.js                ← from cdnjs pdf.js 3.11.174
pdf.worker.min.js         ← from cdnjs pdf.js 3.11.174
```

Internally, the file is organized as:

```
prompt-forge.html
├── <head>
│   ├── Meta tags (dark mode, theme color, viewport)
│   ├── Google Fonts preconnect + link
│   └── <style>  — all CSS, ~700 lines, tokenized
├── <body>
│   ├── Skip link
│   ├── Decorative blobs + noise overlay
│   ├── <header>  — brand, GitHub Issues chip, ArzoKeys chip, reset button
│   ├── <main>
│   │   ├── Hero
│   │   ├── Tips ticker
│   │   ├── Tab bar (7 tabs)
│   │   ├── Panel 1 — Paste Description
│   │   ├── Panel 2 — Service Setup
│   │   ├── Panel 3 — Freelancer Profile
│   │   ├── Panel 4 — Cover Preview
│   │   ├── Panel 5 — Image Prompt
│   │   ├── Panel 6 — Text Prompts
│   │   ├── Panel 7 — Launch Pack
│   │   ├── ArzoKeys promo card
│   │   └── Footer
│   └── Toast
└── <script> ×3
    ├── Global utilities + tips ticker + persistence + reset
    ├── Main studio (canvas, preview, image prompt)
    └── Service data (CV, parsers, text prompts, launch pack)
```

---

## ❓ FAQ

<details>
<summary><strong>Do I need an API key?</strong></summary>

No. Prompt Forge generates **prompts**, not completions. You copy the prompt, then paste it into ChatGPT, Claude, Gemini, Midjourney, DALL·E, Stable Diffusion, or whatever you use.

</details>

<details>
<summary><strong>Does it actually generate images?</strong></summary>

No. It generates the **image prompt**. The live preview on the Cover Preview tab is a **CSS/HTML approximation** of what the composition should look like — it's a design reference, not a rendered image.

</details>

<details>
<summary><strong>Will the AI follow the prompt exactly?</strong></summary>

No model follows any prompt perfectly. But Prompt Forge stacks the deck heavily in your favor with an absolute-rules block, a "render nothing about this spec" directive, a hardened negative list, and a 15-item final checklist. In practice, this dramatically reduces cards, tiles, borders, duplicated logos, and truncated headlines.

</details>

<details>
<summary><strong>Can I use it for non-design services?</strong></summary>

Yes. The tool is built for **any service provider** — developers, marketers, writers, video editors, consultants, accountants, virtual assistants. The extraction library, feature library, tool library, and visual-direction hints all cover dozens of service categories.

</details>

<details>
<summary><strong>What's the difference between Service Setup and Freelancer Profile?</strong></summary>

**Service Setup** (Tab 2) describes the **one service** you're launching right now — its buyer, headline, features, packages, requirements, and keywords. Change these whenever you launch a new offer.

**Freelancer Profile** (Tab 3) describes **you** — your identity, branding, bio, proof, baseline rates, and overall skills. Set it once; every service you launch inherits it.

Every generated prompt and the launch pack merge both together automatically.

</details>

<details>
<summary><strong>My LinkedIn PDF parsed as garbage. What now?</strong></summary>

Try exporting your profile again, or paste the text manually into a `.txt` file and drop that instead. The LinkedIn parser handles most exports, but some PDFs use non-standard font encodings that can't be recovered. The file will still be attached as an AI reference in the launch pack.

</details>

<details>
<summary><strong>Where is my data stored?</strong></summary>

In your browser's `localStorage`, under the key `prompt-forge-v1`. Nothing leaves your machine. Click the reset icon in the header to wipe it.

</details>

<details>
<summary><strong>Can I use this commercially?</strong></summary>

Yes. It's free to share, remix, and ship. Attribution is appreciated but not required.

</details>

<details>
<summary><strong>What's ArzoKeys?</strong></summary>

A free Chrome extension for managing license keys across devices — create, search, filter, cloud-sync, one-click copy, CSV import/export, and sync favorites. The promo card in the footer is the only outbound link in the app. → [arzokeys.com](https://arzokeys.com/)

</details>

---

## 📜 License

**Free to share, remix, and ship.**

Built by [**Yasir Shabbir**](https://yasirshabbir.com).

No warranty, no support guarantee — but if you build something great with it, that's the whole point.

---

<div align="center">

**⚡ Paste. Customize. Preview. Launch.**

Made for freelancers, by a freelancer.

[⬆ Back to top](#-prompt-forge)

</div>