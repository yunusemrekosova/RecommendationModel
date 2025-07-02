# Co-Occurrence Based Recommendation Model

This repository contains a Python notebook implementing a co-occurrence based recommendation model. It analyzes shopping cart data to recommend products frequently bought together, ideal for use in e-commerce and similar applications.

## Objective

The model generates real-time product recommendations by analyzing historical transaction data, specifically highlighting products that customers commonly purchase together.

## Data Requirements

Ensure your data files are in CSV format, using a semicolon (`;`) as the delimiter.

### Required Data Files:

- **ShoppingCart.csv** (essential data)

  - `UserId`
  - `ProductId`
  - `OrderId`
  - `CustomerId`
  - `Quantity`

- **Customers.csv** (used only for testing)

  - `CustomerId`
  - `CustomerName`

- **Products.csv** (used only for testing)

  - `ProductId`
  - `ModelNumber`

## Environment Setup

Standard Python libraries used:

- pandas
- numpy
- scipy

Install dependencies via pip:

```bash
pip install pandas numpy scipy
```

## Parameters

You can customize the model by adjusting the following parameters:

- **Minimum transaction count per customer**: Filters customers based on how many transactions they have made.
- **Minimum item count per shopping cart**: Filters shopping carts based on the number of items per cart.
- **top\_n**: Determines how many recommendations the model provides.

Adjust these parameters in the notebook according to the specifics of your dataset and project requirements.

## Usage Instructions

1. Prepare and place your data files (`ShoppingCart.csv`, `Customers.csv`, `Products.csv`) in the same directory as the notebook.
2. Adjust filtering parameters (`min_transactions`, `min_cart_items`) in the notebook according to your dataset.
3. Set the number of desired recommendations by modifying the `top_n` value in the recommendation function.
4. Execute notebook cells sequentially from start to finish.

## Expected Output

After execution, the notebook generates:

- A co-occurrence matrix of products
- Recommendations for specified products based on historical co-purchases
- Optional lookups displaying customer names and product model numbers for easier validation

## Customization

You can easily adjust recommendation thresholds and the number of recommendations returned by modifying the notebook parameters.

---

Enjoy using this recommendation model in your projects!
