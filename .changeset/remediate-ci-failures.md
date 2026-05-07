---
"@keystone-6/core": patch
---

This patch remediates critical CI build failures and functional regressions introduced in recent validation hook refactoring:

- **Build Stability**: Resolved `MISSING_EXPORT` and Rollup bundling errors in `@keystone-6/core` by simplifying generic type signatures and fixing export nomenclature.
- **Validation Preservation**: Fixed a regression where field-level validation messages were swallowed if a list-level hook crashed. Field errors are now prioritized and propagated correctly.
- **Access Control Transparency**: Fixed an issue where database-level errors during unique item checks were silently swallowed. These are now correctly rethrown to prevent masked infrastructure failures.
- **API Consistency**: Standardized internal error tags and documentation to consistently use the `validate` API nomenclature instead of legacy `validateInput` references.
