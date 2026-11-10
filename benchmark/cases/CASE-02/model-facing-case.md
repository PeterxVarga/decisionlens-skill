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