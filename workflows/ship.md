# Ship

## Description

Prepare the current project for a reliable hackathon/demo deployment.

## Steps

1. Inspect git status and the final diff.
2. Run typecheck/lint/tests/build using the project's actual commands.
3. Fix root causes; do not weaken tests.
4. Search for secrets, debug statements and accidental files.
5. Verify environment variables are documented and not committed.
6. Verify authentication and authorization.
7. Verify API error handling.
8. Verify loading, empty and error states.
9. Verify responsive behavior.
10. Verify external API fallbacks.
11. Verify AI provider fallback if one exists.
12. Verify seed/demo data.
13. Deploy.
14. Open the deployed app in a clean browser context.
15. Execute the exact demo path from start to finish.
16. Report:
    - what passed
    - what was fixed
    - known limitations
    - deployed URL if available
