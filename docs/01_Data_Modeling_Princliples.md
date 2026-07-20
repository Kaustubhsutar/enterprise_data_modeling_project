# Data Modeling Principles

This project transforms a normalized OLTP database into an enterprise-ready Power BI semantic model by applying industry-standard dimensional modeling techniques. These principles improve performance, maintainability, and scalability while providing a clean foundation for analytical reporting.

---

## Star Schema

Each business process is modeled using a central **Fact Table** surrounded by related **Dimension Tables**. This simplifies relationships, improves query performance, and makes report development more intuitive.

---

## Galaxy Schema

The final semantic model follows a **Galaxy Schema**, where multiple fact tables share common dimensions instead of connecting directly to one another.

**Fact Tables**
- fact_sales
- fact_inventory
- fact_sales_target
- fact_campaign_spend
- fact_promotion_coverage
- fact_order_process

**Shared Dimensions**
- dim_products
- dim_customers
- dim_date
- dim_campaign

---

## Table Grain

Every table was designed with a clearly defined grain before any transformations were performed.

Examples:

| Table | One Row Represents |
|--------|--------------------|
| fact_sales | One sales transaction |
| fact_inventory | One inventory snapshot |
| dim_products | One product |
| dim_customers | One customer |

---

## Shared (Conformed) Dimensions

Shared dimensions provide a **single source of truth** across multiple fact tables, enabling consistent business definitions and cross-functional analysis.

Implemented shared dimensions include:

- dim_products
- dim_customers
- dim_campaign
- dim_date

---

## Surrogate Keys

Surrogate keys were used to uniquely identify dimension records and establish reliable relationships within the semantic model.

Naming convention:

- `product_key`
- `customer_key`
- `campaign_key`

---

## Junk Dimension

Low-cardinality attributes such as **Status**, **Priority**, and **Channel** were consolidated into a single **Junk Dimension** (`dim_order_flags`) instead of creating multiple small lookup tables.

---

## Role-Playing Dimension

A **Role-Playing Dimension** is a single dimension that participates in multiple relationships by serving different business roles.

While the **Date** dimension is the most common example, this project implements **dim_geo** as the role-playing dimension.

The **dim_geo** table is related to two different columns in `fact_sales`:

- **bill_to_city**
- **ship_to_city**

This enables analysis from both the **billing location** and **shipping location** perspectives while reusing a single Geography dimension.

---

## Factless Fact

The **fact_promotion_coverage** table records business events without storing transactional measures, enabling event and coverage analysis.

---

## Accumulating Snapshot Fact

The **fact_order_process** table tracks the complete order fulfillment lifecycle by storing milestone dates within a single record.

This supports analysis such as:

- Order-to-Ship Time
- Order-to-Delivery Time
- Fulfillment Performance
- SLA Monitoring

---

## Measures Table

A dedicated **Measures** table centralizes all DAX calculations, ensuring consistent business logic, improving discoverability, and simplifying report development.
