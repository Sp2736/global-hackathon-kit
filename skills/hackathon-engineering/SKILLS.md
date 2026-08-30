---
name: hackathon-engineering
description: Applies a reusable product, architecture, frontend, backend, AI, API, testing, security, deployment, and demo workflow for hackathons and general software projects. Use when building, planning, debugging, reviewing, polishing, or shipping web applications, especially enterprise/SaaS/Odoo-style workflows.
---

# Hackathon Engineering Skill

## Mission

Build reliable, demonstrable software quickly without turning the project into a technology museum.

The priority order is:

```text
Correct problem
→ coherent workflow
→ working vertical slice
→ reliable data/backend
→ good UX
→ useful AI/API integrations
→ polish
→ demo
```

---

## 1. First response to a new project

Before writing code:

### Inspect

- repository tree
- framework
- package manager
- existing README
- existing rules/skills
- entry points
- database/schema
- API layer
- auth
- environment configuration
- existing UI components
- test/lint/build scripts

### Then produce

```text
Problem:
Users:
Core workflow:
Roles:
Inputs:
Outputs:
Constraints:
Acceptance criteria:
Existing architecture:
Proposed minimal architecture:
Risks:
Implementation order:
```

If requirements are incomplete, explicitly mark assumptions.

---

## 2. Problem classification

For a hackathon surprise statement, classify it into one of these reusable shapes.

### Enterprise management

```text
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

Examples:

- assets
- HR
- inventory
- maintenance
- departmental management

### Booking/scheduling

```text
Users
→ Resources
→ Availability
→ Calendar
→ Conflict detection
→ Booking
→ Confirmation
→ Notification
→ Admin
```

### Marketplace

```text
Profiles
→ Listings
→ Search
→ Filters
→ Request
→ Transaction
→ Rating
→ Moderation
```

### Community

```text
Profiles
→ Posts
→ Comments
→ Votes
→ Tags
→ Notifications
→ Moderation
→ Search
```

### AI business workflow

```text
Business data
→ deterministic processing
→ AI enrichment
→ human approval
→ action
→ audit
```

Do not force the problem into a template if the domain clearly needs another architecture.

---

## 3. Vertical-slice rule

Build one complete journey before broadening scope:

```text
Login
→ dashboard
→ core action
→ API/backend
→ database
→ result
```

A single working workflow is more valuable than five disconnected screens.

---

## 4. Default stack selection

For a new TypeScript web project, consider:

```text
Next.js/React
Tailwind
shadcn
Radix
Supabase/Postgres
Zod
Chart.js
Luxon
Motion
```

For AI:

```text
Gemini
→ OpenRouter fallback
→ another provider when justified
```

For deployment:

```text
Vercel
or Cloudflare
```

For custom Python/ML:

```text
FastAPI
```

For edge APIs:

```text
Hono
```

Always inspect the actual project before changing its stack.

---

## 5. Frontend implementation

### Design system first

Freeze:

- typography
- color roles
- spacing scale
- radii
- shadows
- button styles
- card styles
- status colors
- form states
- motion rules

Default enterprise/hackathon style:

```text
80% minimalism
15% controlled neobrutalism
5% glass/liquid glass
```

### Component priority

1. Existing project components
2. shadcn/Radix
3. UIverse for inspiration/source examples
4. Magic UI/Aceternity for selected showcase pieces
5. Animmaster for selected animation components

Do not mix five visual systems.

### Required states

Every meaningful feature should consider:

```text
loading
success
empty
error
disabled
permission denied
```

---

## 6. Animation selection

Choose one primary motion system.

### Simple

```text
CSS + IntersectionObserver/AOS
```

### React

```text
Motion
```

### Cinematic

```text
GSAP ScrollTrigger
```

### Ready-made showcase

```text
Animmaster
```

### Rules

- motion must serve hierarchy or comprehension
- respect reduced-motion preferences
- do not animate essential information out of reach
- avoid expensive layout-triggering animation
- prefer transforms/opacity
- do not add animation until the feature works

For Animmaster, verify licensing before copying paid/source assets into a submission.

---

## 7. API discovery

When external data is useful:

```text
Search public-apis catalog
→ inspect candidate API
→ verify auth/CORS/rate limits/terms
→ test
→ create adapter
→ normalize response
→ cache if useful
→ provide fallback
```

Reference:

https://github.com/public-apis/public-apis

Never bind the UI directly to an unstable third-party response shape.

---

## 8. API contract

Prefer:

```text
route/controller
→ validation
→ service
→ repository/database
```

Use Zod at boundaries.

For TypeScript end-to-end applications, tRPC can be considered when it genuinely simplifies the system.

For explicit contracts, use OpenAPI.

---

## 9. Database

Prefer relational modelling for workflow-heavy applications.

Common reusable entities:

```text
User
Role
Organization/Department
Resource
Request
Booking
Approval
Notification
AuditLog
Attachment
```

Common reusable fields:

```text
id
created_at
updated_at
created_by
status
```

Do not add a second database until the requirement is real.

---

## 10. RBAC

Model:

```text
role
permissions
resource
action
```

Typical starting roles:

```text
ADMIN
MANAGER
OPERATOR
USER
```

Adapt to the actual domain.

Enforce authorization server-side/data-side. Hidden buttons are UX, not security.

---

## 11. AI integration

Only use AI for a real task.

Good:

- classification
- extraction
- summarization
- recommendation
- natural-language reports
- semantic retrieval
- anomaly explanation
- intelligent suggestions

Weak:

- generic chatbot with no workflow value

Use a provider adapter.

Example conceptual interface:

```ts
generate({
  system,
  messages,
  responseFormat
})
```

Return normalized metadata:

```ts
{
  text,
  model,
  provider,
  usage
}
```

Validate structured AI output before using it to mutate data.

---

## 12. RAG

Use RAG only when retrieval is necessary.

```text
documents
→ chunks
→ embeddings
→ vector store
→ top-k retrieval
→ context
→ model
→ validated response
```

If the dataset is small and structured, SQL/filtering is usually simpler.

Candidate resources:

- LlamaIndex
- LangChain
- Chroma
- Qdrant
- Pinecone
- Tavily
- Exa

---

## 13. Localization

When language/accessibility is relevant, use multilingual stress tests.

Reference:

https://50languages.com/

Test at least:

```text
English
Hindi
German
Arabic
Japanese
Chinese
```

Check:

- text expansion
- RTL
- buttons
- cards
- navigation
- forms
- mobile
- typography

Do not redistribute third-party learning content without checking licensing/terms.

---

## 14. Agent coding loop

For every non-trivial task:

```text
INSPECT
→ PLAN
→ IMPLEMENT
→ BUILD/TEST
→ DIFF REVIEW
→ FIX
→ REPEAT
```

Use agentic tools for repository-scale work, but keep acceptance criteria explicit.

Good agent tasks:

- scaffold feature
- implement known component
- refactor a bounded module
- write tests
- diagnose build errors
- review a diff
- update documentation

Bad agent behavior:

- uncontrolled architecture redesign
- broad dependency replacement without justification
- deleting tests to make the build pass
- changing unrelated files
- inventing APIs
- committing secrets

---

## 15. Testing

Minimum hackathon loop:

```text
typecheck
→ lint
→ unit tests where present
→ build
→ manual happy path
→ manual error path
→ mobile/responsive check
→ clean-browser deployed check
```

When fixing a bug:

1. reproduce it
2. identify root cause
3. make the smallest robust fix
4. add/update regression coverage where practical
5. rerun validation

Never claim a test passed unless it actually ran.

---

## 16. Security

Before demo/submission:

- no secrets in client bundle
- `.env` ignored
- RBAC enforced
- RLS/authorization checked
- user input validated
- file uploads restricted
- webhooks verified
- AI outputs validated
- prompt injection considered
- external documents treated as untrusted
- audit logs for meaningful state changes
- synthetic demo data
- least-privilege agent/tool access

---

## 17. Performance

Check:

- bundle size
- image optimization
- lazy loading
- unnecessary client components
- expensive re-renders
- unbounded lists
- animation frame rate
- API waterfalls
- duplicate requests

Prefer simple optimization that can be verified.

---

## 18. Demo engineering

The application must have:

```text
demo account
seed data
stable core path
fallback data
no dependency on an unverified live service
```

60-second demo:

```text
0–10s  Problem
10–20s Solution
20–45s Core journey
45–55s Differentiator
55–60s Impact
```

Do not spend the first half of the demo listing technologies.

---

## 19. Hackathon timeboxing

### 0–1h

```text
Problem
User
Workflow
Acceptance criteria
Architecture
```

### 1–2h

```text
UI direction
Repo
DB skeleton
Deployment skeleton
```

### 2–6h

```text
Vertical slice
```

### 6–10h

```text
Auth
API
DB
AI/integrations
```

### 10–14h

```text
Responsive UI
Motion
Visual system
```

### 14–18h

```text
Testing
Security
Fallbacks
Performance
```

### 18–21h

```text
Polish
Seed data
Demo path
```

### 21–23h

```text
README
Architecture diagram
Demo recording/script
```

### 23–24h

```text
Freeze
Deploy
Clean-browser test
```

For an 8-hour round, compress aggressively and freeze scope after the first hour.

---

## 20. Reference decision table

| Need | First choice |
|---|---|
| Component quickly | shadcn / UIverse |
| Accessible primitive | Radix |
| Animated component | Animmaster |
| Simple reveal | AOS / IntersectionObserver |
| React animation | Motion |
| Cinematic scroll | GSAP |
| Native scroll-linked animation | CSS scroll timeline |
| Tooltip/popover | Floating UI |
| Dashboard chart | Chart.js |
| Date/time | Luxon |
| Confirmation | SweetAlert2 |
| AI UI concept | Stitch |
| Repository coding | Claude Code / OpenCode |
| PR review | CodeRabbit |
| Automation | n8n |
| AI resume | n8n + Claude + Overleaf |
| General backend | Supabase |
| Python AI | FastAPI |
| Edge API | Hono |
| API discovery | Public APIs |
| API testing | Postman/Hoppscotch/Bruno |
| Validation | Zod |
| API contract | OpenAPI |
| AI primary | Gemini |
| AI fallback | OpenRouter |
| Alternative inference | NVIDIA |
| RAG | LlamaIndex |
| Vector DB | Qdrant/Pinecone/Chroma |
| Search | Tavily/Exa |
| Email | Resend |
| File/media | Supabase Storage/Cloudinary |
| Monitoring | Sentry |
| Deployment | Vercel/Cloudflare |

---

## 21. Definition of done

Do not say "done" until:

```text
Acceptance criteria pass
+
core workflow works
+
validation exists
+
error states exist
+
authorization is enforced
+
tests/build/typecheck were run where applicable
+
diff inspected
+
no secrets/debug code
+
deployed version checked when relevant
```

---

## 22. Final instruction

Optimize for:

```text
clarity
reliability
speed
maintainability
demoability
```

not:

```text
technology count
```

The best hackathon implementation is usually:

```text
boring infrastructure
+
excellent workflow
+
strong UI
+
one memorable interaction
+
selective AI
+
reliable fallback
+
clean demo
```
