Next.js Architecture Rules

1. App Router: Use app/ and Server Components by default. Add "use client" only for real interactivity (hooks, events).

2. Security: Never expose keys on the client. Do not import databases in client components. Use Route Handlers as a secure bridge.

3. Data: On the server, fetch data directly from the source (fetch/DB), not your own API. Configure cache (no-store or times) explicitly.

4. Optimization: Use tags to update cache when data changes. Avoid duplicate requests using React's cache().

5. SEO: Define metadata only in server components. Use static files for social images (opengraph-image).

6. Order: Separate view (app/) from business logic (src/services). Centralize external API call configurations.

7. Errors & Load: Handle failures with error.js files. Do not load heavy libraries on the client if the server can process them.
