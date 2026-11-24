---
changeKind: fix
packages:
  - "@typespec/http-client-python"
---

Fix model properties returning raw, undeserialized values (for example `str` instead of `datetime`) after the model was changed with `update()`, `pop()`, `popitem()`, `clear()`, `setdefault()` or `del`. These methods now reset the per-field deserialization cache, as `model["key"] = value` already did.
