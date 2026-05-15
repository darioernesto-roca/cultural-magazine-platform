# Cultural Magazine Platform, Codex Source of Truth

**Repository:** `cultural-magazine-platform`  
**Project type:** Laravel + Filament editorial web application  
**Database:** PostgreSQL  
**Primary language of the publication:** Spanish  
**Initial editorial focus:** Colombian Caribbean culture  
**Future expansion:** Colombia-wide cultural magazine / living cultural archive  
**Owner:** Dario Ernesto Roca  
**Last updated:** 2026-05-15  

---

## 0. Purpose of This Document

This Markdown file is the **source of truth for Codex and any AI coding assistant** working on this repository.

Codex must use this document to understand:

1. The editorial purpose of the platform.
2. The cultural categories and content pillars.
3. The technical stack.
4. The Laravel + Filament architecture.
5. The database models.
6. The phased development process.
7. The rule that work must advance **one phase at a time**.
8. The rule that **Dario must manually validate each phase before Codex proceeds to the next one**.

Codex must not treat this as a generic blog project. This is a cultural digital magazine and eventually a living cultural archive.

---

## 1. Core Project Vision

This project is a digital magazine and Laravel web application about Colombian culture, starting from the Colombian Caribbean.

The project revives an older editorial idea, but it must become a new independent brand and platform. It should combine:

- Cultural storytelling
- Practical visitor guides
- Food and culinary memory
- Ecology and territory
- Local history
- Oral tradition
- Places and routes
- People and communities
- Long-form editorial work
- A clean, modern Laravel-based publishing system

The editorial promise is:

> The Colombian Caribbean told from inside, with the possibility of later expanding into a broader Colombia cultural archive.

The project must not feel like a generic tourism blog.

It should feel closer to:

- A digital cultural magazine
- A living archive
- A field notebook
- A cultural map
- A curated editorial platform
- A local knowledge project

---

## 2. Strategic Scope

### 2.1 Initial Scope

The first version must focus on the **Colombian Caribbean region**.

Reason:

- The existing content foundation is Caribbean-centered.
- The source folders already contain many Caribbean-focused article ideas.
- The owner has a personal and editorial connection with the region.
- A Caribbean-first focus gives the project stronger identity.
- It avoids becoming another generic Colombia travel blog.

### 2.2 Future Scope

The platform must be technically flexible enough to expand later into broader Colombian culture.

Codex must avoid hardcoding the word `Caribe` into database names, models, namespaces, or core application structure.

Good generic technical names:

- `Category`
- `EditorialPillar`
- `Post`
- `Place`
- `Region`
- `City`
- `Route`
- `Author`
- `Tag`
- `Collection`

Avoid technical names such as:

- `CaribePost`
- `CaribeCategory`
- `CoastalArticle`
- `ViveCaribePost`

The brand name is not final. Use neutral project naming in code.

---

## 3. Brand Status

The final brand name has **not** been chosen.

Do not hardcode any final public brand identity.

Use temporary copy where needed:

- Site name: `Cultural Magazine Platform`
- Alternative placeholder: `Revista Cultural`
- Tagline placeholder: `Historias de cultura, memoria y territorio.`

The owner is exploring names inspired by:

- Cultural memory
- Time
- Herencia
- Routes
- Living archives
- Literary references
- The idea that life is made from moments, days, stories, and places
- Names like `Macuira`, `El Otro Mapa`, `Archivo Vivo`, `El Tiempo Heredado`, `Los Días que Somos`, and similar concepts

Do not finalize branding in code. Branding should be configurable from a settings table or configuration file in a later phase.

---

## 4. Editorial Identity

### 4.1 What the Platform Is

The platform is:

- A cultural digital magazine
- A place-based storytelling project
- A curated archive of places, memories, routes, foods, and people
- A future educational and cultural reference for Colombian identity

### 4.2 What the Platform Is Not

The platform is not:

- A generic tourism blog
- A simple WordPress-style news feed
- A SEO-only content farm
- A superficial travel guide
- An AI-generated article dump
- A site that exoticizes communities or poverty
- A project that publishes unverified practical data as fact

### 4.3 Editorial Voice

The editorial voice must be:

- Local, but not exclusionary
- Warm, but not superficial
- Informed, but not academic-heavy
- Useful for visitors, but respectful of local communities
- Cultural, practical, and narrative
- Human, literary, and clear
- Aware of social context
- Resistant to clichés about the tropics, tourism, and the Caribbean

Avoid:

- Generic AI-sounding introductions
- Overused travel-blog language
- “Hidden gem” clichés
- Exoticizing local communities
- Poverty tourism
- Promotional copy disguised as editorial content
- Claiming prices, schedules, or conditions without verification
- Treating culture as decoration

### 4.4 Preferred Article Formula

A strong article should usually include:

1. A human, sensory, historical, or place-based opening.
2. Cultural context.
3. Historical or territorial relevance.
4. Practical information when applicable.
5. Local perspective.
6. Responsible recommendation.
7. Related places, routes, foods, people, or stories.
8. Internal links to related articles.

---

## 5. Content Source Material

The source material comes from an older Google Drive project folder:

`My Drive > Working > Dev job > vive-caribe-2023 > projects`

The current repository is:

`cultural-magazine-platform`

The Drive project folders include:

- `caribe-vida-y-experiencias`
- `caribe-ecoturistico`
- `ruta-del-sabor-caribe`
- `lugares-emblematicos`
- `herencia-caribe`
- `cuentos-y-leyendas-del-caribe-colombiano`
- `solidaridad-caribe`
- `colombiaadventures`
- `colombia-languages`
- `colombia-sports`
- `shop`
- `script.txt`

Codex should interpret these as **content pillars and source categories**, not necessarily as final public website categories.

---

## 6. Public MVP Categories

For the first public version, keep the category structure simple.

Use these public categories:

1. **Lugares**
2. **Naturaleza**
3. **Sabor Caribe**
4. **Cultura e Historias**
5. **Guías y Experiencias**

These categories are public-facing and simple for readers.

The internal content pillars can be more detailed.

### 6.1 Suggested Public Category Slugs

- `/categorias/lugares`
- `/categorias/naturaleza`
- `/categorias/sabor-caribe`
- `/categorias/cultura-e-historias`
- `/categorias/guias-y-experiencias`

### 6.2 Article URL Structure

Use Spanish article routes:

- `/articulos/parque-tayrona-guia-cultural-natural`
- `/articulos/cayeye-desayuno-caribe-historia`
- `/articulos/mercado-bazurto-cartagena-identidad`

Use slugs generated from article titles.

---

## 7. Editorial Pillars and AI Instructions

The following pillars must guide the initial content architecture.

Codex must use these descriptions when creating seed data, admin labels, content briefs, sample articles, category descriptions, and UI copy.

---

## 7.1 Pillar: Caribe Vida y Experiencias

### Internal Pillar Name

`Caribe Vida y Experiencias`

### Public Category Mapping

Primary public category:

- `Guías y Experiencias`

Secondary possible categories:

- `Lugares`
- `Cultura e Historias`

### Purpose

Practical and cultural guides for visitors and locals, written from the perspective of people who live in the region.

This pillar should help readers understand how to move through Caribbean cities and places with context, not just as tourists.

### Source Article Ideas

The source TXT includes ideas around:

#### Airports of the Colombian Caribbean

Create future articles about:

1. Aeropuerto Ernesto Cortissoz de Barranquilla
2. Aeropuerto Rafael Núñez de Cartagena
3. Aeropuerto Simón Bolívar de Santa Marta
4. Aeropuerto Almirante Padilla de Riohacha
5. Aeropuerto Alfonso López Pumarejo de Valledupar
6. Aeropuerto Los Garzones de Montería
7. Aeropuerto Las Brujas de Corozal

Each airport article can include:

- Location
- Infrastructure
- Airlines
- Itineraries
- Transport options
- Approximate prices
- Distance to city center
- Local tips
- Updates that require verification before publishing

#### City Guides

Create guide frameworks for:

1. Santa Marta
2. Barranquilla
3. Cartagena
4. Valledupar
5. Riohacha
6. Sincelejo
7. Montería

Each city guide can include:

- Nightlife
- Places to walk
- Cultural tourism
- Sun and beach tourism
- Museums and monuments
- Lunch and food places
- Business travel
- Hotels for business visitors
- Daily life in the city
- Adventure and extreme sports
- Local neighborhoods and rhythms

### Codex Instructions

When building database seeders or admin examples for this pillar, include article ideas such as:

- `Santa Marta desde adentro: planes para caminar, comer y conocer`
- `Barranquilla más allá del Carnaval: río, barrio y ciudad`
- `Cartagena más allá de la postal turística`
- `Cómo llegar al Caribe colombiano: guía de aeropuertos`
- `Guía de viaje de negocios por las ciudades del Caribe colombiano`

---

## 7.2 Pillar: Caribe Ecoturístico

### Internal Pillar Name

`Caribe Ecoturístico`

### Public Category Mapping

Primary public category:

- `Naturaleza`

Secondary possible categories:

- `Lugares`
- `Cultura e Historias`

### Purpose

Nature, ecology, wildlife, conservation, natural parks, and environmental storytelling.

This pillar should combine natural beauty with ecological responsibility and cultural context.

### Source Article Ideas

The source TXT includes the following article ideas:

1. Avistamiento de aves en Minca
2. La ruta del jaguar en la Ciénaga Grande de Santa Marta
3. El hogar del mono tití cabeciblanco
4. Santuario de Fauna y Flora Los Flamencos
5. La Ciénaga de Mallorquín
6. Navegar el Río Magdalena
7. Parque Nacional Natural Tayrona
8. Parque Nacional Natural Corales del Rosario y San Bernardo
9. Vía Parque Isla de Salamanca
10. Parque Nacional Natural Macuira
11. Parque Nacional Natural Old Providence McBean Lagoon
12. Parque Nacional Natural Sierra Nevada de Santa Marta
13. Santuario de Flora y Fauna Los Colorados
14. Los manatíes
15. El caimán aguja
16. El puma
17. Pico Colón, Pico Bolívar, lagunas y significado espiritual
18. Mitos y realidades sobre las zarigüeyas
19. El zorro de montaña
20. Serpientes urbanas y rurales del Caribe colombiano
21. La barracuda y el temor de algunos pescadores
22. Tiburones del mar Caribe colombiano
23. Delfines del mar Caribe colombiano
24. Monos aulladores
25. Sitios de buceo en el Caribe colombiano
26. Jardín Botánico de Turbaco
27. Las iguanas de El Rodadero
28. Los pisingos y la cacería furtiva
29. Tortugas que anidan en playas del Caribe colombiano

### Codex Instructions

When building article structures for this pillar:

- Include fields for ecological sensitivity.
- Include a `requires_fact_check` flag for practical or scientific claims.
- Add optional fields for `species`, `protected_area`, or `conservation_status` in future phases if needed.
- Do not invent scientific facts.
- Do not publish practical travel conditions without validation.
- If sample content is created, clearly mark it as placeholder/draft.

Suggested initial articles:

- `Parque Tayrona: guía cultural y natural desde una mirada local`
- `Minca y el avistamiento de aves en la Sierra Nevada`
- `La Ciénaga Grande de Santa Marta: belleza, conflicto y vida`
- `Flamencos en La Guajira: naturaleza, territorio y cultura`
- `Fauna del Caribe colombiano: animales que debemos conocer y respetar`

---

## 7.3 Pillar: Ruta del Sabor Caribe

### Internal Pillar Name

`Ruta del Sabor Caribe`

### Public Category Mapping

Primary public category:

- `Sabor Caribe`

Secondary possible categories:

- `Cultura e Historias`
- `Lugares`

### Purpose

Food, recipes, culinary traditions, ingredients, markets, local cooks, and cultural stories around Caribbean cuisine.

This pillar should treat food as memory, not just recipes.

### Source Article Ideas

The source TXT includes the following ideas:

1. Dulces artesanales de Semana Santa
2. El cayeye
3. La arepa de huevo
4. La salchipapa costeña
5. El quibbe y la influencia árabe
6. Las almojábanas de La Paz
7. Festival del bollo de Mamatoco
8. Bollos y envueltos
9. La ayaca y el pastel
10. Cazuela de mariscos en el litoral Caribe
11. Arroz de coco de Cartagena
12. Arroz de titote
13. Arroz de pollo
14. Almuerzo de fríjoles con paticas de cerdo, arroz, aguacate, tajada de maduro y jugo de corozo
15. Arroz de lisa
16. Sopa de pescado
17. El ñame
18. Suero costeño
19. Arepuelas
20. Empanada costeña
21. Ceviche
22. Filete de corvina en leche de tigre
23. Variedades de café con denominación de origen en el Caribe colombiano
24. Historia del cacao en el Caribe
25. Aguacates del Caribe
26. Origen de especias y verduras
27. El coco en la cocina Caribe
28. Sancocho de mondongo
29. Sopa de costilla
30. Guandólo
31. Variedades de pescado de mar
32. Cortes de carne
33. Huevo perico
34. Arroz de cecina
35. Sopa de carne salá
36. Chivo de ranchería
37. Chicharroncitos de Villa Country y Baranoa
38. Mojarra de Bazurto
39. Peto
40. Arroz de leche
41. Buñuelitos de harina de trigo
42. Arepas asadas
43. Ron
44. Cervezas artesanales del Caribe colombiano
45. Papa rellena
46. Butifarra
47. Cocada
48. Jugos de frutas típicas
49. Frutas del Caribe colombiano
50. Patacones

### Codex Instructions

For this pillar:

- Treat recipes as cultural narratives.
- Create optional content fields for ingredients and preparation only in a later phase.
- Initial MVP can store all content in `posts.content`.
- Later, add structured recipe support if needed.
- Add sample tags such as `gastronomía`, `cocina tradicional`, `memoria culinaria`, `mercados`, `recetas`, `ingredientes`.

Suggested initial articles:

- `El cayeye: desayuno, memoria y sabor del Caribe`
- `Arepa de huevo: historia viva de la cocina costeña`
- `Suero costeño: el sabor que acompaña al Caribe`
- `Arroz de coco y arroz de titote: dos formas de entender una cocina`
- `Mercado de Bazurto: comida, gente e identidad cartagenera`

---

## 7.4 Pillar: Lugares Emblemáticos

### Internal Pillar Name

`Lugares Emblemáticos`

### Public Category Mapping

Primary public category:

- `Lugares`

Secondary possible categories:

- `Cultura e Historias`
- `Naturaleza`
- `Guías y Experiencias`

### Purpose

Landmarks, towns, cities, beaches, historic places, markets, plazas, monuments, and territories with cultural meaning.

This pillar should show places as living territories, not only as attractions.

### Source Article Ideas

The source TXT includes many places. Use them as a long-term content bank.

Priority examples:

1. Mercado de Bazurto
2. Cerro de la Popa
3. Mompox
4. Chinú and the sombrero vueltiao
5. Tolú and Coveñas
6. Ciudad Perdida
7. Manaure, Cesar
8. Manaure, La Guajira, salinas
9. Galerazamba
10. Fonseca, La Guajira
11. Palomino
12. Ciénaga Grande de Santa Marta
13. Pueblos palafíticos
14. Tasajera
15. Taganga
16. Barú
17. Boca Chica
18. Valledupar
19. Luruaco
20. Nabusímake
21. Cuchilla de San Lorenzo
22. Minca
23. Cabo de la Vela
24. Montes de María
25. El Salado
26. San Jacinto
27. Sampués
28. Lorica
29. Ciénaga
30. Malecón de Barranquilla
31. Ventana al Mundo
32. Puerto Colombia
33. Salgar
34. Santa Verónica
35. Plaza de la Paz
36. Vía 40
37. Pescaíto
38. La Chinita
39. Soledad and butifarra
40. Aracataca
41. Río Grande de la Magdalena
42. Quinta de San Pedro Alejandrino
43. Castillo San Felipe
44. Getsemaní
45. Palenque, Bolívar
46. Mamatoco
47. Iglesia de San Pedro Claver
48. Manga
49. Ronda del Sinú
50. Malecón de Santa Marta
51. Bocagrande
52. Arrecifes in Tayrona
53. Playa Cristal
54. Bahía Concha
55. Gaira
56. San Andrés and Providencia
57. Serranía del Perijá
58. Serranía de Macuira
59. Catedral de Santa Marta

### Codex Instructions

For places:

- Build a `places` table in a later phase, but not necessarily in the first MVP unless requested.
- For the first MVP, `posts` can optionally belong to a `city` and later to a `place`.
- Do not create overly complex geospatial features in phase 1.
- Use this pillar to plan future maps, collections, and destination pages.

Suggested initial articles:

- `Mercado de Bazurto: comida, gente e identidad cartagenera`
- `Mompox: río, historia y artesanía`
- `Taganga: atardeceres, pesca y memoria local`
- `San Jacinto y la memoria cultural de los Montes de María`
- `El Malecón de Barranquilla y la nueva relación con el río`

---

## 7.5 Pillar: Herencia Caribe

### Internal Pillar Name

`Herencia Caribe`

### Public Category Mapping

Primary public category:

- `Cultura e Historias`

Secondary possible categories:

- `Lugares`
- `Sabor Caribe`

### Purpose

Identity, music, traditions, ethnic roots, cultural memory, images of identity, and people of the region.

### Existing Folder Structure

The folder contains subfolders related to:

- `colombia-más-de-mil-ritmos-que-palpitan-en-un-solo-corazón`
- `culturas-que-convergen`
- `rostros-del-caribe-colombiano`
- `imagenes-de-identidad`

### Codex Instructions

This pillar should support:

- Essays
- Profiles
- Interviews
- Cultural explainers
- Music and rhythm stories
- Identity pieces
- Photo essays
- Oral memory
- Indigenous, Afro-Caribbean, Arab, and mestizo influences

Do not reduce this pillar to only history. It is about living inheritance.

Suggested future article ideas:

- `Culturas que convergen en el Caribe colombiano`
- `Rostros del Caribe colombiano`
- `Mil ritmos que palpitan en un solo corazón`
- `Imágenes de identidad: símbolos cotidianos del Caribe`
- `Herencias indígenas, africanas, árabes y mestizas en la región`

---

## 7.6 Pillar: Cuentos y Leyendas del Caribe Colombiano

### Internal Pillar Name

`Cuentos y Leyendas del Caribe Colombiano`

### Public Category Mapping

Primary public category:

- `Cultura e Historias`

Secondary possible categories:

- `Lugares`

### Purpose

Folklore, oral tradition, legends, myths, literary storytelling, and narrative pieces inspired by the Colombian Caribbean.

### Source Article Ideas

The TXT source includes:

1. Punta Aguja, leyendas de marineros
2. La Casa del Diablo en Ciénaga
3. Historias de terror en la Casa de la Inquisición
4. La monja del hospital San Juan de Dios
5. El Kashindukua
6. El Hombre Caimán
7. La troja del otro mundo
8. Un chupacabras salió del jagüey
9. La bruja que pasó a pedir sal
10. Leyendas sobre el puente Pumarejo
11. Leyendas en el centro de Cartagena
12. La leyenda de Buitraguito
13. La leyenda de la sirena en el río Guatapurí
14. La historia de Andrés, el niño que pedía un vaso con agua en un hotel de carretera

### Codex Instructions

For this pillar:

- Keep narrative tone distinct from guide-style articles.
- Add support for a `content_type` field on posts. Possible values:
  - `article`
  - `guide`
  - `essay`
  - `legend`
  - `profile`
  - `recipe_story`
  - `photo_essay`
  - `impact_profile`
- Legends should be clearly categorized as cultural/oral/narrative content.
- Do not present legends as verified historical fact unless researched and sourced.
- Add optional fields later for audio narration or illustrated storytelling.

Suggested initial or future articles:

- `El Hombre Caimán: una leyenda que todavía nada en la memoria`
- `La Casa del Diablo en Ciénaga`
- `La sirena del río Guatapurí`
- `Leyendas de marineros en Punta Aguja`
- `Historias de la Casa de la Inquisición`

---

## 7.7 Pillar: Solidaridad Caribe

### Internal Pillar Name

`Solidaridad Caribe`

### Public Category Mapping

Primary public category:

- `Cultura e Historias`

Secondary possible categories:

- `Lugares`

### Purpose

Highlight foundations, communities, local projects, and people creating positive impact in the region.

### Source Description

The TXT source says:

> Resaltar la labor de fundaciones, comunidades y proyectos con impacto positivo en la región Caribe.

### Codex Instructions

This pillar must be handled with extra respect.

Rules:

- Avoid poverty tourism.
- Avoid savior narratives.
- Focus on dignity, context, local agency, and real impact.
- Do not publish claims about organizations without verification.
- Include source fields, contact fields, and verification fields in future phases if this section grows.
- Consider future content type: `impact_profile`.

Suggested future article structures:

- Community profile
- Foundation profile
- Project impact story
- Interview with local leader
- How readers can support responsibly

---

## 7.8 Pillar: Colombia Adventures

### Internal Pillar Name

`Colombia Adventures`

### Public Category Mapping

Primary public category:

- `Guías y Experiencias`

Secondary possible categories:

- `Naturaleza`
- `Lugares`

### Source Status

The folder appears to contain an older Node/Express-style web project with files like:

- `package.json`
- `package-lock.json`
- `index.html`
- `controllers`
- `routes`
- `sass`
- `src`
- `views`
- `public`

### Codex Instructions

Do not copy old Node/Express architecture into this Laravel project.

Use the folder as historical inspiration only.

If useful, later inspect old files for content or design references, but the new project must be Laravel-based.

---

## 7.9 Pillar: Colombia Languages

### Internal Pillar Name

`Colombia Languages`

### Public Category Mapping

Primary public category:

- `Cultura e Historias`

### Purpose

This can support future content about:

- Regional expressions
- Colombian Spanish
- Indigenous languages
- Caribbean idioms
- Oral traditions
- Words and phrases tied to territory

### Codex Instructions

Do not implement multilingual features in phase 1 unless requested.

Keep the application architecture open to future bilingual Spanish/English content.

---

## 7.10 Pillar: Colombia Sports

### Internal Pillar Name

`Colombia Sports`

### Public Category Mapping

Primary public category:

- `Cultura e Historias`

Secondary possible category:

- `Guías y Experiencias`

### Purpose

This can support future content about:

- Baseball in the Caribbean
- Soccer culture
- Boxing
- Local athletes
- Sports as identity
- Stadiums and neighborhoods
- Community sports stories

### Codex Instructions

Do not prioritize sports in MVP unless the owner requests it.

---

## 7.11 Pillar: Shop

### Internal Pillar Name

`Shop`

### Public Category Mapping

Not part of MVP.

### Purpose

Potential future monetization area.

Could eventually include:

- Digital guides
- Books
- Photo prints
- Cultural products
- Local artisan collaborations
- Affiliate products
- Sponsored products

### Codex Instructions

Do not build e-commerce in the MVP.

Only leave architecture open for future expansion.

---

## 8. Launch Article Candidates

The first launch should include **10 to 12 strong articles**.

Recommended initial list:

1. `Parque Tayrona: guía cultural y natural desde una mirada local`
2. `Minca y el avistamiento de aves en la Sierra Nevada`
3. `Mercado de Bazurto: comida, gente e identidad cartagenera`
4. `El cayeye: desayuno, memoria y sabor del Caribe`
5. `Arepa de huevo: historia viva de la cocina costeña`
6. `Santa Marta desde adentro: planes para caminar, comer y conocer`
7. `Barranquilla más allá del Carnaval: río, barrio y ciudad`
8. `Cartagena más allá de la postal turística`
9. `Mompox: río, historia y artesanía`
10. `La Ciénaga Grande de Santa Marta: belleza, conflicto y vida`
11. `Taganga: atardeceres, pesca y memoria local`
12. `Suero costeño: el sabor que acompaña al Caribe`

Codex may seed these as draft posts, but must clearly mark them as placeholders.

No final published copy should be generated without owner approval.

---

## 9. Technical Stack

Use the following stack:

- Laravel, latest stable compatible version
- Filament Admin Panel, latest stable compatible version
- PostgreSQL
- Blade templates
- Tailwind CSS
- Livewire where useful
- Alpine.js for small interactions
- Vite for frontend assets
- Laravel Pint for formatting
- Pest or PHPUnit for tests, preferably Pest if installed
- Spatie Laravel packages only if useful and approved by phase
- No WordPress
- No Node/Express backend

### 9.1 Version Guidance

Codex must check the current official documentation when executing setup commands.

As of the planning stage:

- Laravel 12 is the current Laravel docs branch.
- Filament documentation currently points to newer stable documentation beyond 4.x, so Codex must use the current stable Filament version compatible with the selected Laravel version.
- Filament panel resources should be used for CRUD admin screens.
- PostgreSQL is the required database.

Do not hardcode outdated installation commands if official docs have changed.

---

## 10. Application Architecture Principles

### 10.1 Keep It Simple at First

Do not over-engineer.

The MVP goal is:

> Publish excellent cultural content beautifully.

Avoid adding complex features before they are needed.

### 10.2 Build in Phases

Codex must complete one phase at a time.

After each phase, Codex must stop and provide:

- What was completed
- Files changed
- Commands run
- How to test
- Any unresolved issues
- What requires Dario’s validation

Codex must not continue to the next phase until Dario validates the previous phase.

### 10.3 Do Not Invent Final Brand Identity

No final brand name has been chosen.

The code should use neutral names and allow branding to be configured later.

### 10.4 Use Spanish Public URLs and Labels

Public-facing site copy should be Spanish.

Admin technical labels can be English where normal for Laravel/Filament, but public category names and routes should be Spanish.

Examples:

- `/articulos`
- `/categorias`
- `/lugares`
- `/sobre-el-proyecto`

### 10.5 Content Safety and Trust

For practical visitor guides, Codex must include editorial flags for:

- `requires_fact_check`
- `contains_practical_info`
- `contains_prices`
- `contains_schedules`
- `contains_sensitive_social_context`

Do not publish such content automatically.

---

## 11. Suggested Database Models

Start with these models.

### 11.1 User

Use Laravel default user model.

Add Filament access control later if needed.

Fields:

- `id`
- `name`
- `email`
- `email_verified_at`
- `password`
- `remember_token`
- timestamps

### 11.2 Author

Represents public-facing article authors.

Fields:

- `id`
- `name`
- `slug`
- `bio`
- `avatar_path`
- `website_url`
- `instagram_url`
- `x_url`
- `linkedin_url`
- `is_active`
- timestamps

### 11.3 Category

Public categories.

Fields:

- `id`
- `name`
- `slug`
- `description`
- `sort_order`
- `is_active`
- timestamps

Initial category seed data:

1. Lugares
2. Naturaleza
3. Sabor Caribe
4. Cultura e Historias
5. Guías y Experiencias

### 11.4 EditorialPillar

Internal editorial pillars based on the source folders.

Fields:

- `id`
- `name`
- `slug`
- `description`
- `source_folder`
- `notes`
- `is_active`
- timestamps

Initial pillar seed data:

- Caribe Vida y Experiencias
- Caribe Ecoturístico
- Ruta del Sabor Caribe
- Lugares Emblemáticos
- Herencia Caribe
- Cuentos y Leyendas del Caribe Colombiano
- Solidaridad Caribe
- Colombia Adventures
- Colombia Languages
- Colombia Sports
- Shop

### 11.5 City

Cities, towns, or municipalities related to posts.

Fields:

- `id`
- `name`
- `slug`
- `department`
- `region`
- `description`
- `latitude` nullable
- `longitude` nullable
- timestamps

Initial city seed examples:

- Santa Marta
- Barranquilla
- Cartagena
- Valledupar
- Riohacha
- Sincelejo
- Montería
- Mompox
- Ciénaga
- Palomino
- Minca
- Taganga
- Puerto Colombia
- Lorica
- San Jacinto

### 11.6 Post

Main editorial content model.

Fields:

- `id`
- `title`
- `slug`
- `subtitle` nullable
- `excerpt`
- `content`
- `featured_image_path` nullable
- `category_id`
- `editorial_pillar_id` nullable
- `author_id` nullable
- `city_id` nullable
- `content_type`
- `status`
- `is_featured`
- `published_at` nullable
- `seo_title` nullable
- `seo_description` nullable
- `reading_time` nullable
- `requires_fact_check` boolean
- `contains_practical_info` boolean
- `contains_prices` boolean
- `contains_schedules` boolean
- `contains_sensitive_social_context` boolean
- timestamps
- soft deletes optional

Allowed `content_type` values:

- `article`
- `guide`
- `essay`
- `legend`
- `profile`
- `recipe_story`
- `photo_essay`
- `impact_profile`

Allowed `status` values:

- `draft`
- `in_review`
- `published`
- `archived`

### 11.7 Tag

Fields:

- `id`
- `name`
- `slug`
- timestamps

Use many-to-many relationship:

- `post_tag`

Initial tag examples:

- gastronomía
- naturaleza
- memoria
- territorio
- historia
- oralidad
- rutas
- ecoturismo
- ciudades
- mercados
- música
- identidad
- leyendas
- fauna
- cocina tradicional

### 11.8 Future Models

Do not build these in phase 1 unless requested:

- `Place`
- `Route`
- `Series`
- `Event`
- `Sponsor`
- `NewsletterSubscriber`
- `ShopProduct`
- `MediaAsset`
- `Source`
- `FactCheckNote`

---

## 12. Filament Admin Requirements

Build an admin panel with Filament.

### 12.1 Required MVP Resources

Create Filament resources for:

- Posts
- Categories
- Editorial Pillars
- Authors
- Cities
- Tags

### 12.2 Post Resource Requirements

The Post admin form should include:

- Title
- Slug
- Subtitle
- Excerpt
- Content editor
- Featured image upload
- Category select
- Editorial pillar select
- Author select
- City select
- Content type select
- Status select
- Featured toggle
- Published at date/time
- SEO title
- SEO description
- Editorial flags:
  - Requires fact check
  - Contains practical info
  - Contains prices
  - Contains schedules
  - Contains sensitive social context

### 12.3 Post Admin Table

The Post table should show:

- Title
- Category
- Editorial pillar
- Content type
- Status
- Featured
- Published date
- Updated date

Add filters for:

- Status
- Category
- Editorial pillar
- Content type
- Featured
- Requires fact check

### 12.4 Admin UX Rule

Filament admin should help the editor manage content clearly.

Do not make the admin interface visually over-customized in the early phase.

Function first, design later.

---

## 13. Public Frontend Requirements

### 13.1 Required MVP Pages

Build public pages only after the backend/admin phase is validated.

Required public pages:

1. Home
2. Article detail
3. Category archive
4. Author page
5. About page
6. Search page or simple search/filtering
7. City page, optional if time allows

### 13.2 Homepage Sections

The homepage should eventually include:

- Hero / featured story
- Latest articles
- Category navigation
- Featured places or guides
- Sabor Caribe section
- Naturaleza section
- Cultura e Historias section
- Newsletter placeholder
- About the project short intro

### 13.3 Article Page Requirements

The article page should include:

- Title
- Subtitle
- Featured image
- Author
- Published date
- Category
- Editorial pillar, optional display
- Reading time
- Content
- Tags
- Related articles
- SEO metadata
- Social sharing metadata

### 13.4 SEO Requirements

Each article should support:

- SEO title
- SEO description
- Canonical URL
- Open Graph title
- Open Graph description
- Open Graph image
- Twitter/X card metadata
- JSON-LD later, not required in the first backend phase

---

## 14. Development Phases

Codex must follow these phases exactly.

---

## Phase 0: Repository Preparation

### Goal

Prepare the repository for Laravel development.

### Tasks

1. Confirm current directory.
2. Confirm Git repository status.
3. Create or update `.gitignore`.
4. Create this source-of-truth file in the repository.
5. Create a basic `README.md` that explains the project.
6. Do not install Laravel until Dario confirms.

### Deliverables

- `CODEX_PROJECT_RULES.md`
- `README.md`
- Clean Git status

### Stop Condition

Stop and ask Dario to validate Phase 0 before moving to Phase 1.

---

## Phase 1: Laravel Project Initialization

### Goal

Install and configure Laravel with PostgreSQL.

### Tasks

1. Install Laravel using current official Laravel instructions.
2. Configure `.env.example`.
3. Set PostgreSQL environment variables.
4. Confirm app key generation.
5. Confirm the app runs locally.
6. Install frontend dependencies.
7. Run migrations.
8. Commit initial Laravel setup.

### Required Environment Variables

Use placeholders:

```env
APP_NAME="Cultural Magazine Platform"
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost:8000

DB_CONNECTION=pgsql
DB_HOST=127.0.0.1
DB_PORT=5432
DB_DATABASE=cultural_magazine_platform
DB_USERNAME=postgres
DB_PASSWORD=
```

### Stop Condition

Stop and ask Dario to validate Phase 1.

---

## Phase 2: Filament Installation

### Goal

Install Filament admin panel.

### Tasks

1. Install current stable Filament version compatible with Laravel.
2. Create Filament panel.
3. Create admin user.
4. Confirm `/admin` route works.
5. Configure production access rules carefully.
6. Do not create resources yet unless Dario validates installation.

### Stop Condition

Stop and ask Dario to validate Phase 2.

---

## Phase 3: Database Models and Migrations

### Goal

Create the core editorial database structure.

### Tasks

Create models, migrations, and relationships for:

- Author
- Category
- EditorialPillar
- City
- Post
- Tag

Create pivot table:

- `post_tag`

Define relationships:

- Post belongs to Category
- Post belongs to EditorialPillar
- Post belongs to Author
- Post belongs to City
- Post belongs to many Tags
- Category has many Posts
- EditorialPillar has many Posts
- Author has many Posts
- City has many Posts
- Tag belongs to many Posts

### Stop Condition

Stop and ask Dario to validate Phase 3.

---

## Phase 4: Seeders

### Goal

Seed the first editorial structure.

### Tasks

Create seeders for:

- Categories
- Editorial Pillars
- Tags
- Cities
- Draft launch posts

### Draft Launch Posts

Seed the 12 launch article candidates as `draft`, not published.

Use placeholder excerpts and mark as requiring editorial review.

### Stop Condition

Stop and ask Dario to validate Phase 4.

---

## Phase 5: Filament Resources

### Goal

Create admin CRUD screens.

### Tasks

Create Filament resources for:

- Posts
- Categories
- Editorial Pillars
- Authors
- Cities
- Tags

Implement Post form and table as defined in this document.

### Stop Condition

Stop and ask Dario to validate Phase 5.

---

## Phase 6: Public Frontend MVP

### Goal

Create the reader-facing digital magazine interface.

### Tasks

Create:

- Home page
- Article detail page
- Category archive page
- Basic about page
- Basic author page
- Basic search/filtering

Use Blade + Tailwind.

Do not overbuild.

### Stop Condition

Stop and ask Dario to validate Phase 6.

---

## Phase 7: Editorial Workflow Enhancements

### Goal

Improve editorial management.

### Possible Tasks

- Preview drafts
- Related posts
- Featured post controls
- Reading time calculation
- Better image management
- SEO metadata helpers
- Editorial checklist fields

### Stop Condition

Stop and ask Dario to validate Phase 7.

---

## Phase 8: Launch Preparation

### Goal

Prepare for first deployment.

### Tasks

- Sitemap
- Robots.txt
- SEO metadata
- Open Graph metadata
- Performance review
- Accessibility review
- Basic analytics placeholder
- Deployment documentation
- Backup notes

### Stop Condition

Stop and ask Dario to validate Phase 8.

---

## Phase 9: Future Growth

Do not build until requested.

Possible features:

- Newsletter
- Interactive map
- Place directory
- Route builder
- Bilingual Spanish/English content
- Contributor system
- Audio stories
- Photo essays
- Sponsored content
- Digital guides
- Shop
- Educational collections
- Living cultural archive

---

## 15. Suggested Repository Structure

After Laravel installation, use standard Laravel structure.

Add project docs:

```txt
/docs
  /editorial
    content-pillars.md
    launch-article-candidates.md
    editorial-voice.md
  /technical
    database-models.md
    filament-admin.md
    deployment.md
CODEX_PROJECT_RULES.md
README.md
```

Do not fight Laravel conventions.

Use standard locations:

- `app/Models`
- `app/Filament/Resources`
- `database/migrations`
- `database/seeders`
- `resources/views`
- `routes/web.php`

---

## 16. Testing Requirements

At minimum, add tests for:

- Homepage loads
- Article detail page loads
- Category page loads
- Only published posts show publicly
- Draft posts are hidden publicly
- Slugs resolve correctly
- Post belongs to category
- Post can have tags

Admin testing can be added later.

---

## 17. Code Quality Rules

Codex must:

- Use clear Laravel conventions.
- Avoid unnecessary abstraction.
- Keep migrations readable.
- Use enums if appropriate for `status` and `content_type`, but avoid complexity if not needed.
- Use form requests only when useful.
- Use route model binding where practical.
- Use Eloquent relationships correctly.
- Keep public controllers simple.
- Prefer explicit readable code over clever code.
- Never commit `.env`.
- Never hardcode credentials.
- Never hardcode final brand name.
- Keep Spanish public slugs and labels.

---

## 18. Content Rules for AI-Generated Drafts

If Codex generates seed content:

- Mark it as draft.
- Mark it as placeholder.
- Do not claim factual accuracy.
- Do not invent prices, dates, schedules, or scientific details.
- Do not write as if the article is final.
- Use excerpts like: `Borrador inicial pendiente de investigación y validación editorial.`
- Set `requires_fact_check = true` for all practical guide or nature content.

---

## 19. MVP Success Definition

The MVP is successful when:

1. Dario can log into Filament.
2. Dario can create/edit categories, pillars, authors, cities, tags, and posts.
3. Dario can mark posts as draft, review, published, or archived.
4. Published articles appear on the public website.
5. Draft articles do not appear publicly.
6. Categories have public archive pages.
7. Article pages have clean readable layouts.
8. The project can publish the first 10 to 12 articles.
9. The code is clean enough to continue iterating.
10. The platform remains flexible for future national expansion.

---

## 20. Final Instruction to Codex

Do not rush into building everything.

Proceed one phase at a time.

At the end of each phase, stop and wait for Dario’s validation.

The first goal is not a perfect platform.

The first goal is a clean Laravel + Filament editorial system that allows this cultural magazine to begin publishing with discipline, identity, and room to grow.
