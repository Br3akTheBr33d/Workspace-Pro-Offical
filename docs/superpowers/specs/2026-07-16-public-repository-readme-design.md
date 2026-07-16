# Public Repository README Refresh Design

## Goal

Refresh the public Workspace Pro information repository so that its README accurately presents the currently published Chrome Web Store release, v1.0.8, and the product information current to the July 2026 website.

## Scope

- Keep v1.0.8 as the only published/live version in the badge, release copy, installation flow, and Store link.
- Replace the stale “Coming soon” Store badge with a live Chrome Web Store badge and link.
- Update the product overview, free and Pro feature tables, widgets, shortcuts, privacy copy, and browser compatibility from `website-july-2026` and the current extension manifest.
- Include an explicit, visually separate v1.1.0 preview. It must state that the feature set is in development and is not included in the v1.0.8 Store release.
- Add a small, curated set of current product screenshots from `website-july-2026`, stored in the repository's existing `assets/` directory and embedded from local paths.
- Preserve the repository's purpose as a public issue tracker: website, documentation, bug report, feature request, contact, privacy, and terms links remain prominent.

## Non-Goals

- Do not copy the whole marketing website or publish source code for the proprietary extension.
- Do not claim v1.1.0 is released, available in the Chrome Web Store, or installable.
- Do not alter issue templates or change the live extension version.
- Do not change the existing product pricing beyond describing the established free and one-time Pro tiers.

## Content Design

The README begins with a logo, a v1.0.8 live badge, a Chrome Web Store live badge, platform compatibility, and links to the website, documentation, and issue forms. The first product section states that Workspace Pro is local-first and summarizes the current release.

Feature information is grouped into Free, Pro, and dashboard widget tables. The language is concise and user-facing; it does not expose internal implementation details such as API endpoint names or internal storage keys. The keyboard section adds the Assistant shortcut while retaining the existing popup and dashboard shortcuts.

The v1.1.0 preview is a dedicated section after the live feature overview. It summarizes the unreleased Wiki, richer Assistant coverage, Drive restore points, and popup improvements, then links readers to the website documentation. A warning line explicitly keeps the live/released boundary clear.

## Assets

Copy only current visual assets needed by the README from `website-july-2026/files/` into `assets/`: the dashboard overview, Wiki graph, popup Assistant, and Drive snapshots. README image references use relative paths, so they render on GitHub without depending on a raw-content URL or a branch name.

## Validation

- Check all stated version references: v1.0.8 is live; v1.1.0 is preview-only.
- Confirm every local README image path exists and renders as a GitHub-relative asset path.
- Check all external URLs and the Chrome Web Store identifier.
- Render the Markdown locally if a renderer is available; otherwise perform structural checks for headings, tables, images, and links.
- Review the diff to ensure only README, curated assets, and this specification are added or modified.

## Risks and Mitigations

The main risk is confusing readers about release availability. Version labels and installation language therefore use v1.0.8 exclusively, while the preview has explicit unreleased wording. The second risk is README bloat; only four screenshots are included and the full documentation stays on the website.
