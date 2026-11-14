---
"@ui-sdk/core": minor
---

Let `allow` say who refused an agent's step: return `{ refusedBy: "person" }` or `{ refusedBy: "app" }` in place of `false`, from the `allow` of `createAgent` or of `registerTools`, and the step fails with `The person said no to …` or `The app refused …`. A plain `false` on a step marked with `data-agent-confirm` now fails with `The person or the app said no to "…"`, since a rule of the app's can return it as well as the person. Every other object `allow` returns now refuses the step, where a truthy one like `{ isConfirmed: true }` used to let it run.
