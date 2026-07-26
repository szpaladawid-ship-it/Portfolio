# Capability — Multilingual Web Delivery

## Service profile

Design and implementation support for multilingual corporate websites, product platforms, and agency-delivered frontend projects built with React and Next.js.

## Demonstrated capabilities

- locale-prefixed route architecture,
- JSON and typed translation contracts,
- language switchers,
- localized navigation and CTA targets,
- localized product and corporate pages,
- canonical and hreflang architecture,
- Open Graph localization,
- static-generation validation,
- existing-language regression checks,
- Vercel preview and production verification,
- production HTTP smoke tests.

## Delivery workflow

1. map the existing content model,
2. define locale keys and regional variants,
3. isolate shared and product-specific copy,
4. implement one locale per controlled branch,
5. validate structure and TypeScript,
6. run production builds,
7. test routes, metadata, links, and fallback behavior,
8. review desktop and mobile layouts,
9. deploy through pull requests and previews,
10. verify production routes after merge.

## Regional-language policy

Regional variants are treated as separate content products when vocabulary, writing conventions, cultural framing, or regulatory expectations differ.

Examples:

- Simplified Chinese and Traditional Chinese require separate review.
- Norwegian copy should be written for the intended Norwegian audience rather than translated word-for-word from English.
- Japanese and Korean navigation requires compact labels and dedicated line-breaking review.

Automatic translation may accelerate a draft, but it does not replace editorial review, product-context review, or qualified native review for sensitive content.

## Agency and white-label fit

This capability is suitable for agencies that need:

- implementation from approved multilingual designs,
- migration from one-language to locale-aware routing,
- SEO repairs for multilingual pages,
- structured translation integration,
- regression-safe language expansion,
- documented handoff and release procedures.

## Evidence project

See [ShinGiTai Global — Multilingual Corporate and Product Platform](../case-studies/shingitai-global-multilingual-platform.md).

The production project demonstrates English, Norwegian, Polish, and Japanese releases, 351/351 static page generation, validated localized metadata, and live production smoke testing.

## Boundaries

- legal and regulatory translations require qualified review,
- accessibility and SEO claims must be validated per project,
- a route scaffold is not presented as a completed language release,
- production status is claimed only after deployment and live verification.
