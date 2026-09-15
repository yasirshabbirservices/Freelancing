# ⚡ Prompt Forge

### Service Launch Studio

**Paste a service description. Customize the brief and branding. Review the inputs. Preview the cover. Generate the prompts. Ship the launch pack.**

A single-file, zero-dependency HTML studio that turns a rough freelance service description into a complete launch kit — cover image prompt, listing copy, pricing tiers, FAQ, SEO tags, order messages, proposals, and a full launch pack — all tuned for ChatGPT, Claude, Gemini, and any image generator.

[![Single File](https://img.shields.io/badge/build-single%20HTML%20file-00D68F?style=flat-square)](#-quick-start)
[![No Dependencies](https://img.shields.io/badge/dependencies-none-00D68F?style=flat-square)](#-quick-start)
[![Offline Ready](https://img.shields.io/badge/works-offline-00D68F?style=flat-square)](#-privacy--offline-use)
[![Accessible](https://img.shields.io/badge/a11y-WCAG%20minded-00D68F?style=flat-square)](#-accessibility)
[![License](https://img.shields.io/badge/license-free%20to%20remix-00D68F?style=flat-square)](#-license)

Built by [Yasir Shabbir](https://yasirshabbir.com)

> **Current build documentation:** This README describes the single-file `prompt-forge.html` implementation supplied with this repository. Keep the README and HTML file in sync when features or platform rules change.

---

## 📖 Table of Contents

* [What It Is](#-what-it-is)
* [Why It Exists](#-why-it-exists)
* [Feature Highlights](#-feature-highlights)
* [Quick Start](#-quick-start)
* [The Seven Tabs](#-the-seven-tabs)
* [Canvas & Platform Presets](#-canvas--platform-presets)
* [Branding & Design System](#-branding--design-system)
* [Service Setup & Freelancer Profile](#-service-setup--freelancer-profile)
* [Generated Prompts](#-generated-prompts)
* [Live Service Review](#-live-service-review)
* [The Launch Pack](#-the-launch-pack)
* [Privacy & Offline Use](#-privacy--offline-use)
* [Accessibility](#-accessibility)
* [Browser Support](#-browser-support)
* [Technical Architecture](#-technical-architecture)
* [Current Platform Rules](#-current-platform-rules)
* [Customization](#-customization)
* [File Structure](#-file-structure)
* [FAQ](#-faq)
* [License](#-license)

---

## 🎯 What It Is

**Prompt Forge** is a self-contained HTML application — one file, no build step, no server, no npm — that acts as a **launch studio for service providers**. Paste in a raw description of what you do (a gig description, portfolio blurb, job post, or your own notes), and Prompt Forge:

1. **Extracts** the headline, features, tools, trust line, and a visual direction hint from your text.
2. **Lets you tune** branding — colors, fonts, corner radius, or upload an entire design spec.
3. **Previews** a live, pixel-accurate cover composition at the correct canvas size for Fiverr, Upwork, Contra, or any custom dimension.
4. **Generates** a hardened, art-director-grade **image prompt** for your cover.
5. **Generates** every **text prompt** you need — listing copy, pricing tiers, FAQ, SEO tags, proposals, and more.
6. **Bundles** everything into a single **launch pack** you can paste into one AI chat.
7. **Reviews the service brief live** so obvious omissions and risky inputs are visible before generation.

It's designed for **any** service provider: designers, developers, marketers, writers, video editors, consultants, agencies, and solo freelancers.

---

## 💡 Why It Exists

Most AI prompt generators give you a vague blob of text and wish you luck. Prompt Forge is different:

| Problem                                                              | Prompt Forge's Answer                                                                                                        |
| -------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| AI covers come out with cards, tiles, and borders you didn't ask for | A hardened **ABSOLUTE RULES** block forbids containers, borders, duplicates, dimension annotations, and separator-style text |
| AI renders "1280×800" and "safe area" *inside* the image             | Explicit **"render nothing about this spec"** instruction plus a final verification checklist                                |
| AI truncates your headline mid-word                                  | **"Render the headline complete"** with balanced two-line guidance                                                           |
| AI reuses one logo for two different tools                           | **Distinct and accurate official-logo enforcement** plus one-logo-per-tool rules                                             |
| Taglines become dot-separated / pipe-separated text on the cover     | **List-like detection** flags suspicious secondary/trust text and the image prompt can explicitly mark it as rejected        |
| The brief is technically valid but still incomplete                  | A **live service review** flags missing or risky fields and links directly to the field that needs attention                 |
| Advanced fields overwhelm a quick workflow                           | **Show advanced fields** keeps buyer positioning, pricing, process, SEO, and visual notes collapsed until needed             |
| You re-type the same brand info into every prompt                    | A shared **Service Brief + Freelancer Profile** is injected into generated prompts                                           |
| LinkedIn PDF exports parse as garbage                                | **PDF.js + manual PDF fallback + LinkedIn-aware repair + garbage detection**                                                 |
| You lose everything when you close the tab                           | **Auto-save to localStorage** with a debounced 500 ms write                                                                  |

---

## ✨ Feature Highlights

<table>
<tr>
<td width="50%" valign="top">

### 🧠 Smart Extraction

Paste a paragraph, click **Extract & Auto-fill**, and Prompt Forge heuristically parses:

* Main headline (with "I will…" stripping)
* Features from a 200+ keyword library
* Tools from a ~140-entry tool dictionary
* Trust line from the last pipe-separated line
* Visual direction hint from 16 service archetypes

</td>
<td width="50%" valign="top">

### 🎨 Live Cover Preview

A real **canvas-accurate** preview that scales to fit your viewport:

* Correct aspect ratio per platform
* Safe-area guides (always visible as a dashed outline)
* Tool icons rendered in their mapped official brand colors
* Feature items as icon + text pairs, never cards
* Headline in your chosen heading font

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 📄 CV & LinkedIn Parsing

Drop a PDF, Markdown, or text résumé:

* **PDF.js** primary extractor with CMap support
* **Manual PDF parser** fallback using `DecompressionStream` where available
* **LinkedIn-aware repair** for garbled exports
* **Garbage detection** so you never fill fields with nonsense
* Auto-fills profile fields without overwriting your manual edits

</td>
<td width="50%" valign="top">

### 📦 Eleven Prompt Types

Every text prompt you need, one checkbox each:

* Full listing copy
* 3 listing variations
* Pricing packages
* FAQ & objections
* Search tags & SEO
* Buyer requirements
* Order messages
* Proposal / cover letter
* Profile bio & headline
* Single-field rewrite
* Thumbnail layer spec (JSON)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🩺 Live Service Review

While you edit the Service Setup, Prompt Forge checks the brief for common problems:

* Missing service topic or main headline
* Missing / overlong feature items
* Missing / excessive tool icons
* List-like secondary taglines or trust lines
* Missing buyer, problem, outcome, keywords, search intent, tone, or packages when advanced mode is on
* Links each issue back to the affected field
* Errors are distinct from warnings so blocking omissions are obvious

</td>
<td width="50%" valign="top">

### 🧩 Design Spec Mode

Switch from manual branding to **Upload / Paste Spec** and drop:

* Brand guide text
* CSS tokens
* JSON design tokens
* Figma-style descriptions
* Reference images (as named visual refs)

The spec becomes the **authoritative brief** inside every prompt.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🔒 100% Client-Side

* No application server
* No analytics
* No tracking
* No file upload service
* State persists locally via `localStorage`
* Works without a backend
* Optional Google Fonts and lazy PDF.js CDN resources

</td>
<td width="50%" valign="top">

### ⚙️ Single-File Workflow

The whole application ships as:

* One `prompt-forge.html`
* No bundler
* No framework runtime
* No npm install
* No database
* No build step required

Open it directly, serve it locally, or place it on any static host.

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

### Option 2 — Serve locally

Serving through localhost is useful when you want cleaner CDN/PDF.js behavior during development.

```bash
# Python 3
python -m http.server 8080

# Node
npx serve .
```

Then open:

```text
http://localhost:8080/prompt-forge.html
```

### Option 3 — Host it anywhere static

Drop the single HTML file onto GitHub Pages, Netlify, Vercel, Cloudflare Pages, S3, or another static host.

There is no application server to configure.

---

## 🗂 The Seven Tabs

|   #   | Tab                    | What it does                                                                                                                                                                                                                                                                                             |
| :---: | ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1** | **Paste Description**  | Paste raw text, click **Extract & Auto-fill**, or pick one of six sample chips: Graphic Design, Web / App Dev, SEO / Marketing, Video / Motion, Copywriting, Social Media.                                                                                                                               |
| **2** | **Service Setup**      | Per-service fields: service topic, platform / canvas preset, headline structure, floating features, tool icons, and — behind an **Advanced** toggle — visual direction, buyer positioning, packages & pricing, requirements & process, and SEO. A **live service review** flags missing or risky inputs. |
| **3** | **Freelancer Profile** | Profile-wide identity and contact fields, branding, bio, proof, differentiators, baseline rates, and overall skills / SEO. Optionally auto-filled from a CV / LinkedIn upload.                                                                                                                           |
| **4** | **Cover Preview**      | Live composition preview at native canvas ratio, with a dashed safe-area outline and canvas + safe-area dimension chips.                                                                                                                                                                                 |
| **5** | **Image Prompt**       | The hardened markdown prompt for your cover image. Copy or download it as `.md`.                                                                                                                                                                                                                         |
| **6** | **Text Prompts**       | Select one or more prompt types. The tool generates one combined markdown document with each selected prompt separated by `---`.                                                                                                                                                                         |
| **7** | **Launch Pack**        | Everything in one document: service brief, freelancer profile, platform rules, image prompt, and every selected text prompt.                                                                                                                                                                             |

Each tab is keyboard-navigable (`←` `→` `Home` `End` `Enter` `Space`) and honors `prefers-reduced-motion`.

### Recommended workflow

1. Start in **Paste Description** and drop in the raw service description.
2. Click **Extract & Auto-fill** or use one of the sample service chips.
3. Open **Service Setup** and fix anything highlighted by the live review.
4. Turn on **Show advanced fields** only when you need deeper positioning, pricing, process, SEO, or visual notes.
5. Open **Freelancer Profile** and set the reusable identity, branding, proof, rates, and overall skills.
6. Check **Cover Preview** before generating the final image prompt.
7. Use **Image Prompt**, **Text Prompts**, or the all-in-one **Launch Pack** depending on how much you want to generate.

> **Important:** Auto-fill is heuristic. It is intentionally a starting point; review the extracted fields before treating the brief as final.

---

## 🖼 Canvas & Platform Presets

Prompt Forge currently exposes four ready-made canvas presets plus a fully custom mode.

| Platform            |    Canvas   |  Safe Area  | Padding |      Ratio      | Style Direction                                   |
| ------------------- | :---------: | :---------: | :-----: | :-------------: | ------------------------------------------------- |
| **Fiverr**          |  1280 × 769 |  1130 × 619 |  75 px  |  5:3 landscape  | High-contrast, premium, bold geometric typography |
| **Upwork**          |  1000 × 750 |  880 × 630  |  60 px  |  4:3 landscape  | Refined, modern, restrained, breathable           |
| **Contra**          | 1600 × 1200 | 1420 × 1020 |  90 px  |       4:3       | Sophisticated, design-forward, premium            |
| **Other / Generic** |  1280 × 800 |  1130 × 650 |  75 px  | 16:10 landscape | Modern, premium, bold geometric                   |
| **Custom**          | 200–8000 px |     auto    |   auto  |     computed    | Composition tuned for the computed ratio          |

The **platform selector** exposes Fiverr, Upwork, Contra, Other / Generic, and Custom. The codebase also contains a LinkedIn-specific text-rule set for prompt generation, but LinkedIn is not currently exposed as a selectable canvas preset.

### Custom Sizes

Pick **Custom** and you get:

* Width & height inputs clamped to `200–8000 px`
* Auto-computed padding based on the shorter side
* Quick-size chips such as `1280×800`, `1280×720`, `1920×1080`, `1080×1080`, `1080×1350`, `1200×628`, `1500×1000`, and `2000×2000`
* A live safe-area readout (`customSafePreview`)
* A simplified computed aspect-ratio/orientation label

---

## 🎨 Branding & Design System

> **Where it lives:** Branding is set on the **Freelancer Profile** tab (Tab 3) because it represents your reusable identity. Once set, it applies across service launches.

### Manual mode

Set four colors — each with a swatch picker and a synchronized hex input:

| Color                     |  Default  | Purpose                                                      |
| ------------------------- | :-------: | ------------------------------------------------------------ |
| **Primary / Accent**      | `#00D68F` | Ambient glow, checkmark icons, trust line, tool icon accents |
| **Secondary / Highlight** | `#00FFAA` | Secondary accent used by prompt and visual system            |
| **Background**            | `#0A100E` | Canvas base                                                  |
| **Primary Text**          | `#F3F3F1` | Headline, supporting text, and feature labels                |

Then choose:

* **Heading font** — Syne, Space Grotesk, Inter, Poppins, Montserrat, Manrope, Sora, Outfit, DM Sans, Plus Jakarta Sans, Bricolage Grotesque, Playfair Display
* **Body / UI font** — supported UI fonts from the selector
* **Soft icon corner radius** — `0px`, `8px`, `12px`, `16px`, `20px`, `24px`, or `9999px`

The radius setting is intended for **icon glyphs**, not content containers.

### Spec mode

Switch to **Upload / Paste Spec** and either:

* Paste brand guide text, CSS tokens, JSON design tokens, or design notes
* Drop text files such as `.txt`, `.md`, `.json`, `.css`, `.scss`, `.less`, `.html`, `.svg`, `.csv`, `.yml`, `.js`, `.jsx`, `.ts`, `.tsx`, `.xml`, or `.log`
* Drop image files as named visual references

The design spec is inserted into every generated prompt as the **authoritative brief**.

> **Spec limits:** 40,000 characters per text file · 120,000 characters total. Oversized content is truncated with a marker rather than allowed to grow without bound.

---

## 🧾 Service Setup & Freelancer Profile

Prompt Forge deliberately splits your data into **two levels**:

* **Service Setup (Tab 2)** — describes **one service** you're launching right now. Change these every time you launch something new.
* **Freelancer Profile (Tab 3)** — describes **you** as a freelancer. Stays the same across every service.

Every generated prompt and the launch pack merge both levels together automatically.

### The Service Setup tab (Tab 2)

Seven sections, with advanced sections hidden until enabled:

1. **Service Basics** — service topic, platform / canvas preset, main headline, secondary tagline, supporting line
2. **Features & Tools** — floating feature items, tool / software icons, trust line
3. **Visual Direction — This Service** — composition notes, must-avoid, additional notes
4. **Buyer Positioning — This Service** — target buyer, main problem solved, promised outcome
5. **Packages & Pricing — This Service** — Basic / Standard / Premium, add-ons, deliverables
6. **Requirements & Process — This Service** — what the buyer must provide, process steps, FAQ seeds
7. **SEO & Search Intent — This Service** — primary keywords, buyer search phrases, tone of voice for this listing

### Package format

The three core package fields accept:

```text
name | price | delivery days | revisions | what's included
```

Add-ons accept:

```text
name | price | delivery
```

### The Freelancer Profile tab (Tab 3)

Five reusable sections:

1. **Identity & Contact** — name / studio, professional title, headline, experience level & years, location, languages, availability, LinkedIn, website
2. **Branding & Design System** — manual color / font / radius or Upload / Paste Spec mode
3. **Bio, Proof & Differentiators** — short bio, proof / credibility, why-you differentiators
4. **Rates & Pricing Preferences** — currency, minimum project budget, hourly range, rate notes
5. **Profile Skills & Overall Search Intent** — complete toolkit, profile keywords, overall buyer search phrases

### CV / LinkedIn upload

Toggle **Upload CV / LinkedIn PDF** on the Freelancer Profile tab and drop a supported file.

The parser pipeline:

| Step               | What happens                                                                                                                                                                     |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Extract**     | PDF.js first. If that fails or returns garbage, the manual parser walks `stream…endstream` blocks and attempts to inflate and read PDF text operators.                           |
| **2. Detect type** | LinkedIn exports are recognized using LinkedIn markers and common export artifacts.                                                                                              |
| **3. Repair**      | LinkedIn-specific garbled date tokens and HTML entities are cleaned where possible.                                                                                              |
| **4. Parse**       | Extracts profile identity, headline, bio, location, experience, proof points, skills, tools, differentiators, languages, availability, search intent, and tone where detectable. |
| **5. Fill**        | Only **empty** profile fields are filled, so manual edits are preserved.                                                                                                         |

> **Garbage detection:** if extracted text is too sparse, has too few real words, or lacks recognizable CV / LinkedIn vocabulary, it is treated as an **AI reference only** and profile fields are left untouched.

Supported CV / profile file extensions currently accepted by the UI include:

```text
.pdf
.md
.markdown
.txt
.rtf
.json
.html
.htm
.yml
.yaml
.csv
.log
.doc
.docx
```

---

## 🧾 Generated Prompts

### 🖼 Image Prompt (Tab 5)

The image prompt is the star of the studio. It opens with a hardened instruction layer.

```text
1. RENDER NOTHING ABOUT THIS SPEC.
2. NO CONTAINERS. EVER.
3. NO BORDERS OR DIVIDERS.
4. NO DUPLICATES.
5. RENDER THE HEADLINE COMPLETE.
6. TOOL LOGOS MUST BE DISTINCT AND ACCURATE.
7. ONLY RENDER TEXT THAT ADDS MEANING. DROP EVERYTHING ELSE.
8. NEVER RENDER A SEPARATOR LIST.
```

Then it layers in:

* **Canvas** — exact dimensions, margin rules, and explicit "no guides in the image" instructions
* **Composition** — headline → secondary → supporting → tool logos → features → trust line
* **Content** — service headline, tagline, support line, features, tools, trust line
* **Branding** — manual design tokens or the full uploaded design spec
* **Visual direction** — your notes or extracted service hint
* **Style** — platform-specific art direction
* **Must avoid** — a hardened negative list
* **Rejected-field handling** — suspicious list-like text can be marked as `⛔ REJECTED` and must be omitted
* **Final checklist** — 18 explicit checks before the model returns the image

### List-like text detection

Prompt Forge specifically detects fields that look like a separator list, such as:

```text
Word • Word • Word
Word | Word | Word
Word, Word, Word
```

When secondary or trust text is detected as list-like, the review warns about it and the generated image prompt instructs the image model to drop that field rather than rendering an unwanted list on the cover.

### Text Prompts (Tab 6)

Eleven prompt types are available:

| Prompt                       | What it produces                                                      |
| ---------------------------- | --------------------------------------------------------------------- |
| **Full listing copy**        | Search-optimized title, one-line summary, full description            |
| **Three listing variations** | Direct/results-led · story-led · bold/punchy                          |
| **Pricing packages**         | Buyer-ready tiers + add-ons + pricing sanity check                    |
| **FAQ & objections**         | 5–7 Q&A entries covering buyer questions and objections               |
| **Search tags & SEO**        | Exactly 5 tags, secondary keywords, profile overlap, placement advice |
| **Buyer requirements**       | 6–8 onboarding questions with reasons                                 |
| **Order messages**           | Welcome · delivery · review request                                   |
| **Proposal / cover letter**  | Under 250 words + 3 swap-in lines                                     |
| **Profile bio & headline**   | Headline, short bio, full bio, skills                                 |
| **Single-field rewrite**     | Rewritten version + 2 alternatives + change rationale                 |
| **Thumbnail layer spec**     | Structured JSON layer array + layout rationale                        |

Each selected prompt includes the shared service brief, freelancer profile, platform rules, tone, and relevant source fields.

Use **Select all** or **Clear** to control the full prompt set quickly.

Prompts are joined with `---` separators so you can paste the whole thing or copy one block.

---

## 🩺 Live Service Review

The **Service Setup** tab contains a real-time review layer designed to catch common prompt-quality problems before you generate anything.

### Always-checked fields

* Service topic — required
* Main headline — required
* Secondary tagline — warns when it looks like a separator/list
* Trust line — warns when it looks like a separator/list
* Feature items — warns when empty, over the six-item limit, or too wordy
* Tool icons — warns when empty or over the eight-icon limit

### Advanced checks

When **Show advanced fields** is enabled, the review also checks:

* Target buyer
* Main problem solved
* Promised outcome
* Primary service keywords
* Buyer search phrases
* Tone of voice
* Basic / Standard / Premium package coverage

### Warning vs error behavior

* **Errors** indicate missing inputs that materially weaken the generated brief.
* **Warnings** indicate risky or low-quality input that Prompt Forge can still process.
* Each flagged field receives a visual state, and review items are interactive so you can jump back to the source field.

This review is intentionally advisory. It does not invent missing business facts for you.

---

## 📦 The Launch Pack

The final tab bundles the reusable profile, the current service, platform rules, the image prompt, and the selected text prompts into one markdown document.

Conceptually:

```text
# <Service> — complete launch pack

Platform: <Fiverr | Upwork | Contra | Other | Custom>

---

## FREELANCER PROFILE
... identity, branding & design system, bio, rates, skills,
... plus any attached CV / LinkedIn reference text

## THIS SERVICE
... service setup for the offer being launched

## PLATFORM RULES
... exact rules used by the selected platform

---

# 1 · COVER IMAGE PROMPT
... full hardened image prompt

---

# 2 · FULL LISTING COPY
# 3 · THREE LISTING VARIATIONS
# 4 · PRICING PACKAGES
# 5 · FAQ & OBJECTIONS
...
```

The pack is designed to be pasted into a single AI chat and processed section by section.

---

## 🔒 Privacy & Offline Use

| Concern                       | Answer                                                                                                                             |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| Do you send my data anywhere? | **No.** The application logic runs in your browser.                                                                                |
| Do you upload my CV?          | **No.** Files are read locally through browser file APIs and parsed in the page.                                                   |
| Do you track me?              | **No.** There is no application analytics, tracking pixel, or telemetry layer.                                                     |
| What's stored?                | Form state is stored in `localStorage` under `prompt-forge-v1`.                                                                    |
| How do I wipe it?             | Click the **reset** icon in the header, or clear site data.                                                                        |
| Does it work offline?         | **Yes**, after the first load. Google Fonts are loaded remotely and PDF.js is loaded lazily from a CDN when PDF parsing is needed. |

> **Tip:** To make the app completely self-contained for PDF parsing, download `pdf.min.js` and `pdf.worker.min.js` from the pinned PDF.js version (`3.11.174`), place them alongside the HTML file, and update the PDF.js loader in the application to use the local files.

### Important privacy boundary

"Client-side" means Prompt Forge does not send your service brief or profile to a Prompt Forge server. Any AI service you later paste the generated prompts into will have its **own** privacy and data-retention policies.

---

## ♿ Accessibility

Prompt Forge is built with accessibility in mind:

* **Skip link** to jump straight into the generator
* **ARIA roles** — `tablist`, `tab`, `tabpanel`, `radiogroup`, `status`, `alert`
* **Keyboard navigation** — arrow-key support on the tab bar, `Enter` / `Space` activation, and roving `tabindex`
* **Focus-visible rings** on interactive elements
* **`prefers-reduced-motion`** honored — animations collapse to near-zero duration
* **`forced-colors: active`** support for Windows High Contrast Mode
* **Live regions** for status and toast messages
* **Semantic labels** — inputs have associated labels, with `.sr-only` used where visual labels are unnecessary
* **Text wrapping controls** for balanced headings and readable paragraphs
* **`aria-current="true"`** for the active section navigation link

---

## 🌐 Browser Support

| Browser        | Version | Status                                                                                  |
| -------------- | :-----: | --------------------------------------------------------------------------------------- |
| Chrome / Edge  |   111+  | ✅ Full support including `DecompressionStream` for the manual PDF fallback              |
| Safari         |  16.4+  | ✅ Full support                                                                          |
| Firefox        |   113+  | ✅ Full support                                                                          |
| Chrome / Edge  |  90–110 | ✅ Works — manual PDF fallback degrades gracefully                                       |
| Older browsers |    —    | ⚠️ The app can render, but PDF parsing may rely more heavily on the fallback / CDN path |

The UI uses modern browser capabilities including CSS custom properties, `backdrop-filter`, `aspect-ratio`, `clamp()`, CSS grid, `text-wrap`, browser file APIs, and modern JavaScript.

---

## 🏗 Technical Architecture

### No application dependencies (except two optional network resources)

| Dependency                                  | Purpose             | Loaded                                                                         |
| ------------------------------------------- | ------------------- | ------------------------------------------------------------------------------ |
| **Syne** + **Space Grotesk** (Google Fonts) | Typography          | Eagerly via `<link>`                                                           |
| **pdf.js 3.11.174**                         | PDF text extraction | **Lazily**, only when a PDF is dropped; manual parser is available as fallback |

There is no framework runtime, npm dependency tree, database, backend, or API key.

### Design tokens

The main theme flows from CSS custom properties at `:root`:

```css
--primary: 160 100% 42%;      /* #00D68F */
--accent:  160 100% 50%;      /* #00FFAA */
--background: 160 25% 5%;     /* #0A100E */
--fg: 60 10% 95%;             /* #F3F3F1 */
--card: 160 20% 8%;
--border: 160 15% 18%;
--arzokeys: 25 100% 50%;      /* #FF7A00 */
```

### JavaScript modules

The application is organized as IIFEs and plain browser JavaScript rather than bundled modules.

| Module                           | Responsibility                                                                                                                                                            |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Global utilities**             | `showToast()` and small DOM helpers                                                                                                                                       |
| **Tips ticker**                  | Rotating tips bar above the tab list                                                                                                                                      |
| **Persistence**                  | `localStorage` collect / restore / debounced save                                                                                                                         |
| **Reset All**                    | Confirm + wipe + reload                                                                                                                                                   |
| **Main studio**                  | Canvas presets, color sync, mode switches, spec files, tabs, section navigation, extraction, preview, image prompt, and output actions                                    |
| **Service data / prompt engine** | Platform rules, PDF.js loader, manual PDF extractor, garbage detection, LinkedIn parser, generic parser, service brief builder, text-prompt builders, launch-pack builder |
| **Live service review**          | Required-field checks, warning/error states, and focusable issue links                                                                                                    |

### State persistence

Storage key:

```text
prompt-forge-v1
```

The application collects form controls, radios, checkboxes, and relevant state, serializes them to JSON, and saves through a 500 ms debounce.

Conceptual state shape:

```js
{
  "topic": "...",
  "mainHeadline": "...",
  "primaryHex": "#00D68F",
  "radio:designMode": "manual",
  "radio:profileMode": "upload",
  "kind-listing": true,
  "kind-pricing": false
}
```

### PDF extraction pipeline

```text
File dropped
   │
   ├─► PDF.js extractText
   │       │
   │       └─► cleanup → garbage check → ✅ use it
   │
   └─► fallback manual extractor
           │
           ├─► walk `stream…endstream` blocks
           ├─► inflate via `DecompressionStream('deflate')` where available
           ├─► read BT/Tj/TJ text operators
           └─► cleanup → garbage check → ✅ use it
```

### Prompt construction model

The prompt engine effectively combines:

```text
Freelancer Profile
        +
Current Service Brief
        +
Selected Platform Rules
        +
Brand / Design Spec
        +
Output-Specific Instructions
        =
Generated Prompt
```

That shared-context approach prevents the same identity, rates, branding, proof, and service facts from being manually repeated in every prompt type.

---

## 🧭 Current Platform Rules

The text prompt builders inject platform-specific rules into every generated prompt.

### Fiverr

* Title starts with **"I will"** and stays at or under 80 characters
* Exactly 3 packages: Basic, Standard, Premium
* Description: 300–1200 characters, plain text, short paragraphs
* Exactly 5 lowercase search tags, 1–3 words each, no punctuation
* FAQ: 3–5 short Q&A pairs
* Cover: 1280 × 769 px with a 75 px clear margin

### Upwork

* Project Catalog title is an outcome statement at or under 90 characters
* 3 fixed-price tiers with scope, delivery time, and revisions
* Buyer outcome → scope → process structure
* No contact details or off-platform links
* Cover: 1000 × 750 px with a 60 px clear margin

### LinkedIn

A LinkedIn-specific rule set exists in the generator for text prompt construction:

* Headline under 220 characters, first person, professional tone
* Service page description under 2000 characters
* Up to 10 skills / specialities as keywords
* Cover guidance: 1200 × 627 px with a 60 px clear margin

> The current platform dropdown does **not** expose LinkedIn as a selectable canvas preset. Its rule set is still part of the internal platform-rules dictionary.

### Contra

* Friendly independent-creator tone
* 3 service packages with clear scope and timeline
* Emphasize portfolio proof and past client results
* Cover: 1600 × 1200 px with a 90 px clear margin

### Other / Generic

* Outcome-led title under 90 characters
* 3 packages with price, timeline, and revisions
* Plain text, short paragraphs, no contact details

Custom canvas sizes inherit the generic text-rule behavior while using the dimensions and ratio you specify.

---

## 🛠 Customization

### Change the theme colors

Edit the `:root` block at the top of the `<style>` tag:

```css
:root {
  --primary: 160 100% 42%;
  --accent:  160 100% 50%;
  --background: 160 25% 5%;
  --fg: 60 10% 95%;
}
```

Colors are generally stored as HSL triplets without the `hsl()` wrapper so they can be reused with alpha:

```css
hsl(var(--primary) / 0.5)
```

### Add a platform preset

In the `CANVAS_PRESETS` object in the main script:

```js
const CANVAS_PRESETS = {
  // ...
  Behance: {
    w: 1400,
    h: 900,
    pad: 80,
    safeW: 1240,
    safeH: 740,
    ratio: '14:9 landscape',
    label: 'Behance project cover',
    style: 'Editorial, portfolio-grade composition. Confident negative space.'
  }
};
```

Then add the matching option to the `#platform` select.

If you also want platform-specific title, description, tag, or FAQ constraints, add a matching entry to `PLATFORM_RULES`.

### Add a tool to the brand color map

Add a tool to `BRAND_COLORS`:

```js
const BRAND_COLORS = {
  // ...
  "my tool": "#123456"
};
```

Optionally add a preferred initials mapping:

```js
const BRAND_INITIALS = {
  // ...
  "my tool": "Mt"
};
```

### Add a text-prompt type

1. Add a checkbox to the prompt-type check grid in the Text Prompts panel:

```html
<label class="check-option">
  <input
    class="sr-only"
    type="checkbox"
    id="kind-newthing"
    name="promptKind"
    value="newthing"
  />
  <span class="check-box">...</span>
  <span class="check-body">
    <span class="check-title">My new prompt</span>
    <span class="check-sub">Short description</span>
  </span>
</label>
```

2. Add a builder to `BUILDERS`:

```js
newthing: () => wrap(
  'My New Prompt',
  'The task description...',
  'The output format...'
)
```

3. Add the label:

```js
const LABELS = {
  // ...
  newthing: 'My new prompt'
};
```

The checkbox, generated output, download naming, and launch-pack section are wired through the shared prompt-engine flow.

---

## 📁 File Structure

The minimal project is:

```text
prompt-forge.html      ← the entire application

# Optional, for fully offline PDF parsing:
pdf.min.js             ← PDF.js 3.11.174
pdf.worker.min.js      ← PDF.js 3.11.174
```

Internally, the HTML file is organized roughly as:

```text
prompt-forge.html
├── <head>
│   ├── Meta tags (dark mode, theme color, viewport)
│   ├── Google Fonts preconnect + link
│   └── <style> — all CSS, tokenized
├── <body>
│   ├── Skip link
│   ├── Decorative blobs + noise overlay
│   ├── <header> — brand, GitHub Issues chip, ArzoKeys chip, reset button
│   ├── <main>
│   │   ├── Hero
│   │   ├── Tips ticker
│   │   ├── Tab bar (7 tabs)
│   │   ├── Panel 1 — Paste Description
│   │   ├── Panel 2 — Service Setup
│   │   │   ├── Advanced-field toggle
│   │   │   └── Live service review
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
    └── Service data / parsers / prompt builders / launch pack
```

---

## ❓ FAQ

<details>
<summary><strong>Do I need an API key?</strong></summary>

No. Prompt Forge generates **prompts**, not AI completions. You copy the prompt and paste it into ChatGPT, Claude, Gemini, Midjourney, DALL·E, Stable Diffusion, or another AI tool.

</details>

<details>
<summary><strong>Does it actually generate images?</strong></summary>

No. It generates the **image prompt**. The Cover Preview tab is a **CSS/HTML approximation** of the target composition — a design reference, not a final AI-rendered image.

</details>

<details>
<summary><strong>Will the AI follow the prompt exactly?</strong></summary>

No model follows any prompt perfectly. Prompt Forge is designed to improve consistency through an absolute-rules block, explicit spec isolation, negative instructions, rejected-field handling, and an 18-item final checklist.

</details>

<details>
<summary><strong>What does the live service review do?</strong></summary>

It checks the current service brief for missing or risky inputs before you generate prompts. It does not write business facts for you; it highlights places where the brief is incomplete, overloaded, or likely to produce weak output.

</details>

<details>
<summary><strong>What does "Show advanced fields" change?</strong></summary>

It reveals the deeper service fields for visual direction, buyer positioning, packages, process, and service SEO. Leave it off for a faster basic workflow; turn it on when you want tighter control over the generated listing and launch pack.

</details>

<details>
<summary><strong>Can I use it for non-design services?</strong></summary>

Yes. The tool is built for **any service provider** — developers, marketers, writers, video editors, consultants, virtual assistants, and other freelancers. The extraction and prompt systems are service-oriented rather than tied to a single profession.

</details>

<details>
<summary><strong>What's the difference between Service Setup and Freelancer Profile?</strong></summary>

**Service Setup** (Tab 2) describes the **one service** you're launching right now — its buyer, headline, features, packages, requirements, visual notes, and service keywords.

**Freelancer Profile** (Tab 3) describes **you** — identity, branding, bio, proof, baseline rates, and overall skills. Set it once; every service you launch reuses it.

Every generated prompt and the launch pack merge both layers automatically.

</details>

<details>
<summary><strong>My LinkedIn PDF parsed as garbage. What now?</strong></summary>

Try exporting the profile again, or save the relevant text as `.txt` / Markdown and drop that instead. The parser contains LinkedIn-aware cleanup, but some PDF files use font encodings that cannot be recovered reliably. When extraction fails the file can remain an AI reference instead of overwriting your profile fields.

</details>

<details>
<summary><strong>Where is my data stored?</strong></summary>

In your browser's `localStorage`, under the key `prompt-forge-v1`. Prompt Forge does not maintain a backend database. Use the reset icon in the header to clear the stored state.

</details>

<details>
<summary><strong>Can I use this commercially?</strong></summary>

Yes. The project is documented as free to share, remix, and ship. Attribution is appreciated but not required.

</details>

<details>
<summary><strong>What's ArzoKeys?</strong></summary>

ArzoKeys is a free Chrome extension for managing API keys and license tokens locally in the browser with cloud-sync. Prompt Forge includes an ArzoKeys promo card and outbound link.

→ [arzokeys.com](https://arzokeys.com/)

</details>

---

## 📜 License

**Free to share, remix, and ship.**

Built by [**Yasir Shabbir**](https://yasirshabbir.com).

No warranty, no support guarantee — but if you build something great with it, that's the whole point.

---

<div align="center">

**⚡ Paste. Customize. Review. Preview. Launch.**

Made for freelancers, by a freelancer.

[⬆ Back to top](#-prompt-forge)

</div>
