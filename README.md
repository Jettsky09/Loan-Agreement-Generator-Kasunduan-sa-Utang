# 📄 Loan Agreement Generator — Kasunduan sa Utang

A single-file, offline-capable HTML tool for generating formal Filipino loan agreement documents. Built for **Juan & Wife Dela Cruz**.

---

## Features

- **Live preview** — the document updates in real-time as you fill in the form
- **No internet required** — works fully offline once downloaded
- **Print to PDF** — generate a clean, printable PDF directly from the browser
- **Dynamic lender selection** — choose Juan, Wife, or both as the lender
- **Optional sections** — collateral, remata clause, term length, and witnesses can be toggled on or off
- **Auto-filled Petsa & Lugar** — the date at the bottom of the document mirrors what you enter in the form; the place is pre-filled as _Malacanang, Palace_

---

## How to Use

1. **Open** `loan-agreement-generator.html` in any modern browser (Chrome, Edge, Firefox, Safari).
2. **Fill in the form** on the left panel:
   - Borrower's name and address
   - Loan amount and date received
   - Monthly interest rate, monthly payment amount, and due day
   - Optional: term length, collateral details, remata clause, witnesses
3. **Check the preview** on the right to see the document update live.
4. Click **⬇ I-download bilang PDF** and select **Save as PDF** as the destination in the print dialog.

---

## Form Fields

| Field                 | Description                                             |
| --------------------- | ------------------------------------------------------- |
| Pangalan ng Umuutang  | Full name of the borrower                               |
| Tirahan ng Umuutang   | Complete address of the borrower                        |
| Halaga ng inutang     | Loan amount in Philippine Peso (e.g. `10,000`)          |
| Petsa ng pagtanggap   | Day, month, and year the money was received             |
| Buwanang interes (%)  | Monthly interest rate (e.g. `5` for 5%)                 |
| Buwanang tubo (Php)   | Computed monthly interest in pesos                      |
| Bayad tuwing ika-\_\_ | Day of the month payment is due                         |
| May takdang buwan     | Toggle: adds a fixed repayment term in months           |
| May kolateral         | Toggle: adds a collateral clause                        |
| REMATA clause         | Toggle: lender may seize/sell collateral on default     |
| Nagpapautang          | Select Juan, Wife, or both as lender(s)                 |
| Saksi                 | Toggle: adds a witness section with dynamic name fields |

---

## Document Structure

The generated _Kasunduan sa Utang_ contains:

1. **Paragraph 1** — Borrower identity, address, lender(s), amount, and date received
2. **Paragraph 2** — Interest rate, monthly payment, due date, and optional term
3. **Collateral clause** — either a description of the collateral or a statement that none exists
4. **Default clause** — consequences of non-payment (with or without remata)
5. **Signature block** — borrower and lender(s)
6. **Witness section** _(if enabled)_ — one or more witness signature lines
7. **Petsa at Lugar** — always appears at the bottom

---

## Pre-filled Defaults

| Field        | Default Value                                  |
| ------------ | ---------------------------------------------- |
| Lugar        | Malacanang, Palace                             |
| Nagpapautang | Juan Dela Cruz & Wife Dela Cruz (both checked) |

---

## Technical Notes

- Pure HTML/CSS/JavaScript — no frameworks, no dependencies, no build step
- All logic runs client-side; no data is sent to any server
- Print styles are included for clean A4 output (decorative borders hidden on print)
- Tested on Chrome and Edge; `window.print()` is used for PDF export

---

## File

```
loan-agreement-generator.html   ← the entire app in one file
```
