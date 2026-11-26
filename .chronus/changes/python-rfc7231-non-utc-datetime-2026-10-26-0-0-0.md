---
changeKind: fix
packages:
  - "@typespec/http-client-python"
---

Fix model properties encoded as `rfc7231` raising `ValueError: usegmt option requires a UTC datetime` for naive datetimes, datetimes with a non-UTC offset, or UTC datetimes whose `tzinfo` isn't `datetime.timezone.utc` (such as values parsed by `isodate`). They are now converted to GMT, and naive datetimes are treated as UTC, like the `rfc3339` and `unix-timestamp` encodings and the msrest serializer.
