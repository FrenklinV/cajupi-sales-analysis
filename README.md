# Cajupi Sales Analysis

Exploratory analysis of restaurant point-of-sale data (invoices and product-level sales), covering revenue trends, peak hours, weekday vs. weekend behavior, top-selling products, and a June-vs-July comparison.

## What's in the notebook

1. **Data loading & cleaning** — parses dates/times, derives hour, day name, and weekday/weekend flags.
2. **Invoice-level analysis** — total revenue, invoice count, average invoice value, daily and hourly revenue trends.
3. **Product-level analysis** — top-selling products, sales by hour for key items, morning vs. afternoon behavior.
4. **Combined analysis** — merges invoices and product sales to look at which products appear in higher-value invoices and how they split across weekdays/weekends.
5. **Month-over-month comparison (June vs. July)** — revenue, invoice count, average invoice value, hourly revenue, weekday/weekend split, and peak-hour revenue.

## Data

Included in `data/`:

| File | Description |
|---|---|
| `fatura_qershor_dataset_v2.xlsx` | June invoices |
| `shitje_produkte_lidhur_me_fatura.xlsx` | Product-level sales linked to invoices |
| `fatura_korrik_dataset.csv` | July invoices |

Columns include `invoice_id`, `date`, `time`, `price_lek`, `product_name`, and `quantity`.

## Running it

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Open `Cajupi.ipynb` in Jupyter or Colab.
3. Run all cells — the notebook automatically loads the files from `data/`.
   (If `data/` isn't found — e.g. a fresh Colab session without the repo cloned in — it will prompt you to upload the files instead.)

## Notes

- Chart labels are in Albanian ("Të ardhurat" = revenue, "Sasia" = quantity, etc.).
- `price_lek` is in Albanian Lek.
