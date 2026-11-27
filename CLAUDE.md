@AGENTS.md

## Conventions

- Log every product, domain or engineering decision in [docs/decisions.md](docs/decisions.md) in the same PR as the change. Never rewrite an entry; supersede it.
- `main` is protected. Work on short-lived branches, open a PR against this repo's `main` (`gh pr create --repo slowTake/northfina-lease-loop --base main`), rebase-merge once `npm run check:all` passes locally and CI is green (D-010, D-061), so keep each commit small and green on its own.
- Write domain tests first (red, green, refactor). Expected values come from the data pack's worked example or a hand calculation, noted next to the assertion, never from running the code.
- Round money only with `roundHalfUp` from `src/domain/money.ts`, once per amount.
- `.local/` is git-ignored scratch space for plans and notes that don't belong in the submission.
