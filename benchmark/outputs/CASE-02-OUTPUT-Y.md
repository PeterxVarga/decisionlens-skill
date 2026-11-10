# CASE-02 — OUTPUT-Y

# RAW EXECUTION

Case: CASE-02
Lane: [REDACTED]


## INITIAL USER CASE

# CASE-02 — LedgerGrid

You are reviewing **LedgerGrid**, a live finance reconciliation SaaS.

Its main reconciliation workspace is a dense table.

Each row is a transaction/reconciliation item. The visible columns are:

- account;
- date;
- counterparty;
- amount;
- source;
- match state;
- owner;
- exception reason.

Users can:
- sort/filter;
- compare nearby rows;
- multi-select;
- bulk assign;
- resolve exceptions inline.

Observed research and telemetry:

- Expert users reconcile for 1–3 hours at a time.
- Typical sessions involve comparing 8–12 rows repeatedly.
- Users frequently compare the same 5–7 columns across adjacent rows.
- 74% of resolved exceptions use inline or bulk actions.
- 92% of reconciliation sessions are on displays 1440px wide or larger.
- 6% are tablet.
- 2% are mobile; mobile users mostly check status and do not perform full reconciliation.
- In moderated testing, users explicitly valued seeing more items without opening each one.

A stakeholder says:

> “Tables feel old. We should replace this with modern cards so each transaction is easier to understand.”

Review this decision. You may recommend responsive differences if justified. Do not build the UI.


## ASSISTANT TURN 1

## Findings

| Severity | Area | Evidence | User impact | Recommendation |
| --- | --- | --- | --- | --- |
| P1 | Primary reconciliation workspace | Work is comparison-heavy: users repeatedly scan 5–7 fields across 8–12 adjacent rows; 74% resolve through inline or bulk actions. | Replacing the table with cards would increase scrolling, obscure cross-row comparison, and make selection/bulk workflows slower. | Keep the dense table as the primary desktop workspace. |
| P1 | Long expert sessions | Experts work for 1–3 hours and explicitly value seeing more items without opening details. | Card layouts consume vertical space and force repeated expand/collapse behavior, increasing fatigue and context switching. | Optimize table density, readability, and progressive detail—not card conversion. |
| P2 | Responsive behavior | 92% of sessions are ≥1440px; mobile is primarily status checking. | One layout for every device would compromise the dominant desktop task. | Use task-specific responsive modes: table on desktop, condensed review/status views on tablet and mobile. |
| P2 | Row comprehension | The stakeholder concern—individual transactions being easier to understand—is valid, but does not require cards. | Important detail can be hard to inspect if every column competes equally. | Add a row details panel, expandable inline detail, or inspector drawer while preserving the comparison grid. |

## Decision

Do not replace the reconciliation table with cards.

LedgerGrid’s core job is not reading isolated transactions; it is rapidly comparing adjacent records, spotting exceptions, selecting several items, and resolving them inline. A table is the appropriate interaction model for that work. “Modern” should mean clearer hierarchy, better states, and faster resolution—not abandoning the format that best supports the task.

## Recommended flow

Current effective model:

`Filter/sort → compare neighboring rows → multi-select → inline or bulk resolve`

Recommended refinement:

`Filter/sort → scan a stable, dense table → compare pinned key columns → inspect selected row in-place/side panel → inline or bulk resolve → clear success and next-exception feedback`

## UX direction

- Keep frequently compared columns visible and consistently ordered: account, date, counterparty, amount, source, match state, owner, exception reason.
- Support horizontal density without losing orientation: pin account/date/counterparty and match state; allow users to choose optional columns.
- Make exception reason and match state visually scannable with text labels plus restrained color—not color alone.
- Preserve row height appropriate for long sessions; offer a compact/default density choice rather than forcing oversized rows.
- Use a details drawer or expandable row for supporting metadata, audit history, notes, attachments, and actions that do not need constant cross-row comparison.
- Make multi-select unmistakable: persistent selection count, clear bulk action bar, safe undo where resolution can be reversed, and confirmation only for consequential changes.
- Keep filters, sorting, column visibility, and scroll position stable after inline updates and bulk actions.
- Provide loading, empty, permission-denied, conflict, and save-failure states without clearing selections or losing in-progress work.

## Responsive approach

- Desktop (primary): full reconciliation table, persistent filters, pinned comparison columns, multi-select, bulk actions, and optional inspector.
- Tablet: retain a horizontally scrollable table with a reduced default column set and a details drawer; avoid converting primary reconciliation to cards unless the task is intentionally narrowed.
- Mobile: optimize for status checking—exception counts, assigned items, recent changes, and a compact transaction detail view. Full reconciliation can be available but should not be presented as the primary mobile workflow.

## Accessibility and performance checks

- Use a semantic table where feasible, with clear column headers and sortable-header state.
- Ensure keyboard users can move through rows, select items, open details, and invoke bulk actions with visible focus and predictable focus return.
- Do not make hover the only way to reveal row actions or exception detail.
- Virtualize very large datasets carefully: preserve keyboard navigation, selection state, screen-reader context, and a stable scroll position.
- Reserve space for bulk-action bars and inline status changes to prevent layout shifts during active reconciliation.

## Remaining risk

Before changing density or column priority, validate with expert users using realistic 8–12-row comparison tasks. The key success measures are time to resolve, row-to-row comparison errors, bulk-action completion, and reported fatigue—not whether the surface appears more contemporary.
