---
"@inngest/ci": minor
---

Pipelines can now check pull request and push events against GitHub before they run, so a forged webhook can't start one; an event GitHub doesn't agree with fails the run without retrying.

```ts
const ci = createCi(inngest, { verifyEvents: true });
```
