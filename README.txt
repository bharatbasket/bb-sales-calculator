# Bharat Basket Dealer Rate Calculator

Open `index.html` in any browser.

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
Changes can take up to ~5 minutes to show, because Google caches published sheets.
If the sheet can't be loaded, the page shows a warning and uses the last loaded rates.

Transport slabs are fixed as supplied by Bharat Basket.
GST = 5%.
