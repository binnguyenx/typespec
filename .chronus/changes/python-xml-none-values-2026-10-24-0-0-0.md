---
changeKind: fix
packages:
  - "@typespec/http-client-python"
---

Fix XML serialization writing the literal text `None` for `None` values in lists, dict values, and properties set to `None` through dict syntax. Such elements are now written empty (for example `<Tag />`) and `None` attributes are omitted, matching the msrest serializer.
