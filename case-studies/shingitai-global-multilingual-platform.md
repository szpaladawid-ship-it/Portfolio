# ShinGiTai Global — Multilingual Corporate and Product Platform

## Status

**Production**

Live website: `https://shingitaiglobal.com`

Repository visibility: private implementation repository; public production result available.

## Project summary

ShinGiTai Global is a multilingual corporate and product website for ShinGiTai Holding Groupe. It presents the holding structure, product portfolio, investor information, download status, and dedicated landing experiences for OdynAI, Forge, Game Studio, Language, WildZone, and Foundation.

The project combines corporate information architecture with product storytelling, locale-aware routing, technical SEO, controlled release validation, and a staged language rollout.

## Objective

Build one coherent public platform capable of representing several different ventures without reducing them to unrelated landing pages.

The website needed to:

- explain the holding model,
- preserve individual product identities,
- support multiple languages,
- scale to additional markets,
- provide consistent metadata and navigation,
- distinguish live capability from planned capability,
- support repeatable release and validation workflows.

## Role and responsibilities

- product direction,
- information architecture,
- technical scope definition,
- multilingual rollout planning,
- localization review,
- QA criteria,
- release management,
- production verification.

Implementation work used a tool-assisted development workflow, with changes reviewed and accepted through explicit file scopes, local validation, Git branches, pull requests, Vercel previews, and live smoke tests.

## Delivery scope

### Corporate layer

- multilingual homepage,
- ecosystem and project presentation,
- roadmap and development timeline,
- partners and investors page,
- company information pages,
- download center,
- shared navigation and footer.

### Product layer

Dedicated landing experiences for:

- OdynAI,
- Forge,
- Game Studio,
- Language.

Shared product framework for:

- WildZone,
- Foundation.

### Localization layer

Production-grade public content completed and validated for:

- English,
- Norwegian,
- Polish,
- Japanese.

Additional locale scaffolding exists in the application, but it is not presented as completed localization.

### SEO and routing

- locale-prefixed routes,
- localized canonical URLs,
- `hreflang` alternates,
- `x-default`,
- localized Open Graph URLs,
- localized titles and descriptions,
- locale-aware CTA links and in-page anchors.

## Technology stack

- Next.js 16 App Router
- React 19
- TypeScript
- Tailwind CSS 4
- Vercel
- static generation
- JSON dictionaries
- typed product-translation modules
- Git and GitHub pull-request workflow

## Architecture approach

The website separates translation responsibilities into three layers:

1. shared JSON dictionaries for common website copy,
2. typed translation modules for complex product landing pages,
3. shared product configuration for statuses, roadmap stages, FAQ, downloads, and resource content.

This structure keeps the common website consistent while allowing complex products to use strongly typed copy contracts.

## Localization delivery approach

Each locale was delivered as an isolated release rather than a bulk machine-translation pass.

The process included:

- branch isolation,
- exact changed-file scope,
- key-structure verification,
- product-specific copy review,
- production build,
- HTTP and language-attribute validation,
- known fallback detection,
- CTA and anchor checks,
- canonical, hreflang, and Open Graph checks,
- regression checks for existing languages,
- desktop and mobile visual review,
- Vercel deployment verification,
- production smoke tests.

## Verified release evidence

### Build and generation

- Next.js production build: PASS
- TypeScript validation: PASS
- Static generation: 351/351 pages

The generated page count includes registered locale-route combinations. It does not mean every registered locale is fully translated.

### Japanese release

- pull request: #4
- feature commit: `be9ffb888fe13c8e94fa895b436519520a2ceb11`
- merge commit: `7d1b51f755f56c40a3239fb6774bc2a39c5a38f2`
- changed paths: 12
- automated localization validator: PASS
- Vercel production deployment: success
- production smoke test: 9/9 key Japanese routes returned HTTP 200

Validated Japanese routes included:

- homepage,
- OdynAI,
- Forge,
- Game Studio,
- Language,
- WildZone,
- Foundation,
- download center,
- investors page.

### Regression evidence

The Japanese release included HTTP, language-attribute, and representative-content regression checks for English, Norwegian, and Polish routes.

## Key technical problem solved

The download page initially inherited the homepage canonical URL. The release validator detected the mismatch. The page received its own localized metadata generator, including exact canonical, locale alternates, `x-default`, and Open Graph URL. The corrected validator then passed.

This is representative of the project approach: treat build success as necessary but insufficient, and validate the public contract separately.

## Outcome

- one production website for the holding and its product ecosystem,
- four completed public language versions,
- repeatable localization release workflow,
- scalable route and translation architecture,
- validated multilingual SEO,
- controlled distinction between current and planned functionality,
- foundation for Korean, Simplified Chinese, Traditional Chinese, and later European language releases.

## Portfolio capabilities demonstrated

- multilingual Next.js architecture,
- information architecture for multi-product organizations,
- typed localization systems,
- responsive product landing pages,
- technical SEO for localized routes,
- release engineering and QA,
- GitHub pull-request discipline,
- Vercel preview and production verification,
- evidence-based documentation.

## Current limitations

- not every registered locale is fully translated,
- final native-language review remains advisable for high-risk or culturally sensitive public copy,
- authentication and application routes are preview layers until production backend services are connected,
- private implementation details are not exposed through the public portfolio.
