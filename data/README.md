# Data

Synthetic e-commerce data created for analytics education: a retailer of beauty and home-care products, with
51,290 order lines from 2020 to 2023. The data do not describe a real company or real people.

## `EcomSales.csv` (one row per order line)

| Column | Description |
|---|---|
| `RowID` | Line identifier |
| `OrderID` | Order identifier (an order can have several lines) |
| `OrderDate` | Order date (M/D/YYYY) |
| `CustomerID` | Customer identifier |
| `Segment` | Consumer, Corporate or Self-Employed |
| `RegionCode` | Delivery region |
| `ProductCode` | Product identifier |
| `Quantity` | Units |
| `Sales` | Line revenue (USD) |
| `Discount` | Discount rate (0–1) |
| `Profit` | Line profit (USD); negative when the line loses money |

## `Product.csv`

| Column | Description |
|---|---|
| `ProductCode` | Product identifier |
| `Product` | Product name |
| `Category`, `Subcategory` | Product hierarchy |

## `Customer.csv`

Reduced to the fields the analysis uses. Names, e-mail addresses and dates of birth from the original teaching file
were removed before publication.

| Column | Description |
|---|---|
| `CustomerID` | Customer identifier |
| `Gender` | M or F; missing for 124 customers |
| `AnnualIncome` | Annual income (USD) |
| `Occupation` | Occupation group |

## `Region.csv`

Reduced to region code, country, region and market; used only to validate region keys.

| Column | Description |
|---|---|
| `RegionCode` | Region identifier |
| `Country` | Country |
| `Region`, `Market` | Geographic grouping |

## Known data issues

Two product codes (`PPP000002`, `PPP000010`) and one region code (`RRR0001`) in `EcomSales.csv` carry a tripled
prefix. The notebook corrects them before joining.
