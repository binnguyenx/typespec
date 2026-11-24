---
changeKind: fix
packages:
  - "@typespec/http-client-python"
---

Fix XML serialization raising a confusing `TypeError: can only concatenate str (not "NoneType") to str` instead of the intended `ValueError` when a value such as `None` or a number cannot be serialized into XML.
