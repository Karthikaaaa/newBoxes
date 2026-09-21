# Risk register table

Vue 3 + TypeScript + Vite. No backend: data comes from `src/data/risks.json`.

```bash
npm install
npm run dev        # http://localhost:5173
npm run typecheck
```

- `http://localhost:5173/?rows=10000` generates 10,000 messy rows to check performance.
- Read `DECISIONS.md` for scope, assumptions and API feedback.

## Layout

- `src/composables/useRiskTable.ts`: filter, sort, paginate, status edit (all state lives here)
- `src/normalize.ts`: cleans API data once at the boundary
- `src/components/`: SeverityChip, OwnerAvatar, OwnerSelect, FilterPanel, ActiveFilters, StatusCell, RiskTable, Pagination
- `src/data/`: fake API, sample JSON, generator, owner lookup
