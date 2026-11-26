---
changeKind: fix
packages:
  - "@typespec/http-client-js"
---

Match response `Content-Type` headers by exact, case-insensitive media type instead of by substring. Previously a response such as `application/json-patch+json`, or one whose parameters mentioned `application/json`, could be handled by the `application/json` branch.
