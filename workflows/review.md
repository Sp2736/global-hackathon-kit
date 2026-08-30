# Review

## Description

Perform a senior-engineer review of the current implementation before submission or merge.

## Steps

1. Inspect the diff and changed files.
2. Check architecture consistency.
3. Check for duplicate components/utilities.
4. Check data validation.
5. Check authorization/RBAC.
6. Check secret exposure.
7. Check error handling.
8. Check async failure handling.
9. Check loading/empty/error UX.
10. Check accessibility.
11. Check responsive behavior.
12. Check performance risks.
13. Check AI output validation and prompt-injection exposure where relevant.
14. Check third-party API reliability/fallbacks.
15. Check tests and build.
16. Rank findings:
    - blocker
    - high
    - medium
    - low
17. Fix blockers/high issues when explicitly asked to do so.
18. Do not perform unrelated refactors.
