# Copilot Instructions for sdc-vendor-docs

This project is a Mintlify documentation site. AI coding agents should follow these guidelines to be productive and maintain consistency:

## Project Structure

- **Docs are written in MDX** and organized by topic: `api-reference/`, `essentials/`, `ai-tools/`, `snippets/`, `pages/start/`, etc.
- **Entry point:** `docs.json` defines site structure and navigation.
- **API reference:** `api-reference/openapi.json` and related MDX files document endpoints.
- **Images and logos:** Use assets from `images/` and `logo/` for illustrations and branding.

## Developer Workflow

- **Local development:**
  - Install Mintlify CLI: `npm i -g mint`
  - Start local preview: `mint dev` (run in project root)
  - Preview at `http://localhost:3000`
- **Publishing:**
  - Changes pushed to the default branch are auto-deployed via Mintlify's GitHub integration.
- **Troubleshooting:**
  - If dev server fails, run `mint update`.
  - 404 errors often mean `docs.json` is missing or invalid.

## Conventions & Patterns

- **MDX pages:**
  - Use frontmatter (`---`) for title/description.
  - Link to external resources with full URLs.
  - Reference images with relative paths (e.g., `images/hero-dark.png`).
- **Navigation:**
  - Organize guides and references by topic for discoverability.
  - Use `essentials/` for reusable patterns and code snippets.
- **API docs:**
  - Document endpoints in `api-reference/endpoint/` using clear, example-driven MDX.
  - Reference OpenAPI spec for endpoint details.

## External Integrations

- **Mintlify CLI** for local dev and deployment.
- **GitHub App** for auto-publishing.

## Key Files & Directories

- `docs.json`: Site structure and navigation
- `README.md`: Project overview and setup
- `api-reference/openapi.json`: API schema
- `essentials/`: Core documentation patterns
- `pages/start/index.mdx`: Getting started guide

## Example: Adding a New Guide

1. Create a new `.mdx` file in the appropriate directory.
2. Add frontmatter for title/description.
3. Update `docs.json` to include the new page in navigation.
4. Preview locally with `mint dev`.

---

If any conventions or workflows are unclear, please request clarification or examples from the user before proceeding.
