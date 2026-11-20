# Bharat Basket Dealer Rate Calculator

Open the hosted page (e.g. GitHub Pages). Opening `index.html` straight from
disk may not load the Google Sheet; the page then shows a warning and default rates.

The page shows, per product, Ex-Factory + GST and FOR + GST (ex-factory +
distance-slab transport, then 5% GST). Logo and colours follow bbasket.in.

Daily ex-factory rates are read from the admin's Google Sheet (link set in
SHEET_CSV_URL inside index.html). Only people with edit access to the sheet
can change rates; salesmen can only view. The sheet's version history keeps
a record of every change.

Sheet format (first tab, header row, one product per row):
  Product        | Rate    | Unit
  Packing        | 163.53  | L
  15L            | 2432.09 | TIN
  15Kg           | 2661.25 | TIN
  13Kg           | 2321.75 | TIN
  Kachi Ghani 1L | 167.53  | L

Unit must be L (transport per litre) or TIN (transport per tin).
For L products, a pack size in the name (e.g. "500ML", "2 L", "5 L") multiplies
the per-litre transport; names without a size are treated as 1 litre.
Enter rates WITHOUT GST; the page adds 5%.
Changes can take up to ~5 minutes to show, because Google caches published sheets.
If the sheet can't be loaded, the page shows a warning and uses the last loaded rates.

Transport slabs (per litre; per tin = 15 x per litre), as supplied by Bharat Basket:
  0-50 KM 0.50 | 50-100 1.00 | 100-150 1.50 | 150-200 2.00
  200-250 2.50 | 250-300 3.00 | 300-350 3.00 | 350-400 3.00
GST = 5%.
