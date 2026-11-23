# Offline-bill-generator
A standalone HTML tool to generate invoices offline

# Document Studio — Quotation, PO, Invoice & Delivery Note Generator

A standalone, zero-dependency, browser-based business document studio built with pure HTML, CSS, and JavaScript. Designed for marine, logistics, and commercial supply operations, it allows users to create, customize, preview, and print A4-formatted **Quotations**, **Purchase Orders (PO)**, **Invoices**, and **Delivery Notes** with offline local persistence.

---

## Key Features

- **4-in-1 Document Modes:** Dynamically switches layout headers, table columns, and footer notes between **Quotation**, **Purchase Order**, **Invoice**, and **Delivery Note** modes.
- **One-Click Document Conversion:** Independently copy line items and metadata across workflows (e.g., *Quote → PO*, *PO → Invoice*, or *Invoice → Delivery Note*).
- **Live A4 Print Preview:** Real-time WYSIWYG A4 sheet preview with clean print media styling (`Ctrl + P` / *Print / PDF* button) that hides editor panels and formats cleanly for PDF export.
- **Excel Copy-Paste Import:** Paste tab-separated rows directly from Microsoft Excel or Google Sheets to bulk-populate line items (including sub-item numbering like `1.50` and `**red highlight**` notes).
- **Multi-Currency & Tax Engine:** Supports `USD ($)`, `INR (₹)`, `SGD (S$)`, and `EUR (€)` with automatic calculations for `CGST 9% + SGST 9%`, `IGST 18%`, custom `Discount %`, or tax-exempt totals.
- **Authorization & Branding Controls:** Toggle between **Sign + Seal**, **Sign Only**, or a **Blank Line** for manual signing, plus an optional partner badge in the Delivery Note footer.
- **Offline Vault & Dual-Folder Backup:**
  - Automatically stores records and saved customer/vendor addresses locally in **IndexedDB**.
  - Uses the browser's **File System Access API** to link up to two local or cloud-synced directories (e.g., Local Drive + Google Drive/OneDrive folder), saving individual `.json` files alongside a consolidated `Master_Document_Register.csv`.
  - Supports `.txt`, `.json`, and printable `.pdf` export/import for the address book.

---

## Quick Start

1. Download or clone this repository.
2. Open the `.html` file directly in any modern desktop browser (**Google Chrome** or **Microsoft Edge** recommended for local folder backup support).
3. Select a **Document Type** from the left editor panel, fill in your details, and click **Print / PDF** to generate an A4 document.

---

## Roadmap & Future Enhancements

| Planned Feature | Description | Status |
| :--- | :--- | :--- |
| **Password / PIN Lock for Bank Details** | Add a PIN-protected lock toggle (`Lock` / `Unlock to Edit` + `Change PIN` stored in IndexedDB) on the **Bank Account Details** section in Invoice Mode to prevent accidental or unauthorized edits to remittance account numbers, IFSC, and SWIFT codes. | Planned |
| **Custom Branding Settings Panel** | UI controls to upload custom company logos, signatures, and corporate seals directly from the browser without editing the HTML source. | Planned |
| **Multi-Page Table Pagination** | Automatic repeating table headers and page numbering (`Page X of Y`) for long line-item lists spanning multiple A4 pages. | Planned |
