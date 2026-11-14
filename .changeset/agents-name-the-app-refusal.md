---
"@ui-sdk/core": patch
---

When the bridge's `allow` lets a step marked with `data-agent-confirm` through and the `allow` of `registerTools` refuses it, the step now fails with `The app refused press on c1.` instead of `The person said no to "…"`. The first of the two checks answers for the person, so ask the person in the bridge's `allow`, or in the `allow` of `registerTools` when the bridge has none.
