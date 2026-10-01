# Techable Australia — Content & Image Handover

Site: `http://localhost:10049` (WordPress, theme `techable`). Log in at `/wp-admin/`.
Everything below is a content/image task — no code changes are needed. Items are ordered by what visitors see first.

---

## 1. Where things are edited

| Area | Edit in WP admin |
|---|---|
| Header, mega menu, footer columns, newsletter, copyright, social links | **Techable Settings** (left sidebar) |
| Home page sections (hero, stats, work showcase, testimonials, pricing teaser) | **Pages → Home** (fields below the editor) |
| About, Pricing, Contact, Blog listing, Career listing, Request a Demo, legal pages | **Pages → [page]** — each hero title/paragraph and section text is a field |
| Service pages (39) — title, excerpt, featured image | **Services** post type |
| Service page body copy (overview, what's included, process, outcomes, FAQs) | Developer file `inc/service-copy.php` — send copy changes to the developer, or paste into the post **Excerpt** to override the intro |
| Practice-area hub pages (Digital Marketing, Development, …) | **Services → Categories** — the *Description* field is the hero paragraph |
| Case studies | **Work** post type — title, featured image, excerpt, body (`H2` headings become labelled rows: *Challenge / Approach / Outcomes*), **Project date** field |
| Job ads | **Career** post type — title, excerpt, body, fields *Job location*, *Employment type*, *Apply URL* |
| Blog posts | **Posts** |

---

## 2. Priority fixes — placeholder or unverified claims still live

| Page | What | Action |
|---|---|---|
| Home (hero cards) | "25+ Global Enterprise drives innovation", location pills **Mexico / Australia**, "25+ Our Esteemed Clients and Partners" | Replace with real figures and real locations. Fields: *Pages → Home → Hero collage*. |
| Home (stats band) | Counter numbers | Confirm they are real. *Pages → Home → Stats*. |
| Services pages (why-us band) | "25+ Brands and partners supported across Australia and Mexico" | Give the developer the real client count / regions (lives in `inc/service-proof.php`). |
| Blog, Contact, Career heroes | A **"Watch Demo"** button from the template | Either supply a real video URL (*Techable Settings → Demo video*) or ask the developer to remove the button on those pages. |
| About page | Team/leader names, awards list, "Trusted by" logos — all template content | Supply real team members (name, role, photo), real awards, real client logos. |
| Pricing page | Plan names, prices, feature lists | Confirm plans are real. *Pages → Pricing*. |
| Testimonials (Home) | Quotes and names are template copy | Supply 3–6 real client quotes with name, role, company, and photo. |
| Case studies (5) | Titles *Market Magnet, Growth Engine, Trend Beacon, Market Motion, Tidal Strategy* and all body copy are template examples | Replace with real projects (see §4), or unpublish the ones you can't replace. |
| Blog (4 posts) | Template articles | Replace or unpublish. |
| Careers (3 roles) | Template roles | Replace with real openings or unpublish all (the listing shows a friendly "no open roles" message when empty). |
| Legal pages (Privacy, Terms, Licence) | Template legal text | Replace with Techable's own. |
| Footer newsletter | Form is wired to the Contact Form 7 shortcode set in *Techable Settings* | Confirm where subscriptions go. |

---

## 3. Images to replace (all currently template stock)

Upload via **Media**, then assign in the location named. Use WebP or JPG, ≤ 400 KB each unless noted.

| Location | Size (px) | Notes |
|---|---|---|
| Home hero collage (3 images) | 800 × 1000 portrait, 1200 × 800 landscape | *Pages → Home → Hero collage* |
| Home work showcase | 1600 × 900 | Uses each case study's featured image |
| **About page** — 17 template images: team portraits, office/culture photos, award logos, partner logos | Portraits 800 × 1000; logos SVG or PNG on transparent | *Pages → About* fields |
| **Case studies** — featured image (banner + card) | 2000 × 1125 (16:9) | *Work → [project] → Featured image*. Also used as the gallery on other case studies, so every project needs one. |
| **Services** — featured image (banner on the service page, thumbnail on hover rows) | 1600 × 1000 | *Services → [service] → Featured image*. None are set yet — all 39 use 4 rotating template images. |
| Blog — post featured images (10 template images on the listing) | 1600 × 900 | *Posts → Featured image* |
| Open-graph / social preview image | 1200 × 630 | Send to developer (no SEO plugin installed) |
| Favicon / site icon | 512 × 512 PNG | *Appearance → Customize → Site Identity* |

---

## 4. Case study template (what each Work post needs)

- **Title** — client or project name
- **Excerpt** — one sentence summary (shown as the intro lead)
- **Featured image** — 16:9
- **Project date** — e.g. `March – 2026`
- **Category** — Brand Strategy / Digital Marketing / Growth Marketing / Web & Experience (drives the portfolio filters)
- **Body** — write with `Heading 2` sections; each becomes a labelled row. Suggested: *Challenge*, *Approach*, *Outcomes*. Paragraphs and bullet lists are supported.
- Optional fields to ask the developer to enable: *Client name*, *Industry* (the template already displays them when present).

## 5. Service page template (per service)

Each service page shows: hero (title + excerpt), banner image, **Overview** (2 paragraphs) + **Who it's for**, **What's included** (6 bullets), **How we work** (4 steps), **Outcomes** (3 bullets), related work, why-us, **FAQ** (4 Q&As), related services. Supply copy in that shape per service and the developer drops it into `inc/service-copy.php`. Setting a post **Excerpt** overrides the hero summary immediately without developer help.

---

## 6. Already done — no action

- Mega menu, services listing, practice-area hubs, service pages, portfolio with filters, case-study and footer layouts
- Every page has one H1, a meta description, canonical URL, and schema (FAQ, Service, Breadcrumb) where relevant
- No broken links or 404s across 73 crawled pages; legacy template brand ("Markeio") removed
- Old blog/career URLs from the template redirect to the right pages
