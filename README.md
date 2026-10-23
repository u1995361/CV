# CV Website · Jaume Cañellas López

Preliminary submission for Hypermedia (Part 1): a single-page website featuring my Curriculum Vitae, built with HTML and CSS.

- **Published website:** _(pending: add the GitHub Pages link)_
- **Figma design:** https://www.figma.com/design/vbGeTNpaQQR43cZIE0RZHe/CV?node-id=0-1&t=fUCX1tEwJ0s6fTBW-1
---

## 1. Project Analysis

### 1.1 User Profile (Persona)

**Primary persona (fictional): Marta Ferrer**

| | |
|---|---|
| **Age and role** | 41 years old. Front desk and human resources manager at a four-star hotel in northern Mallorca. |
| **Usage context** | Reviews CVs between tasks, often on her phone and sometimes on the reception computer. Spends between 30 and 60 seconds on each candidate before deciding whether to contact them. |
| **What she expects to find** | A clearly displayed name and contact details, previous hotel experience, language skills (especially English), availability, and a driving licence, as many hotels are far from public transport. |
| **Goals** | Fill seasonal positions quickly with reliable, experienced people who can start soon. |
| **Frustrations** | Long or poorly organised CVs, PDFs that are difficult to read on a phone, and contact details that are hard to find or copy. |

**Secondary persona (fictional): Pau Serra**

He is 29 years old and works as a producer at an indie video game studio. He is looking for student interns and wants to quickly find their degree, technical skills and, when available, a project portfolio. This profile explains why university studies and technical skills (languages and game engines) should be visible, and informs the planned addition of a projects section.

### 1.2 Information Architecture

The CV is a single page with two columns. The information is organised by data type and its priority for the reader, keeping Marta's profile in mind: limited time and a need to find contact details and work experience immediately.

The **left column** is a sidebar containing quick-reference information that changes less frequently: the photograph, contact details (phone and email with direct `tel:` and `mailto:` links), languages, driving licence, skills, technical skills (programming languages and game engines), and an additional information note about availability. These details help readers decide whether they can contact the person and whether the candidate meets the basic requirements. On desktop, the sidebar is *sticky*, so contact details remain visible while the rest of the page is being read.

The **right column** contains the narrative content. It starts with the name header, continues with **work experience**, and ends with **education**. I placed experience before education because hospitality employers, the main target audience, prioritise previous experience. Education appears in the final block, ordered from most recent to oldest.

Each block is a card with a section heading and an icon, allowing readers to scan the page in a few seconds. Work experience and education entries follow the same pattern (role or institution, period, and key points), so once readers understand one entry, they can understand them all.

On narrow screens, the two columns become a single column, with the sidebar at the top. This ensures that contact details and profile information are also the first things readers see on mobile.

### 1.3 Visual Design

**Palette.** I chose a single accent colour, a soft turquoise (`#0ea5a5`), against a neutral base: a `#fcfcfc` background, white cards, `#111` text, `#5b5b5b` secondary text, and `#e9ecef` borders. The turquoise evokes the sea and Mallorca, conveys calm and trust, and suits the hospitality sector without drawing too much attention. It is used only for details (icons, language and licence tags, and link underlines) to keep the focus on the content. The main colours are CSS variables in `:root` (`--bg`, `--ink`, `--muted`, `--accent`, `--line`, `--chip`), so the palette can be changed by editing just a few values.

**Typography.** I use **Inter** (Google Fonts), a sans-serif typeface designed for screen readability, with weights from 300 to 800 to create hierarchy: the name uses weight 800 and a fluid font size (`clamp`); section headings are small, uppercase, and widely spaced; job titles use weight 700; and dates are smaller and grey.

**Composition.** The layout uses CSS Grid: a 340 px sidebar and a flexible column, with a maximum width of 1100 px to prevent excessively long lines. Information is grouped into cards with rounded corners (16 px) and a thin border rather than heavy shadows, creating a clean, modern appearance.

**Icons and image.** The icons are inline SVGs (Lucide-style) that inherit their colour through `currentColor`, and the photograph is circular to create a friendly impression.

**Responsive layout and printing.** Below 920 px, the layout switches to a single column. There is also an A4 print stylesheet so the CV can be saved as a PDF.

## 2. Figma Design

_(Pending: add the Figma project link here.)_

Design inspiration: _(pending: add the projects consulted for inspiration.)_

## 3. Technologies and Rationale

- **HTML5 and CSS3**, with no JavaScript and **no frameworks** (neither Bootstrap nor any other framework was used).
- **Why no framework:** this is a static, single-page website with only a few components. A framework would add unnecessary weight and a generic appearance that I do not need. Writing the CSS by hand allowed me to control the layout with Grid and Flexbox, the variables, and the responsive behaviour, while keeping the code clear.
- **Class naming convention** similar to BEM (`block__title`, `item__role`, `item__meta`) to keep the CSS easy to read.
- **External typeface:** Inter is loaded from Google Fonts. If it cannot be loaded, the browser uses the system font.

## 4. Repository Structure

```text
.
├── index.html     # CV structure and content
├── styles.css     # Styles, colour variables, responsive layout, and printing
├── foto.jpeg      # Photograph
└── README.md
```

## 5. How to View and Publish It

- **Locally:** open `index.html` in a browser.
- **Publishing:** the website has been published using GitHub Pages (_Settings → Pages → Deploy from a branch → `main` / `root`_). For this to work, the main file must be named `index.html`.

## 6. Credits

- [Inter](https://rsms.me/inter/) typeface (SIL Open Font License).
- Icons inspired by [Lucide](https://lucide.dev) (ISC licence).
- Photograph: my own.
