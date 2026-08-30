# Odoo / SIH-Style Hackathon Master Execution Guide

## Purpose

This is the consolidated execution guide built from the supplied
**Frontend + AI + Hackathon Resource Guide**, the **Frontend + AI +
Hackathon Winning Playbook**, the additional resources
`animmasterlib.dev`, `50languages.com`, and
`github.com/public-apis/public-apis`, plus the Odoo-focused strategy
discussed earlier.

The guide is organized around **what the team should do, when to do it,
which resource to use, and why**.

> **Core rule:** choose the smallest reliable stack that demonstrates
> the most value. A working product with coherent UX, defensible
> architecture, believable data, and a resilient demo beats a graveyard
> of fashionable libraries.

------------------------------------------------------------------------

## 1. New resources and exactly where they fit

| Resource                                     | Role                                 | Use                                                                                  |
|----------------------------------------------|--------------------------------------|--------------------------------------------------------------------------------------|
| <https://animmasterlib.dev/>                 | Animation/component sourcing         | Ready-made scroll, hero, text, grid, hover, transition, WebGL and 3D patterns        |
| <https://50languages.com/>                   | Localization / education inspiration | Multilingual UX, localization stress testing, education workflows                    |
| <https://github.com/public-apis/public-apis> | API discovery                        | Find external APIs for weather, finance, sports, education, transport, science, etc. |

**Important:** Animmaster Lib contains paid resources, so check the
license before copying anything into a submission. 50LANGUAGES has its
own copyright/licensing terms; use it as a reference and test source
rather than blindly scraping content. The Public APIs repository is a
discovery catalog, not a guarantee that every listed API is stable,
free, authenticated-free, CORS-enabled, or suitable for production.

------------------------------------------------------------------------

# 2. Default Odoo-style hackathon stack

``` text
Next.js / React
+ Tailwind CSS
+ shadcn/ui
+ Radix
+ Supabase
+ PostgreSQL
+ Auth / RLS
+ Zod
+ Gemini
+ OpenRouter fallback
+ NVIDIA alternative
+ Motion
+ Chart.js
+ Luxon
+ Vercel / Cloudflare
+ GitHub
+ Sentry if time permits
```

Optional:

``` text
Floating UI
AOS
GSAP ScrollTrigger
Animmaster
Cloudinary
Resend
Upstash Redis
FastAPI
Hono
OpenCode
Claude Code
CodeRabbit
RAG/vector search
```

Do not use all of these by default. The previous playbook explicitly
recommends changing the stack when the problem demands it.

------------------------------------------------------------------------

# 3. Frontend resource map

## Core UI

### Tailwind CSS

<https://tailwindcss.com/>

Primary styling system.

### shadcn/ui

<https://ui.shadcn.com/>

Default hackathon component system because components are source-owned
and easy to customize.

### Radix

<https://www.radix-ui.com/primitives>

Accessible primitives for dialogs, menus, popovers, tabs and tooltips.

### Headless UI

<https://headlessui.com/>

Unstyled accessible components.

### UIverse

<https://uiverse.io/>

Rapid component inspiration and starting points: buttons, cards,
loaders, inputs, switches and glass-style elements.

### UIverse Galaxy

<https://github.com/uiverse-io/galaxy>

Useful when inspecting the underlying collection/source.

### Magic UI

<https://magicui.design/>

Polished animated components.

### Aceternity UI

<https://ui.aceternity.com/>

Animated React/Tailwind components for hero and marketing sections.

### daisyUI

<https://daisyui.com/>

Fast conventional Tailwind components.

### Flowbite

<https://flowbite.com/>

Fast Tailwind component ecosystem.

**Rule:** choose one primary component system. Do not create a
Frankenstein UI from five unrelated libraries.

------------------------------------------------------------------------

# 4. Animmaster Lib

<https://animmasterlib.dev/>

The site currently presents animated resources covering:

- scroll animations
- mouse effects
- page transitions
- sliders
- hero animations
- grid animations
- WebGL shaders
- backgrounds
- navigation
- hover effects
- text animation
- 3D
- physics
- SVG animation

## Use it when

You already have:

``` text
working product
+
stable design system
```

and need:

``` text
one or two memorable visual interactions
```

### Best assignment

| Need              | Animmaster category |
|-------------------|---------------------|
| Hero              | Hero animations     |
| Product story     | Scroll animation    |
| Feature reveal    | Text animation      |
| Portfolio/gallery | Grid animation      |
| Navigation        | Navigation effects  |
| Premium visual    | WebGL / 3D          |
| Interaction       | Mouse / hover       |
| Page transition   | Page transitions    |

### Do not

Use every flashy component.

The correct pattern is:

``` text
shadcn
+
one motion system
+
1–2 Animmaster showcase effects
```

------------------------------------------------------------------------

# 5. Design semantics

## Odoo default

### 80% Minimalism

### 15% Controlled Neobrutalism

### 5% Glass/Liquid Glass accents

This produces:

``` text
modern SaaS
+
enterprise dashboard
+
technical personality
```

rather than a visually noisy "look what CSS can do" project.

## Theme matrix

| Problem type       | Primary      | Secondary        |
|--------------------|--------------|------------------|
| ERP / enterprise   | Minimalism   | Neobrutalism     |
| Developer tool     | Neobrutalism | Minimalism       |
| FinTech            | Minimalism   | Glass            |
| AI platform        | Minimalism   | Glass            |
| Education          | Minimalism   | Clay             |
| Healthcare         | Minimalism   | Soft clay        |
| Sustainability     | Minimalism   | Organic          |
| Marketplace        | Minimalism   | Bento            |
| Creative portfolio | Asymmetric   | Liquid Glass/Y2K |
| Community          | Minimalism   | Clay             |
| Experimental demo  | Neobrutalism | Y2K              |

### Morphism rules

**Glassmorphism:** premium/futuristic; use for AI, fintech, media and
hero overlays. Do not make every card translucent.

**Liquid Glass:** premium visual demo/hero. Keep restrained because blur
can hurt contrast and performance.

**Neobrutalism:** strong choice for hackathons, developer tools, student
products and indie SaaS.

**Claymorphism:** friendly products, education, productivity and playful
dashboards.

**Skeuomorphism:** only when a physical metaphor improves understanding.

**Minimalism:** safest default for complex or trust-heavy applications.

------------------------------------------------------------------------

# 6. Layout patterns

| Pattern             | Use                                        |
|---------------------|--------------------------------------------|
| F-pattern           | Docs, articles, admin information          |
| Asymmetric          | Creative/product landing pages             |
| Masonry             | Galleries, feeds, project showcases        |
| Bento               | Dashboards, product features, AI platforms |
| Retro/Y2K           | Creative or experimental demos             |
| Hero + feature grid | SaaS/startup/hackathon landing             |
| Sidebar + content   | Dashboards/admin/data-heavy apps           |
| Sticky sections     | Storytelling/process walkthrough           |
| Full-page sections  | Presentation/launch/portfolio              |

**Responsive rule:** design mobile composition deliberately. Do not
merely shrink desktop.

------------------------------------------------------------------------

# 7. Motion decision system

| Need                             | First choice               |
|----------------------------------|----------------------------|
| Simple reveal                    | AOS / IntersectionObserver |
| React state/layout animation     | Motion                     |
| Native scroll-linked animation   | CSS scroll timelines       |
| Cinematic scroll                 | GSAP ScrollTrigger         |
| Ready-made animated component    | Animmaster                 |
| Tooltip/popover positioning      | Floating UI                |
| Simple carousel                  | CSS overflow + scroll snap |
| Vertical-to-horizontal cinematic | GSAP                       |

### Floating UI

<https://floating-ui.com/>

Use for robust tooltip, popover, dropdown, combobox and anchored-menu
positioning.

### AOS

<https://michalsnik.github.io/aos/>

Fast reveal-on-scroll.

### Motion

<https://motion.dev/>

React animation, gestures and layout transitions.

### GSAP ScrollTrigger

<https://gsap.com/docs/v3/Plugins/ScrollTrigger/>

Complex scrub, pin, snap and timeline animation.

### MDN Scroll-driven Animations

<https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Scroll-driven_animations>

Native scroll timelines.

### IntersectionObserver

<https://developer.mozilla.org/en-US/docs/Web/API/IntersectionObserver>

Simple viewport entry/exit detection.

### Lenis

<https://lenis.darkroom.engineering/>

Smooth scrolling; use carefully.

------------------------------------------------------------------------

# 8. Scroll implementation recipes

## Parallax

``` text
Layer A = 1.0x
Layer B = 0.5x
Layer C = 0.25x
```

Prefer transforms.

For serious animation use:

``` text
requestAnimationFrame
or CSS scroll timelines
or Motion
or GSAP
```

## Text reveal

``` text
Text
→ split into words/lines/chars
→ clip-path / transform / opacity
→ view-progress animation
```

Keep real text in the DOM for accessibility.

## Scroll-trigger

Simple:

``` text
IntersectionObserver
```

Continuous progress:

``` text
Motion / GSAP / CSS timeline
```

## Sticky

``` css
position: sticky;
top: 5rem;
```

Use for:

``` text
fixed visual
+
changing explanation
```

## Horizontal scroll

``` css
overflow-x: auto;
scroll-snap-type: x mandatory;
```

Use GSAP for cinematic vertical-to-horizontal effects.

## Progress indicator

Prefer native CSS scroll timelines where acceptable.

------------------------------------------------------------------------

# 9. Frontend utility libraries

### Chart.js

<https://www.chartjs.org/docs/>

Use for:

- KPIs
- line/bar charts
- utilization
- financial trends
- inventory
- booking statistics

### Luxon

<https://moment.github.io/luxon/>

Use for:

- date/time
- time zones
- scheduling
- event ranges
- deadlines

### SweetAlert2

<https://sweetalert2.github.io/>

Use for:

- destructive confirmation
- success/failure feedback
- small confirmation forms

Do not hide important application state inside alerts.

------------------------------------------------------------------------

# 10. API discovery and the Public APIs repository

<https://github.com/public-apis/public-apis>

Use it when a problem benefits from real external data.

Potential categories include:

``` text
weather
maps
finance
sports
education
transport
books
science
government
food
games
utilities
```

## Correct workflow

``` text
Problem
↓
Need external data?
↓
Search Public APIs
↓
Check:
  HTTPS
  auth
  CORS
  rate limits
  terms
  reliability
↓
Test in Postman/Hoppscotch
↓
Create server-side adapter
↓
Normalize response
↓
Cache if needed
↓
Fallback to seeded demo data
```

Never let an unknown third-party API become a single point of failure
for the demo.

------------------------------------------------------------------------

# 11. 50LANGUAGES

<https://50languages.com/>

50LANGUAGES provides language-learning material including lessons,
vocabulary, phrasebook-style content, tests, games and audio.

## Where it helps in hackathons

### Education problems

Use its structure as inspiration for:

``` text
lesson
→ vocabulary
→ practice
→ test
→ progress
```

### Localization testing

Stress-test UI with:

``` text
English
Hindi
German
Spanish
Arabic
Japanese
Chinese
```

Test:

- text expansion
- RTL
- button width
- cards
- navbar
- mobile
- font rendering

### Multilingual product ideas

Good fit for:

- education
- tourism
- migration
- government services
- public accessibility
- multilingual communication

Do not scrape/repackage material without checking its terms.

------------------------------------------------------------------------

# 12. API tools

### Postman

<https://www.postman.com/>

API debugging and collections.

### Hoppscotch

<https://hoppscotch.io/>

Fast browser API testing.

### Bruno

<https://www.usebruno.com/>

Git-friendly API collections.

### OpenAPI

<https://www.openapis.org/>

API contracts and documentation.

### Swagger Editor

<https://editor.swagger.io/>

OpenAPI design/validation.

### Zod

<https://zod.dev/>

Runtime validation.

### tRPC

<https://trpc.io/>

Type-safe TypeScript-to-TypeScript API calls.

------------------------------------------------------------------------

# 13. Backend decision system

### Supabase

<https://supabase.com/>

Default for:

``` text
Postgres
Auth
Storage
Realtime
Edge Functions
```

### Firebase

<https://firebase.google.com/>

Mobile/consumer/realtime/Google ecosystem.

### Appwrite

<https://appwrite.io/>

Open-source backend platform.

### Convex

<https://www.convex.dev/>

Reactive TypeScript backend.

### Hono

<https://hono.dev/>

Tiny edge/serverless APIs.

### FastAPI

<https://fastapi.tiangolo.com/>

Python/AI/ML-heavy backend.

### Express

<https://expressjs.com/>

Conventional Node backend.

------------------------------------------------------------------------

# 14. Database selection

| Need                      | Choice              |
|---------------------------|---------------------|
| Relational workflow       | PostgreSQL          |
| General hackathon default | Supabase Postgres   |
| Serverless Postgres       | Neon                |
| Document data             | Firestore / MongoDB |
| Cache/rate limit          | Upstash Redis       |
| Lightweight edge SQLite   | Turso               |
| Realtime relational       | Supabase            |

Do not introduce multiple databases unless the problem genuinely
requires them.

------------------------------------------------------------------------

# 15. Authentication and RBAC

### Supabase Auth

<https://supabase.com/docs/guides/auth>

### Clerk

<https://clerk.com/>

### Auth.js

<https://authjs.dev/>

### Better Auth

<https://www.better-auth.com/>

Remember:

``` text
Authentication = who are you?
Authorization = what may you do?
```

For Odoo-style systems, prepare:

``` text
ADMIN
MANAGER
OPERATOR
USER
```

and adapt roles to the statement.

Enforce authorization at the server/data boundary.

------------------------------------------------------------------------

# 16. AI API arsenal

### Gemini

<https://ai.google.dev/gemini-api/docs/>

### Google AI Studio

<https://aistudio.google.com/>

### NVIDIA Build

<https://build.nvidia.com/>

### OpenRouter

<https://openrouter.ai/>

### OpenRouter free router

<https://openrouter.ai/openrouter/free/>

### Hugging Face Inference Providers

<https://huggingface.co/docs/inference-providers/pricing>

### Cloudflare Workers AI

<https://developers.cloudflare.com/workers-ai/>

### Groq

<https://console.groq.com/>

### Cerebras

<https://www.cerebras.ai/>

### Together AI

<https://www.together.ai/>

## Provider rule

Never spread provider-specific code through the UI.

Use:

``` ts
generate({
  system,
  messages,
  responseFormat
})
```

Return:

``` ts
{
  text,
  model,
  provider,
  usage
}
```

Then:

``` text
Gemini
OpenRouter
NVIDIA
Other
   ↓
Provider Adapter
   ↓
Application
```

If one provider fails, switch configuration instead of rewriting the
app.

------------------------------------------------------------------------

# 17. RAG and AI search

### LlamaIndex

<https://www.llamaindex.ai/>

### LangChain

<https://www.langchain.com/>

### Chroma

<https://www.trychroma.com/>

### Pinecone

<https://www.pinecone.io/>

### Qdrant

<https://qdrant.tech/>

### Tavily

<https://tavily.com/>

### Exa

<https://exa.ai/>

Architecture:

``` text
documents
→ chunks
→ embeddings
→ vector store
→ top-k retrieval
→ context
→ LLM
→ answer/citations
```

Use RAG only when retrieval is actually necessary. Small structured
datasets are often better handled with SQL/filtering.

------------------------------------------------------------------------

# 18. Files, email and observability

### Cloudinary

<https://cloudinary.com/>

Images/video/transformation.

### Supabase Storage

<https://supabase.com/docs/guides/storage>

Authenticated object storage.

### UploadThing

<https://uploadthing.com/>

Fast file uploads.

### Resend

<https://resend.com/>

Transactional email.

### Sentry

<https://sentry.io/>

Error and performance monitoring.

------------------------------------------------------------------------

# 19. Deployment

### Vercel

<https://vercel.com/>

Default for Next.js.

### Cloudflare Workers

<https://developers.cloudflare.com/workers/>

Edge/serverless.

### Cloudflare Pages

<https://pages.cloudflare.com/>

Static/modern deployment.

### Render

<https://render.com/>

Custom Node/Python services.

### Railway

<https://railway.com/>

Fast backend deployment.

### Docker

<https://www.docker.com/>

Reproducible environments.

Deploy early. A local application at hour 18 is not a deployed hackathon
application.

------------------------------------------------------------------------

# 20. Agentic coding stack

### Claude Code

<https://docs.claude.com/en/docs/claude-code/overview>

Repository-level implementation/debugging.

### OpenCode

<https://opencode.ai/docs>

Multi-provider coding agent.

### CodeRabbit

<https://www.coderabbit.ai/>

AI-assisted PR review.

### Google Antigravity

<https://www.antigravity.google/>

Agent-oriented development ecosystem.

### Stitch

<https://stitch.withgoogle.com/>

AI UI generation and design iteration.

Stitch can be used to explore 2–3 design directions before freezing the
design system, then exported toward Antigravity for continued
development.

------------------------------------------------------------------------

# 21. Agent loop

``` text
ACCEPTANCE CRITERIA
↓
INSPECT REPOSITORY
↓
PLAN
↓
IMPLEMENT ONE VERTICAL SLICE
↓
BUILD / TEST
↓
INSPECT GIT DIFF
↓
REVIEW
↓
FIX
↓
COMMIT
↓
REPEAT
```

Optional GSD search:

<https://github.com/search?q=get+shit+done+claude+code&type=repositories>

Optional Ralph Loop search:

<https://github.com/search?q=ralph+loop+claude+code&type=repositories>

Treat these as workflow patterns, not magic switches.

Never give an agent unrestricted destructive permissions around secrets
or production credentials.

------------------------------------------------------------------------

# 22. Claude reel "secret codes"

The claimed strings were:

``` text
/ghost
ARTIFACTS
OODA
L99
/godmode
```

Correct usage:

- `/ghost` — unverified; do not treat as an official AI-detector bypass.
- `ARTIFACTS` — useful capability category, not a magic multiplier.
- `OODA` — useful explicit decision framework.
- `L99` — unverified.
- `/godmode` — unverified.

Use explicit instructions instead:

``` text
Act as a senior frontend engineer.

Before coding:
1. State assumptions.
2. Identify constraints.
3. Propose the simplest robust architecture.
4. Flag accessibility/performance risks.
5. Implement only after the plan is clear.
6. Provide tests and edge cases.
7. Do not invent APIs or facts.
```

------------------------------------------------------------------------

# 23. Automated resume workflow

Resources:

- <https://docs.n8n.io/>
- <https://learn.n8n.io/>
- <https://docs.overleaf.com/>
- <https://docs.claude.com/>

Architecture:

``` text
Form
↓
Job Description + Base Resume
↓
n8n
↓
Claude
↓
Structured Resume Data
↓
LaTeX Template
↓
Overleaf
↓
PDF
```

Critical constraint:

**Never invent achievements, employers, dates, technologies, metrics or
certifications.**

Add:

``` text
JD
↓
Keyword analysis
↓
Missing keywords
↓
Claude rewrite
↓
ATS risk report
```

This belongs in the career automation toolkit unless the hackathon
problem itself is recruitment-oriented.

------------------------------------------------------------------------

# 24. Freelancing and problem discovery

### Contra

<https://contra.com/>

### PeoplePerHour

<https://www.peopleperhour.com/>

### Toptal

<https://www.toptal.com/>

Sell outcomes, not generic skills.

Bad:

``` text
"I do frontend."
```

Better:

``` text
"I build responsive SaaS dashboards in React/Next.js."
```

Problem portals such as the Razorpay example are useful for practicing
real constraints, but verify the current portal URL before relying on
it.

------------------------------------------------------------------------

# 25. Odoo problem-statement DNA

The previously discussed 2024/2025 examples point toward a repeated
pattern:

``` text
real-world problem
+
identifiable users
+
multiple roles
+
CRUD
+
search/filter
+
state transitions
+
approval
+
notifications
+
dashboard
+
data modelling
```

The recurring categories discussed earlier included:

- crime reporting
- library management
- skill exchange
- Q&A
- clothing exchange
- sports booking
- HRMS

The exact surprise statement should not be guessed. Prepare reusable
architectures instead.

------------------------------------------------------------------------

# 26. 2026 calibration: AssetFlow

Public 2026 material shows an **AssetFlow / Enterprise Asset & Resource
Management** style problem centered on:

``` text
Departments
Employees
Assets
Allocations
Bookings
Maintenance
Audits
Reports
RBAC
Notifications
```

One public implementation uses a pattern involving:

``` text
React
Express
Zod
Prisma
PostgreSQL
RBAC
transactional workflows
```

This is a valuable calibration case because it demonstrates the type of
enterprise workflow that can appear in an Odoo-style surprise challenge.

Use it as a pattern, not as something to copy.

------------------------------------------------------------------------

# 27. Five architectures to prepare

## A. Enterprise management

``` text
Auth
→ RBAC
→ Dashboard
→ Entities
→ CRUD
→ Search
→ Filters
→ Workflow
→ Approval
→ Notifications
→ Reports
→ Audit
```

Use for:

- asset management
- HRMS
- inventory
- maintenance
- departmental systems

## B. Booking

``` text
Users
→ Resources
→ Availability
→ Calendar
→ Conflict Detection
→ Booking
→ Confirmation
→ Notification
→ Admin
```

Use for:

- rooms
- sports
- vehicles
- equipment
- labs
- appointments

## C. Marketplace

``` text
Profiles
→ Listings
→ Search
→ Filters
→ Requests
→ Transactions
→ Ratings
→ Moderation
```

## D. Community

``` text
Profiles
→ Posts
→ Comments
→ Votes
→ Tags
→ Notifications
→ Moderation
→ Search
```

## E. AI business workflow

``` text
Business Data
→ Retrieval / Analysis
→ AI
→ Recommendation
→ Human Approval
→ Action
→ Audit Log
```

------------------------------------------------------------------------

# 28. Team task distribution — 4 people

## Member 1 — Product + Architecture

Own:

- problem interpretation
- acceptance criteria
- data model
- architecture
- API contract
- integration decisions
- demo narrative

## Member 2 — Frontend + UI/UX

Own:

- Stitch
- design system
- shadcn
- responsive UI
- dashboard
- animation
- visual polish

Use:

``` text
Tailwind
shadcn
Radix
UIverse
Animmaster
Motion
GSAP only when necessary
```

## Member 3 — Backend + Database

Own:

- schema
- auth
- RBAC
- APIs
- validation
- workflows
- transactions
- seed data
- error handling

Use:

``` text
Supabase
Postgres
Zod
REST/OpenAPI
or tRPC
```

## Member 4 — AI + Integrations + QA

Own:

- AI provider
- Public APIs discovery
- external integrations
- RAG if needed
- email
- uploads
- testing
- deployment
- fallback mode

Use:

``` text
Gemini
OpenRouter
NVIDIA
Public APIs
Resend
Cloudinary
Sentry
Vercel/Cloudflare
```

Everyone still reviews the complete system.

------------------------------------------------------------------------

# 29. Three-person team

### Person 1

Product + architecture + backend

### Person 2

Frontend + UI/UX + animation

### Person 3

AI + integrations + QA + deployment

All three participate in architecture, testing and demo.

------------------------------------------------------------------------

# 30. Actual hackathon task distribution

## 0–60 minutes — DECIDE

Everyone:

``` text
WHO
WHAT
WHY
INPUT
PROCESS
OUTPUT
ROLES
CONSTRAINTS
SUCCESS METRIC
```

Product lead:

``` text
acceptance criteria
```

Frontend:

``` text
visual direction
```

Backend:

``` text
schema
```

AI/integration:

``` text
external APIs + AI opportunities
```

------------------------------------------------------------------------

## 60–180 minutes — DESIGN + SKELETON

Frontend:

``` text
Stitch
→ 2–3 directions
→ freeze one
→ design tokens
```

Backend:

``` text
database
auth
roles
entities
seed data
```

AI/integration:

``` text
provider adapter
API adapter
environment variables
fallback/mock data
```

Architecture lead:

``` text
API contract
workflow
acceptance checklist
```

------------------------------------------------------------------------

# 31. 3–8 hours — VERTICAL SLICE

Build:

``` text
Login
→ Dashboard
→ Core action
→ Backend
→ Database
→ Result
```

This is more valuable than building five disconnected pages.

Assign:

- Floating UI → popovers/dropdowns/tooltips
- Chart.js → standard charts
- Luxon → time/date logic
- SweetAlert2 → confirmation
- Public APIs → external data
- Zod → validation

------------------------------------------------------------------------

# 32. 8–16 hours — MAKE IT CONVINCING

Add:

- responsive behavior
- loading states
- empty states
- error states
- validation
- notifications
- real-looking seed data
- one standout interaction
- one high-impact animation
- API fallback

Good standout interactions:

``` text
sticky workflow
scroll reveal
bento transition
horizontal showcase
interactive chart
calendar
live status
drag/drop
```

Choose one or two.

------------------------------------------------------------------------

# 33. Final hours — HARDEN

### Security

``` text
No frontend secrets
RBAC enforced
RLS/authorization
Webhook verification
Input validation
Upload validation
AI prompt-injection handling
Synthetic demo data
```

### Quality

``` text
No console errors
No broken images
No overflow
No dead buttons
No empty states in demo
No missing seed data
No broken API
```

### Deployment

Deploy early and test the deployed version from a clean browser.

------------------------------------------------------------------------

# 34. 24-hour plan

| Time   | Target                                                          |
|--------|-----------------------------------------------------------------|
| 0–1h   | Problem, user, demo sentence, acceptance criteria, architecture |
| 1–2h   | Wireframe/design, repo, deployed skeleton                       |
| 2–6h   | End-to-end vertical slice                                       |
| 6–10h  | DB/auth/API/AI + error states                                   |
| 10–14h | Responsive UI + design system + motion                          |
| 14–18h | Testing + fallback + security + performance                     |
| 18–21h | Typography + spacing + micro-interactions + data                |
| 21–23h | Demo + screenshots/video + README + architecture                |
| 23–24h | Freeze + deploy + clean-browser test                            |

------------------------------------------------------------------------

# 35. 8-hour virtual round plan

``` text
0–1h   Understand + architecture + scope freeze
1–2h   Scaffold + DB + UI shell + deploy
2–5h   Core vertical slice
5–6h   Validation + errors + responsive
6–7h   Visual polish + one standout interaction
7–8h   Testing + demo + submission
```

Do not attempt the full product.

Build the most convincing 60-second experience.

------------------------------------------------------------------------

# 36. Odoo application shell to keep ready

``` text
app/
  dashboard/
  users/
  resources/
  bookings/
  approvals/
  notifications/
  reports/
  settings/

components/
  ui/
  forms/
  tables/
  charts/
  dialogs/
  navigation/
  status/

lib/
  auth/
  db/
  api/
  ai/
  validation/
  date/
  notifications/

types/
  domain/
  api/

supabase/
  migrations/
  seed/
```

Adapt names to the problem.

------------------------------------------------------------------------

# 37. Components to have ready

``` text
Sidebar
Navbar
Command Palette
Modal
Drawer
Dropdown
Tabs
Data Table
Search
Filter
Pagination
Calendar
Date Picker
Kanban
Timeline
Stats Cards
Charts
Empty State
Loading Skeleton
Error State
Confirmation Dialog
File Upload
Avatar
Badge
Status Indicator
Toast
```

------------------------------------------------------------------------

# 38. Generic data patterns

## Entity

``` text
id
created_at
updated_at
created_by
status
```

## Workflow

``` text
id
requester_id
assignee_id
status
submitted_at
reviewed_at
completed_at
```

## Audit

``` text
id
actor_id
entity_type
entity_id
action
old_value
new_value
timestamp
```

## Notification

``` text
id
user_id
type
title
message
read
created_at
```

------------------------------------------------------------------------

# 39. AI that actually makes sense

Good:

``` text
summarization
classification
recommendation
document extraction
semantic search
report generation
anomaly explanation
smart suggestions
```

Weak:

``` text
AI chatbot because the judges like AI
```

Strong:

``` text
Business data
→ deterministic rules
→ AI enrichment
→ human approval
→ action
```

------------------------------------------------------------------------

# 40. Public API rule

Use external APIs when external information creates actual product
value.

Always:

``` text
External API
→ adapter
→ normalized internal schema
→ application
```

Never:

``` text
UI
→ random third-party API
```

Build a fallback:

``` text
Live API
   ↓ failure
Seed/demo data
```

------------------------------------------------------------------------

# 41. When to use 50LANGUAGES

Use when the problem involves:

``` text
education
language
migration
tourism
public service
multilingual accessibility
```

Use it for:

- lesson structure
- vocabulary
- phrasebook concepts
- tests
- progress
- multilingual UI testing

Test:

``` text
English
Hindi
Arabic
German
Japanese
Chinese
```

especially for RTL and text expansion.

------------------------------------------------------------------------

# 42. When to use Animmaster

Use after the core product works.

Best phase:

``` text
10–14h
```

unless animation is the product itself.

Use for:

``` text
hero
feature reveal
page transition
grid
hover
text
background
3D
```

Pick one or two excellent effects.

------------------------------------------------------------------------

# 43. When to use RAG

Ask:

``` text
Does the application need retrieval from a meaningful document/data collection?
```

If no:

``` text
Do not use RAG.
```

If yes:

``` text
Storage
→ chunk
→ embed
→ vector DB
→ retrieve
→ LLM
```

------------------------------------------------------------------------

# 44. When to use an agent

Use an agent when the task involves:

``` text
multiple tool calls
+
planning
+
uncertain natural-language decisions
```

Do not use an agent when:

``` text
if/else
+
database query
+
deterministic workflow
```

is sufficient.

------------------------------------------------------------------------

# 45. Security pre-demo audit

- [ ] API keys only in server/edge secrets
- [ ] RLS/authorization enforced
- [ ] RBAC enforced
- [ ] Webhooks verified
- [ ] Zod/input validation
- [ ] Upload size/type validation
- [ ] AI input treated as untrusted
- [ ] Demo data synthetic
- [ ] No secrets committed
- [ ] `.env` ignored
- [ ] Agent permissions limited

------------------------------------------------------------------------

# 46. 60-second demo

``` text
0–10s  Problem
10–20s Solution
20–45s Live core journey
45–55s Differentiator
55–60s Impact
```

Do not spend 40 seconds explaining the tech stack before showing the
product.

------------------------------------------------------------------------

# 47. Judge-facing architecture explanation

``` text
Problem
→ Users
→ Workflow
→ Architecture
→ Technology choice
→ Security
→ Scalability
→ Impact
```

The judges do not care that you used seventeen libraries. They care that
the product works, the problem matters, and your choices make sense.

------------------------------------------------------------------------

# 48. Final decision table

| Need                           | Reach for                   |
|--------------------------------|-----------------------------|
| Fast components                | shadcn / UIverse            |
| Animated components            | Animmaster                  |
| Accessible primitives          | Radix / Headless UI         |
| Simple scroll                  | AOS / IntersectionObserver  |
| React motion                   | Motion                      |
| Cinematic scroll               | GSAP                        |
| Native scroll                  | CSS scroll timelines        |
| Floating UI                    | Floating UI                 |
| Charts                         | Chart.js                    |
| Dates/timezones                | Luxon                       |
| Confirmations                  | SweetAlert2                 |
| AI UI                          | Stitch                      |
| Coding agent                   | Claude Code / OpenCode      |
| Review                         | CodeRabbit                  |
| Workflow automation            | n8n                         |
| Resume automation              | n8n + Claude + Overleaf     |
| Backend                        | Supabase                    |
| Mobile/Google ecosystem        | Firebase                    |
| Reactive TS                    | Convex                      |
| Python AI                      | FastAPI                     |
| Edge API                       | Hono                        |
| SQL                            | Postgres                    |
| Cache/rate limit               | Upstash Redis               |
| Vector search                  | Qdrant/Pinecone/Chroma      |
| RAG                            | LlamaIndex                  |
| Search                         | Tavily/Exa                  |
| AI fallback                    | OpenRouter                  |
| Gemini                         | Gemini API / AI Studio      |
| NVIDIA inference               | NVIDIA Build/NIM            |
| Low latency                    | Groq/Cerebras               |
| Open model inference           | Hugging Face/Together       |
| Edge AI                        | Cloudflare Workers AI       |
| External API discovery         | Public APIs GitHub          |
| API testing                    | Postman/Hoppscotch/Bruno    |
| API contract                   | OpenAPI/Swagger             |
| Validation                     | Zod                         |
| Type-safe TS API               | tRPC                        |
| Files                          | Supabase Storage            |
| Image/video                    | Cloudinary                  |
| Uploads                        | UploadThing                 |
| Email                          | Resend                      |
| Monitoring                     | Sentry                      |
| Next.js deploy                 | Vercel                      |
| Edge deploy                    | Cloudflare                  |
| Custom backend deploy          | Render/Railway              |
| Reproducible env               | Docker                      |
| Freelancing                    | Contra/PeoplePerHour/Toptal |
| Language/education inspiration | 50LANGUAGES                 |

------------------------------------------------------------------------

# 49. Final Odoo default

If the statement says:

> "Build a system for managing X."

Immediately translate it into:

``` text
AUTH
RBAC
ENTITIES
CRUD
SEARCH
FILTER
WORKFLOW
APPROVAL
NOTIFICATION
DASHBOARD
REPORTING
AUDIT LOG
```

Then ask:

``` text
Where can AI genuinely help?
Where does external data add value?
What is the one memorable interaction?
What can be shown in 60 seconds?
```

------------------------------------------------------------------------

# 50. Final frontend default

``` text
Style:
80% Minimalism
15% Neobrutalism
5% Glass

Shell:
Sidebar + content

Dashboard:
Bento overview

Data:
Tables + cards + charts

Workflow:
Timeline + status + approvals

Landing:
Hero + feature grid

Story:
Sticky section

Motion:
Motion

Premium:
Animmaster / GSAP

Components:
shadcn + Radix

Validation:
Zod
```

------------------------------------------------------------------------

# 51. Final AI default

``` text
Primary:
Gemini

Fallback:
OpenRouter

Alternative:
NVIDIA

Coding:
Claude Code / OpenCode

Review:
CodeRabbit

RAG:
Only when required

Provider abstraction:
YES

Secret keys:
SERVER ONLY
```

------------------------------------------------------------------------

# 52. Final backend default

``` text
Next.js / React
        ↓
Supabase
        ↓
PostgreSQL
        ↓
Auth + RLS
        ↓
Storage / Realtime
        ↓
Edge Functions
        ↓
AI Provider Adapter
```

Use FastAPI when Python/ML genuinely warrants it.

------------------------------------------------------------------------

# 53. Final winning loop

``` text
PROBLEM
↓
USER
↓
WORKFLOW
↓
MVP
↓
DESIGN
↓
VERTICAL SLICE
↓
DATA
↓
AI/API ENRICHMENT
↓
VALIDATION
↓
MOTION
↓
SECURITY
↓
DEPLOY
↓
DEMO
```

The actual mental model:

> Build boring infrastructure. Build excellent UX. Use AI selectively.
> Use animation deliberately. Keep provider fallbacks. Deploy early.
> Test the happy path. Then test what happens when everything goes to
> shit.

------------------------------------------------------------------------

# 54. Pre-hackathon checklist

## Repository

- [ ] React/Next starter
- [ ] Tailwind
- [ ] shadcn
- [ ] Supabase pattern
- [ ] Zod
- [ ] Chart.js
- [ ] Luxon
- [ ] Motion
- [ ] API adapter
- [ ] AI provider adapter
- [ ] deployment
- [ ] GitHub

## UI

- [ ] Sidebar
- [ ] Navbar
- [ ] Table
- [ ] Search
- [ ] Filter
- [ ] Modal
- [ ] Toast
- [ ] Form
- [ ] Calendar
- [ ] Chart
- [ ] Empty state
- [ ] Loading state
- [ ] Error state
- [ ] Mobile layout

## Backend

- [ ] Auth
- [ ] RBAC
- [ ] Database
- [ ] RLS
- [ ] Validation
- [ ] CRUD
- [ ] Workflow
- [ ] Notifications
- [ ] Audit log

## AI

- [ ] Gemini
- [ ] OpenRouter fallback
- [ ] NVIDIA alternative
- [ ] Provider adapter
- [ ] Prompt templates
- [ ] Structured output
- [ ] Failure fallback

## External APIs

- [ ] Public APIs catalog
- [ ] Postman/Hoppscotch
- [ ] API adapter
- [ ] Rate-limit awareness
- [ ] Demo fallback

## Visuals

- [ ] Theme
- [ ] Typography
- [ ] Spacing
- [ ] Radius
- [ ] Shadow
- [ ] Motion system
- [ ] One standout interaction

## Submission

- [ ] Deployed URL
- [ ] Clean-browser test
- [ ] Mobile test
- [ ] Demo account
- [ ] Seed data
- [ ] README
- [ ] Architecture diagram
- [ ] 60-second demo
- [ ] No console errors
- [ ] No exposed secrets

------------------------------------------------------------------------

# 55. Final rule

> **Do not try to prove that your team knows the most technologies.
> Prove that you can take an unfamiliar real-world problem, understand
> it quickly, model it correctly, build a usable solution under
> pressure, make intelligent technology choices, and communicate the
> result clearly.**

When the surprise problem appears:

``` text
DO NOT PANIC.

CLASSIFY:

Enterprise?
Booking?
Marketplace?
Community?
AI workflow?

↓

LOAD TEMPLATE.

↓

ADAPT DOMAIN.

↓

SHIP VERTICAL SLICE.

↓

POLISH.

↓

TEST.

↓

DEMO.
```
