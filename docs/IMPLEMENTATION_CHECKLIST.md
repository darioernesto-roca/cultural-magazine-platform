# Implementation Checklist

Phase-by-phase tracker derived from `CODEX_PROJECT_RULES.md` (source of truth).

**Rules that apply to every phase**

- Work on **one phase at a time**.
- At the end of each phase, report: what was completed, files changed, commands run, how to test, unresolved issues, and what needs validation.
- **Dario must validate a phase before the next one starts.** Tick the "Owner validated" box only after that sign-off.
- Never commit `.env`, never hardcode credentials, never hardcode a final brand name, never use `Caribe` in technical names.

**Legend:** `[x]` done · `[ ]` pending · `[~]` partially done / blocked (see note)

---

## Phase 0 — Repository Preparation ✅

- [x] Confirm current directory and Git status
- [x] Create / update `.gitignore`
- [x] Add `CODEX_PROJECT_RULES.md` to the repository
- [x] Create basic `README.md`
- [x] Clean Git status
- [x] **Owner validated** (merged in PR #1)

---

## Phase 1 — Laravel Project Initialization ⏳

- [x] Install Laravel (12.x) with current official instructions
- [x] Configure `.env.example` (APP_NAME, APP_URL, `pgsql`, `cultural_magazine_platform`)
- [x] Generate app key in local `.env` (not committed)
- [x] Install frontend dependencies (Vite + Tailwind)
- [x] Commit initial Laravel setup
- [ ] Install / start local PostgreSQL and create database `cultural_magazine_platform`
- [ ] Run `php artisan migrate` successfully against PostgreSQL
- [ ] Confirm the app runs locally (`php artisan serve` → http://localhost:8000)
- [ ] Confirm `npm run dev` / `npm run build` succeeds
- [ ] Update `README.md` with local setup instructions
- [ ] Update `docs/technical/phase-1-initialization-report.md` (blocker resolved)
- [ ] **Owner validated**

---

## Phase 2 — Filament Installation

- [ ] Check current Filament docs and pick the stable version compatible with Laravel 12
- [ ] `composer require filament/filament` (pinned to the chosen major)
- [ ] Create the admin panel (`php artisan filament:install --panels`)
- [ ] Create the admin user (`php artisan make:filament-user`)
- [ ] Confirm `/admin` loads and login works
- [ ] Configure production access rules (`User implements FilamentUser` + `canAccessPanel()`)
- [ ] Do **not** create resources yet
- [ ] **Owner validated**

---

## Phase 3 — Database Models and Migrations

### Models + migrations

- [ ] `Author` — name, slug, bio, avatar_path, website_url, instagram_url, x_url, linkedin_url, is_active
- [ ] `Category` — name, slug, description, sort_order, is_active
- [ ] `EditorialPillar` — name, slug, description, source_folder, notes, is_active
- [ ] `City` — name, slug, department, region, description, latitude (nullable), longitude (nullable)
- [ ] `Tag` — name, slug
- [ ] `Post` — title, slug, subtitle, excerpt, content, featured_image_path, category_id, editorial_pillar_id, author_id, city_id, content_type, status, is_featured, published_at, seo_title, seo_description, reading_time
- [ ] `Post` editorial flags (boolean): requires_fact_check, contains_practical_info, contains_prices, contains_schedules, contains_sensitive_social_context
- [ ] `Post` soft deletes (optional — decide)
- [ ] Pivot table `post_tag`
- [ ] Unique indexes on every `slug`

### Enums

- [ ] `content_type`: article, guide, essay, legend, profile, recipe_story, photo_essay, impact_profile
- [ ] `status`: draft, in_review, published, archived

### Relationships

- [ ] Post → belongsTo Category / EditorialPillar / Author / City
- [ ] Post → belongsToMany Tag
- [ ] Category / EditorialPillar / Author / City → hasMany Post
- [ ] Tag → belongsToMany Post
- [ ] `Post::published()` query scope (status = published and published_at <= now)

### Verification

- [ ] `php artisan migrate:fresh` runs clean on PostgreSQL
- [ ] Factories for each model
- [ ] Tests: Post belongs to category · Post can have tags
- [ ] **Owner validated**

---

## Phase 4 — Seeders

- [ ] `CategorySeeder` — Lugares, Naturaleza, Sabor Caribe, Cultura e Historias, Guías y Experiencias (with Spanish slugs)
- [ ] `EditorialPillarSeeder` — 11 pillars with `source_folder` values
- [ ] `TagSeeder` — 15 initial tags (gastronomía, naturaleza, memoria, …)
- [ ] `CitySeeder` — 15 initial cities with department + region
- [ ] `DraftPostSeeder` — 12 launch candidates:
  - [ ] status = `draft`
  - [ ] excerpt = `Borrador inicial pendiente de investigación y validación editorial.`
  - [ ] `requires_fact_check = true` for guides and nature content
  - [ ] Linked to the correct category, pillar, and city
- [ ] `DatabaseSeeder` calls all seeders; `php artisan migrate:fresh --seed` works
- [ ] **Owner validated**

---

## Phase 5 — Filament Resources

- [ ] `CategoryResource`
- [ ] `EditorialPillarResource`
- [ ] `AuthorResource`
- [ ] `CityResource`
- [ ] `TagResource`
- [ ] `PostResource` form: title, auto slug, subtitle, excerpt, rich content editor, featured image upload, category / pillar / author / city selects, content type, status, featured toggle, published_at, SEO title, SEO description, 5 editorial flags
- [ ] `PostResource` table columns: title, category, pillar, content type, status, featured, published date, updated date
- [ ] `PostResource` filters: status, category, pillar, content type, featured, requires fact check
- [ ] Storage link for uploads (`php artisan storage:link`)
- [ ] Manual check: create, edit, and delete a record in every resource
- [ ] **Owner validated**

---

## Phase 6 — Public Frontend MVP

- [ ] Base Blade layout (Tailwind, neutral configurable site name, Spanish copy)
- [ ] Home page `/`
- [ ] Article detail `/articulos/{post:slug}`
- [ ] Category archive `/categorias/{category:slug}`
- [ ] Author page
- [ ] About page `/sobre-el-proyecto`
- [ ] Basic search / filtering
- [ ] City page (optional)
- [ ] Only published posts are publicly visible (404 for drafts)
- [ ] Tests: homepage loads · article page loads · category page loads · drafts hidden · only published posts listed · slugs resolve
- [ ] **Owner validated**

---

## Phase 7 — Editorial Workflow Enhancements

- [ ] Draft preview for logged-in editors
- [ ] Related posts
- [ ] Featured post controls
- [ ] Automatic reading time calculation
- [ ] Better image management
- [ ] SEO metadata helpers
- [ ] Editorial checklist fields
- [ ] **Owner validated**

---

## Phase 8 — Launch Preparation

- [ ] Sitemap
- [ ] `robots.txt`
- [ ] SEO metadata: title, description, canonical URL
- [ ] Open Graph + Twitter/X card metadata
- [ ] Configurable branding (settings table or config file)
- [ ] Performance review
- [ ] Accessibility review
- [ ] Analytics placeholder
- [ ] `docs/technical/deployment.md`
- [ ] Backup notes
- [ ] **Owner validated**

---

## Supporting Docs (section 15)

- [ ] `docs/editorial/content-pillars.md`
- [ ] `docs/editorial/launch-article-candidates.md`
- [ ] `docs/editorial/editorial-voice.md`
- [ ] `docs/technical/database-models.md`
- [ ] `docs/technical/filament-admin.md`
- [ ] `docs/technical/deployment.md`

---

## MVP Success Criteria (section 19)

- [ ] Dario can log into Filament
- [ ] Dario can create and edit categories, pillars, authors, cities, tags, and posts
- [ ] Posts can be marked draft / in review / published / archived
- [ ] Published articles appear publicly
- [ ] Draft articles do not appear publicly
- [ ] Categories have public archive pages
- [ ] Article pages have clean, readable layouts
- [ ] First 10–12 articles can be published
- [ ] Codebase is clean enough to keep iterating
- [ ] Platform stays flexible for national expansion

---

## Phase 9 — Future Growth (do not build until requested)

Newsletter · interactive map · place directory · route builder · bilingual ES/EN · contributor system · audio stories · photo essays · sponsored content · digital guides · shop · educational collections · living cultural archive.
