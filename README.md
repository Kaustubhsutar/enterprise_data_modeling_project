<div align="center">

# Enterprise Data Modeling in Power BI
### Transforming a Chaotic OLTP Database into an Enterprise-Ready Star Schema

<p align="center">

<!-- Technology -->

<img src="https://img.shields.io/badge/Technology-Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
<img src="https://img.shields.io/badge/Power_Query-217346?style=for-the-badge"/>
<img src="https://img.shields.io/badge/DAX-0F6CBD?style=for-the-badge"/>

<br>

<!-- Data Modeling -->

<img src="https://img.shields.io/badge/Data_Modeling-Star_Schema-blue?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Dimensional_Modeling-Kimball-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Semantic_Model-Enterprise-purple?style=for-the-badge"/>

<br>

<!-- Advanced Concepts -->

<img src="https://img.shields.io/badge/Junk_Dimension-Implemented-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Factless_Fact-Implemented-informational?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Accumulating_Snapshot-Implemented-9cf?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Dynamic_RLS-Enabled-red?style=for-the-badge"/>

<br>

<!-- Status -->

<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge"/>
<img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge"/>

</p>

### Enterprise Semantic Modeling • Star Schema Design • Dynamic Security • Advanced Power BI Data Modeling

This project demonstrates the complete transformation of a highly normalized operational database into an enterprise-ready analytical model using dimensional modeling principles, Power Query, DAX, and Power BI.

⭐ **If you found this project useful, consider starring the repository!**

</div>

---

# 📖 Executive Summary

Business Intelligence projects are only as strong as the data model behind them.

Unlike traditional Power BI portfolio projects that begin with clean analytical datasets, this project starts with a fragmented operational database containing poorly structured transactional tables, duplicated entities, inconsistent naming conventions, and complex relationships.

The objective was to redesign the entire database into an enterprise-grade semantic model capable of supporting secure, scalable, and high-performance analytics.

The project demonstrates real-world dimensional modeling techniques commonly used in enterprise Business Intelligence solutions, including:

- Star Schema Design
- Fact & Dimension Modeling
- Power Query Data Transformation
- Junk Dimension
- Factless Fact Table
- Accumulating Snapshot Fact
- Role-Playing Dimensions
- Dynamic Row-Level Security (RLS)
- Enterprise Semantic Modeling
- Model Governance

Rather than focusing only on dashboards, this project emphasizes **data architecture**, **model performance**, **maintainability**, and **business usability**.

---

# 🎯 Business Problem

The source database represented an operational (OLTP) system designed for transactional processing rather than analytics.

As a result, several challenges existed:

- Highly normalized schema
- Fragmented business entities
- Duplicate information across tables
- Multiple transactional processes
- Mixed data granularities
- Complex relationship network
- Technical naming conventions
- No centralized semantic layer
- Difficult report development
- Limited scalability for self-service analytics

Without redesigning the model, creating accurate and maintainable Power BI reports would be both time-consuming and error-prone.

This project addresses these challenges by applying dimensional modeling principles to transform the operational database into an optimized analytical model.

---

# 🎯 Project Objectives

The project was designed with the following objectives:

| Objective | Description |
|-----------|-------------|
| Transform OLTP into OLAP | Convert a normalized operational database into an analytical model |
| Build Star Schema | Design a scalable dimensional model |
| Improve Performance | Reduce relationship complexity and optimize filtering |
| Reusable Dimensions | Create shared business dimensions |
| Secure Analytics | Implement Dynamic Row-Level Security |
| Enterprise Standards | Apply naming conventions and governance |
| Self-Service BI | Simplify report development for business users |
| Model Maintainability | Build an architecture that is easy to extend |

---

# 🏗️ Solution Architecture

```text
              Dimension Tables
────────────────────────────────────────────

Customers
Products
Campaigns
Geography
Date
Order Flags

────────────────────────────────────────────
                │
                │
        Shared Relationships
                │
                ▼

        Fact Sales
             │
             ├───────────────┐
             │               │
             ▼               ▼

Fact Inventory      Fact Order Process

             │
             ▼

Fact Campaign Spend

             │
             ▼

Fact Promotion Coverage

             │
             ▼

Fact Sales Target

────────────────────────────────────────────

Supporting Tables

• Exchange Rates
• Security (Dynamic RLS)

```

---

# 🗂 Dataset Overview

The project is based on a simulated enterprise sales environment containing multiple operational business processes.

The original dataset consisted of over twenty highly normalized tables representing various business domains.

## Business Areas Included

- Orders
- Customers
- Products
- Inventory
- Campaigns
- Payments
- Shipments
- Invoices
- Exchange Rates
- Customer Contacts
- Geography
- Sales Targets
- Security Mapping

The objective was to consolidate these disconnected operational entities into reusable business dimensions and analytical fact tables.

---

# 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Power BI Desktop | Semantic model & reporting |
| Power Query | Data extraction & transformation |
| DAX | Business calculations |
| Data Modeling | Star Schema implementation |
| Dimensional Modeling | Enterprise architecture |
| GitHub | Version control & documentation |

---

# 🔄 Development Workflow

```text
Raw Operational Database
            │
            ▼
Data Investigation
            │
            ▼
Power Query Transformation
            │
            ▼
Dimension Modeling
            │
            ▼
Fact Modeling
            │
            ▼
Relationship Design
            │
            ▼
Semantic Model
            │
            ▼
DAX Measures
            │
            ▼
Dynamic Row-Level Security
            │
            ▼
Enterprise Power BI Solution
```

---

# 📁 Repository Structure

```bash
Enterprise_Data_Modeling_PowerBI/
│
├── Documentation/
│
├── Docs/
│   ├── Model/
│   │   ├── Before Model.png
│   │   └── Final Model.png
│   │
│   ├── Security/
│   │   ├── Before RLS.png
│   │   └── After RLS.png
│   │
│   ├── Dashboard/
│   │   └── Dashboard Preview.png
│   │
│   └── Power Query/
│       └── Query Structure.png
│
├── README.md
│
└── LICENSE
```

---

# 📊 Model Transformation

## Before — Operational Database (OLTP)

The original model contained:

- 20+ operational tables
- Complex relationship network
- Multiple business processes
- Technical naming conventions
- Mixed granularities
- Duplicate customer information
- Duplicate product attributes
- No semantic layer
- Difficult navigation

**Model View**

```text
📷 Docs/Model/Before Model.png
```

<!-- Insert Screenshot -->

<p align="center">
<img src="Docs/Model/Before Model.png" width="100%">
</p>

---

## After — Enterprise Semantic Model

The redesigned model follows dimensional modeling principles.

Highlights include:

- Star Schema
- Shared Dimensions
- Multiple Fact Tables
- Centralized Date Dimension
- Geography Dimension
- Junk Dimension
- Role-Playing Dimensions
- Dynamic RLS
- Dedicated Measure Table
- Business-Friendly Naming

<p align="center">
<img src="Docs/Model/Final Model.png" width="100%">
</p>

---

**(Continue with "Data Modeling Methodology" in the next part.)**
