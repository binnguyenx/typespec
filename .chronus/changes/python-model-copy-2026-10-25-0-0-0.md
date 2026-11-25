---
changeKind: fix
packages:
  - "@typespec/http-client-python"
---

Fix `Model.copy()` returning a plain `Model` that wraps the original's internals instead of a copy of the model, and `copy.copy(model)` returning a copy that shares its fields with the original. Both now return a shallow copy of the same model class, like `dict.copy()`.
