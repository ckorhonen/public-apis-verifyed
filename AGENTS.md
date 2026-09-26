# Repository instructions

`README.md` is the canonical API table; `CONTRIBUTING.md` defines categories, alphabetical ordering, description length, and Auth/HTTPS/CORS values. Preserve those conventions and the free-access eligibility rules. `db/` is generated; do not hand-edit it.

`scripts/db/update-db.js` parses README tables through `utils/db/` and writes `db/resources.json` and `db/categories.json`. The root package exposes `npm run update-db`, with no test, lint, typecheck, or app build script. This generator writes files and is not a read-only link check. Use the repository's Node dependency setup only when generator work requires it.

For table changes, inspect the changed rows, allowed values, category/TOC links, duplicates, and `git diff --check -- <changed-paths>`. Validate only changed remote links as necessary; do not crawl or invoke every API. Prose-only instruction edits need no database regeneration.

The main-branch update-db workflow generates and commits database changes. The scheduled/manual broken-link workflow can create/update issues; neither workflow is a local validation substitute or permission to publish. Distinguish checked links, generated data, and unverified service availability in the completion report.

Complete the authorized change through relevant verification and repair of introduced failures. Resolve routine implementation choices directly; ask only for information or decisions that materially affect the result. If blocked, name the affected action and missing prerequisite, continue independent work, and close with changed paths, checks actually run, and unverified behavior.
