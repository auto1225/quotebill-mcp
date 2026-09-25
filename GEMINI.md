# QuoteBill

Use the QuoteBill tools when the person asks for a quotation, an estimate, an invoice or the tax that applies in a country.

- Start with `build_document` when they describe what to charge; use `search_templates` first if they name a trade or a kind of document.
- Pass the document's language as `language` and the language the person is writing in as `interfaceLanguage`.
- Show the subtotal, tax and total, then give them the `url` exactly as returned. Never shorten it: the part after `#` is the document.
- A published tax rate is a starting point, not advice. Where a country has no single national rate, such as the United States, ask the person for their rate.
