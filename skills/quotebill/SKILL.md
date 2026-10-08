---
name: quotebill
description: Draft quotations, invoices, proforma and commercial invoices, receipts, credit notes, purchase orders, delivery notes, work orders and statements of account with QuoteBill, and look up the tax that applies in a country. Use when the person asks for any of these documents or for a country's VAT/GST/sales tax rate.
---

# QuoteBill

Use the QuoteBill MCP tools (`search_templates`, `get_template`, `get_tax_rule`, `calculate_totals`, `build_document`, `next_document`, `list_guides`, `list_reference`) whenever the person wants a sales document or a tax rate.

1. Start with `build_document` when they describe what to charge. Use `search_templates` first if they name a trade or a kind of document.
2. When they want the next document from one already drafted (the invoice for an accepted quotation, the receipt for a paid invoice), call `next_document` with the `url` that document came back with.
3. Pass `currency` (an ISO code such as USD) when the amounts are not in the currency of `country`, for example a Korean exporter billing in dollars: the tax stays the country's.
4. Pass the document's language as `language` and the language the person is writing in as `interfaceLanguage`.
5. Show the subtotal, tax and total, then give them the `url` exactly as returned. Never shorten or edit it: the part after `#` is the document.
6. A published tax rate is a starting point, not tax advice. Where a country has no single national rate, such as the United States, ask the person for their rate instead of guessing.
7. If a tool says the person is not signed in, tell them to run `/mcp`, choose `quotebill` and sign in (free account).
