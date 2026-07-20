# 📝 Naming Standards

Consistent naming conventions improve readability, maintainability, and collaboration across the semantic model. This project follows a standardized naming approach to ensure tables, columns, and measures are intuitive, consistent, and easy to understand.

---

## Table Naming

Tables are prefixed according to their role within the semantic model.

| Prefix | Description | Example |
|--------|-------------|---------|
| `dim_` | Dimension tables | `dim_products` |
| `fact_` | Fact tables | `fact_sales` |

---

## Column Naming

Columns use **snake_case** with descriptive, business-friendly names.

**Examples**

```text
product_name
customer_name
sales_amount
order_date
unit_price
```

---

## Key Naming

Different suffixes are used to distinguish between source system identifiers and model keys.

### Source System IDs (`_id`)

Columns imported directly from the source system retain the `_id` suffix.

**Examples**

```text
customer_id
product_id
campaign_id
```

### Surrogate & Foreign Keys (`_key`)

Keys used to establish relationships within the semantic model use the `_key` suffix.

**Examples**

```text
customer_key
product_key
campaign_key
date_key
geo_key
```

This distinction makes it easy to identify whether a column originates from the source system or is part of the dimensional model.

---

## Measure Naming

Measures use clear business terminology rather than technical abbreviations.

**Examples**

```text
Total Sales
Total Orders
Inventory Value
Sales vs Target
Average Delivery Time
```

This improves discoverability for both report developers and business users.

---

## General Guidelines

The following conventions were applied throughout the project:

- Use English names
- Use lowercase with `snake_case` for tables and columns
- Prefix dimension tables with `dim_`
- Prefix fact tables with `fact_`
- Preserve source system identifiers with the `_id` suffix
- Use `_key` for surrogate and foreign keys in the semantic model
- Use descriptive, business-friendly names
- Avoid unnecessary abbreviations
- Apply naming conventions consistently across the model

---

## Benefits

Following consistent naming standards provides:

- Improved readability
- Easier navigation
- Clear distinction between source IDs and model keys
- Better collaboration
- Simpler maintenance
- Consistent business terminology

---

## Summary

A consistent naming convention makes the semantic model easier to understand, maintain, and extend. By distinguishing **source system identifiers (`_id`)** from **semantic model keys (`_key`)**, the model remains intuitive for both developers and report authors while supporting long-term scalability.
