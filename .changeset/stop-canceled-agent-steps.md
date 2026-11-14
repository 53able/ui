---
"@ui-sdk/core": patch
---

Fail agent steps when a change created during the action is synchronously canceled with `details.cancel()`. Return `ok: false` and skip later steps without rolling back earlier effects; preserve ordinary `false` results and no-op changes.
