Astro Architecture Rules

1. HTML Default: Serve static HTML. Use client:* directives only for interactive components.

2. Hydration Strategy: client:load for critical UI; client:idle for background; client:visible for off-screen elements.

3. Performance: Keep islands lightweight. Avoid large props (serialization cost). Don't hydrate static content.

4. Structure: Separation of concerns: logic in frontmatter, view in template. Centralize SEO in src/layouts. 

5. Data Layer: Use src/services. Fetch data in server frontmatter, never in UI components. Validate all API responses.

6. SSG/SSR: Avoid user-specific data in SSG builds. Use SSR or client-side fetch for dynamic needs.

7. .astro First: Build UI with .astro. Restrict React/Vue to complex interactive islands only.

8. Routing: Avoid hardcoded strings. Use Astro.url and Content Collections for safe routing.
