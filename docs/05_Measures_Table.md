# 🧮 Measures Table

This project centralizes all DAX measures into a dedicated **Measures** table instead of distributing them across fact and dimension tables.

This approach keeps the semantic model organized, improves discoverability, and ensures business calculations are maintained in a single location.

---

## Why a Measures Table?

By default, Power BI allows measures to be created in any table. As models grow, this can make measures difficult to locate and maintain.

A dedicated Measures table provides:

- Centralized business calculations
- Cleaner field list
- Easier maintenance
- Consistent KPI definitions
- Better developer experience

---

## Organization

Measures are grouped into **Display Folders** based on their business domain.

Example:

```text
📁 Sales KPIs
    ├── Total Sales
    ├── Total Orders
    ├── Average Order Value

📁 Inventory KPIs
    ├── Inventory Value
    ├── Stock on Hand

📁 Customer KPIs
    ├── Total Customers
    ├── Repeat Customers

📁 Time Intelligence
    ├── YTD Sales
    ├── Previous Year Sales

📁 Operational KPIs
    ├── Average Delivery Time
    ├── Order Processing Time
```

This structure keeps related measures together and simplifies navigation.

---

## Naming Convention

Measures follow clear, business-friendly naming conventions.

Examples:

```text
Total Sales
Total Orders
Inventory Value
Average Delivery Time
Sales vs Target
```

Technical abbreviations are avoided wherever possible to improve readability for report developers and business users.

---

## Best Practices Followed

- Store all measures in one dedicated table
- Organize measures using Display Folders
- Use descriptive business names
- Reuse existing measures where possible
- Keep calculations modular and maintainable

---

## Benefits

Using a dedicated Measures table provides:

- Improved organization
- Faster measure discovery
- Consistent business logic
- Easier collaboration
- Better long-term maintainability

---

## Summary

A dedicated Measures table separates business logic from data storage, resulting in a cleaner semantic model that is easier to navigate, maintain, and scale as new KPIs and analytical requirements are introduced.
