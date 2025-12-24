Nest.js Architecture Rules

1. Modularity: Organize by domain (Module, Controller, Service). Controllers orchestrate only. DTOs + ValidationPipe required.

2. Security: Secure-by-default. JWT "Bearer" in header. CORS via enableCors: strict whitelist if credentials=true, no *.

3. Identifiers: Use public UUIDs (ParseUUIDPipe). No incremental IDs. UUIDs are not security replacements.

4. API Control: Global versioning (enableVersioning()), prefer URI. Enable Rate limiting & Helmet.

5. Quality: Centralized error filters. Structured logging (interceptors), no console.log. Typed env (ConfigModule).

6. Performance: Async I/O. Cache frequent reads in services. Compression & timeout interceptors.

7. Documentation: Mandatory Swagger (OpenAPI) for endpoints/DTOs. Keep updated.
