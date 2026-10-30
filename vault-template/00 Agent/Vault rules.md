---
type: rules
updated: 2026-10-30
---
# Vault rules (for the agent)

How the vault is organised and how we work. The agent reads this before any change and updates it when something changes.

## How we work
- The owner says what to add, in their own words, even messily. The agent decides where and how it goes, following the rules below.
- The agent fills in known technical details of a model (specifications) but **never invents** personal data. Unknown fields stay empty.
- If an object already exists, it is updated, not duplicated.
- When a new kind of information appears, the agent proposes a rule and adds it here.

## Folders
| Folder | What it holds |
|---|---|
| `00 Agent/` | This file, the hand-off note and the notifications guide |
| `Inventory/<Category>/` | One note per object; `Inventory/Inventory.base` is the table with saved views |
| `Library/` | One note per book; `Library/Authors/` one note per author |
| `Journal/<Year>/` | One note per event: `YYYY-MM-DD Short title` |
| `Templates/` | Templates for new notes |
| `Attachments/Manuals/<Note name>/` | Manuals and documents, with the extracted text next to each PDF (`<name>.txt`, page markers `=== PAGE N ===`) |

## Note names
- Objects: `Brand Model` (e.g. `Example Router`).
- Books: `Title - Author`.
- Journal: `YYYY-MM-DD Short title`.

## Properties
**Object:** category, brand, model, product_code, serial, owner, quantity, location, purchase_date, shop, price, warranty_until, state, to_do, tags.
**Car (extra):** registration, vin, km, insurance_until, inspection_until.
**Book:** author (list of links), year, publisher, isbn, language, genre, status, rating, lent_to, tags.

## Change history
- 2026-05-01: created the vault with Inventory and Library.
- 2026-05-03: added the `to_do` property and the "Waiting for repair" view.
- 2026-05-10: manuals with extracted text and page markers; answers cite the page.
- 2026-06-02: added the Journal.
