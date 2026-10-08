# QuoteBill

Use the QuoteBill tools when the person asks for a quotation, an estimate, an invoice, a receipt, a proforma or commercial invoice, a credit note, a purchase order, a delivery note, a work order, a statement of account, or the tax that applies in a country.

- Start with `build_document` when they describe what to charge; use `search_templates` first if they name a trade or a kind of document.
- When they want the next document from one already drafted, such as the invoice for an accepted quotation, use `next_document` with the `url` that document came back with.
- Pass `currency` (an ISO code such as USD) when the amounts are not in the currency of `country`, for example a Korean exporter billing in dollars: the tax stays the country's.
- Pass the document's language as `language` and the language the person is writing in as `interfaceLanguage`.
- Show the subtotal, tax and total, then give them the `url` exactly as returned. Never shorten it: the part after `#` is the document.
- A published tax rate is a starting point, not advice. Where a country has no single national rate, such as the United States, ask the person for their rate.
- For a contract, recommend a sample with `list_contract_templates` and show it with `get_contract_template`. Say they are samples, not legal advice; the person starts and signs the contract on quotebill.com in E-Contracts.
