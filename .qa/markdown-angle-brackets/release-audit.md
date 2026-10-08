# Release audit (synthetic QA fixture)

- Method: <https://example.com/docs/audit>
- Parser helpers such as Parse<Number>() and List<Item> appear in prose.

## Open findings (6)

| ID | Location | Problem | Status | Upstream |
|---|---|---|---|---|
| w01-1 | `lib/scale.js:120` | Zoom only accepts 1<ratio<2 and rejects the rest silently | reproduced | none |
| w02-1 | `lib/export.js:88` | Export button stays disabled after save | reproduced | none |
| w03-1 | `src/sync.ts:410` | Sync retries forever when offline | reproduced | reported |
| w04-2 | `src/queue.ts:57` | Queue drops the last item when full | reproduced | none |
| w05-1 | `lib/render.js:301` | List flickers when one row updates | reproduced | none |
| w06-3 | `src/upload.ts:99` | Upload progress resets at 50% | reproduced | none |

## Regressions on main (3)

| ID | Location | Problem | Status | Upstream |
|---|---|---|---|---|
| r01-1 | `lib/theme.js:42` | Dark theme ignores the system setting | reproduced | none |
| r02-1 | `lib/search.js:150` | Search box loses focus after typing | reproduced | none |
| r03-1 | `src/retry.ts:226` | Status 429 -> shown as a generic error | reproduced | none |
