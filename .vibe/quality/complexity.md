# complexity.md — complexity budget

Track every change for:
- files changed
- lines changed
- new dependencies
- new abstractions
- new services
- new DB tables
- new API endpoints
- new state management
- new infrastructure

Default budget:
```yaml
change_budget:
  preferred_files: 1-5
  preferred_lines: 20-300
  max_lines_without_review: 500
  max_new_dependencies: 1
  max_new_architectural_components: 1
```

A tiny feature needing 3 packages, 2 services, 4 abstractions, 7 files → stop and split.
Complexity should be justified, not celebrated.
