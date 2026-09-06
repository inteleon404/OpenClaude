## XSS — Cross-Site Scripting

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for reflected, stored, and DOM-based XSS.
Discover user-controlled inputs, trace their reflection or flow into browser sinks, and safely validate suspected injection points with a harmless PoC.
Report only confirmed findings with endpoint, method, parameter, context, PoC result, evidence, impact, confidence, and remediation.
```

## SQLi — SQL Injection

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for SQL injection across URL, form, JSON, API, and relevant request parameters.
Identify database-backed inputs and safely validate suspicious behavior using non-destructive techniques.
Report only confirmed findings with endpoint, method, parameter, evidence, database behavior, confidence, impact, and remediation.
```

## LFI — Local File Inclusion

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for Local File Inclusion and related file-path injection issues.
Identify file, path, page, template, view, include, and resource parameters and safely validate suspected local inclusion.
Report only confirmed findings with endpoint, parameter, PoC result, evidence, confidence, impact, and remediation.
```

## IDOR / BOLA

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for IDOR/BOLA by mapping user-controlled object references.
Compare access to authorized resources across the available test accounts and identify missing object-level authorization.
Report only confirmed cross-user access with endpoint, object reference, request comparison, evidence, impact, and remediation.
```

## Broken Access Control

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for Broken Access Control across protected resources and functionality.
Map authorization boundaries and safely compare access between available user roles without modifying unauthorized data.
Report confirmed authorization failures with endpoint, role, request, evidence, impact, confidence, and remediation.
```

## SSRF — Server-Side Request Forgery

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for SSRF through URL, webhook, callback, import, fetch, or proxy functionality.
Identify server-side request mechanisms and safely verify whether user-controlled destinations are processed by the backend.
Use controlled validation only and report confirmed SSRF with endpoint, parameter, evidence, impact, confidence, and remediation.
```

## CSRF — Cross-Site Request Forgery

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for CSRF affecting authenticated state-changing actions.
Identify sensitive requests and evaluate CSRF tokens, SameSite cookies, Origin/Referer validation, and request requirements.
Report only reproducible CSRF findings with endpoint, method, affected action, PoC result, evidence, impact, and remediation.
```

## SSTI — Server-Side Template Injection

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for Server-Side Template Injection.
Identify template, rendering, email, notification, and user-content inputs and safely determine whether input is evaluated server-side.
Stop at harmless evaluation and report confirmed SSTI with endpoint, parameter, evidence, confidence, impact, and remediation.
```

## Open Redirect

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for externally controllable redirects.
Identify redirect, return, next, callback, continue, destination, and URL parameters and safely verify redirect behavior.
Report confirmed open redirects with endpoint, parameter, destination behavior, evidence, impact, and remediation.
```

## File Upload

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for security issues in file-upload functionality.
Review upload validation, filename handling, MIME checks, storage, access controls, and post-upload behavior using harmless test files.
Report only confirmed security impact with endpoint, request, evidence, confidence, impact, and remediation.
```

## CORS

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for exploitable CORS misconfigurations.
Inspect origin handling, credential support, preflight responses, and cross-origin access on relevant authenticated endpoints.
Report only confirmed security impact with endpoint, origin behavior, evidence, confidence, and remediation.
```

## API Security

```text
Perform an authorized API security assessment of https://YOUR-DEMO-WEBSITE.example.
Discover API endpoints and evaluate authentication, authorization, object access, input validation, excessive data exposure, and security controls.
Report confirmed findings with endpoint, method, parameter, request/response evidence, impact, confidence, and remediation.
```

## Authentication

```text
Assess authentication security on the authorized target: https://YOUR-DEMO-WEBSITE.example.
Map registration, login, logout, verification, password-reset, and authentication flows and identify inconsistencies or bypass conditions.
Report only confirmed weaknesses with affected flow, endpoint, evidence, confidence, impact, and remediation.
```

## Session Management

```text
Assess session security on the authorized target: https://YOUR-DEMO-WEBSITE.example.
Evaluate session creation, rotation, expiration, logout invalidation, cookie attributes, and authorization consistency using authorized accounts.
Report confirmed weaknesses with affected endpoint, behavior, evidence, impact, and remediation.
```

## Sensitive Information Exposure

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for unintended sensitive information exposure.
Review HTML, API responses, JavaScript, source maps, metadata, error messages, headers, and publicly accessible resources.
Report only verified exposure with exact location, evidence, confidence, impact, and remediation.
```

## Security Misconfiguration

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for security misconfigurations.
Review exposed debug functionality, unnecessary endpoints, verbose errors, unsafe headers, public configuration, and deployment artifacts.
Separate informational observations from security-impacting findings and report verified issues with evidence and remediation.
```

## HTTP Parameter Pollution

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for HTTP Parameter Pollution.
Identify duplicate-parameter behavior across query strings, forms, APIs, and different request methods.
Report only cases producing a demonstrable security impact with endpoint, parameter, evidence, impact, and remediation.
```

## Prototype Pollution

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for client-side or server-side prototype pollution.
Identify object-merging, JSON, configuration, and user-controlled object inputs and safely verify prototype modification.
Report confirmed vulnerabilities with endpoint, parameter, PoC result, evidence, impact, and remediation.
```

## WebSocket Security

```text
Assess WebSocket functionality on the authorized target: https://YOUR-DEMO-WEBSITE.example.
Map WebSocket endpoints, authentication, message parameters, authorization checks, and cross-user data access.
Report confirmed security issues with endpoint, message type, evidence, impact, confidence, and remediation.
```

## HTTP Request Smuggling

```text
Assess the authorized target: https://YOUR-DEMO-WEBSITE.example for HTTP request-parsing inconsistencies between proxy and backend components.
Identify potential front-end/backend parsing differences and perform only controlled, non-disruptive validation.
Report confirmed discrepancies with affected endpoint, evidence, confidence, impact, and remediation.
```

---

# Reconnaissance Prompts

## Subdomain Enumeration

```text
Build a modular reconnaissance script for authorized domains listed in ./scope.txt.
Discover subdomains using configured passive sources, normalize and deduplicate results, enforce scope, and optionally validate discovered hosts.
Include configurable timeouts, rate limits, concurrency, logging, dependency checks, and structured output.
```

## HTTP Service Discovery

```text
Build a scope-aware HTTP discovery script using authorized hosts from ./subdomains.txt.
Identify reachable HTTP/HTTPS services and collect status code, title, redirect, server, technology indicators, and response metadata.
Support concurrency, rate limits, timeouts, deduplication, logging, and machine-readable output.
```

## URL Discovery

```text
Build a URL reconnaissance script for authorized targets in ./scope.txt.
Collect URLs from configured passive sources and authorized crawling, normalize and deduplicate them, and classify discovered paths and parameters.
Make the workflow modular with scope enforcement, rate limits, logging, resumability, and structured results.
```

## JavaScript Recon

```text
Build a JavaScript reconnaissance script for authorized URLs in ./urls.txt.
Discover JavaScript files and extract endpoints, API paths, parameters, source-map references, URLs, and security-relevant configuration indicators.
Deduplicate results and organize output into JS files, endpoints, parameters, and evidence without exploitation.
```

## API Discovery

```text
Build an authorized API discovery script using ./urls.txt and ./js/.
Identify REST, GraphQL, versioned endpoints, HTTP methods, parameters, and authentication indicators from available application data.
Generate a deduplicated API inventory containing endpoint, method, parameter, source, and evidence.
```

## Parameter Discovery

```text
Build a parameter-discovery script for authorized URLs in ./urls.txt.
Extract query, path, form, JSON, and API parameters and classify them by likely function such as ID, file, URL, redirect, search, or template.
Deduplicate results and generate a prioritized parameter inventory with source evidence.
```

## Technology Fingerprinting

```text
Build a passive technology-fingerprinting script for authorized targets in ./httpurls.txt.
Identify observable servers, frameworks, CMS platforms, libraries, versions, headers, and technology indicators without exploitation.
Correlate results per host and flag components requiring manual verification.
```

## JavaScript Security Review

```text
Build a JavaScript security-review script for authorized files in ./js/.
Identify exposed secrets, tokens, API endpoints, credentials-like patterns, environment references, and configuration data.
Redact sensitive values and report file, location, finding type, confidence, and supporting evidence.
```

## Safe Nuclei Pipeline

```text
Build a scope-aware vulnerability-scanning pipeline for authorized URLs in ./httpurls.txt.
Run only appropriate non-destructive templates with configurable concurrency, rate limits, exclusions, and timeouts.
Deduplicate results and separate informational observations from findings requiring manual validation.
```

## Recon Pipeline

```text
Build an end-to-end authorized reconnaissance pipeline starting from ./scope.txt.
Run subdomain discovery → HTTP validation → URL discovery → JavaScript analysis → API/parameter discovery → technology detection → safe vulnerability scanning.
Make every stage modular, resumable, scope-enforced, rate-limited, logged, deduplicated, and organized under ./results/.
```

## Custom Recon Script Builder

```text
Build a customizable reconnaissance script based on the tools and workflow I specify for my authorized scope.
Allow configurable stages, input/output files, tools, concurrency, rate limits, exclusions, logging, and resumability.
Generate the complete script, requirements, usage, directory structure, error handling, and scope enforcement.
```
