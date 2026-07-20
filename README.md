<div align="center">

# 🏗️ Enterprise Power BI Data Modeling
### Power BI | Semantic Modeling | Galaxy Schema | Dimensional Modeling | Power Query | DAX

<p align="center">

<!-- Tech Stack -->

<img src="https://img.shields.io/badge/Technology-Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
<img src="https://img.shields.io/badge/Power_Query-217346?style=for-the-badge"/>
<img src="https://img.shields.io/badge/DAX-0F6CBD?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Data_Modeling-Enterprise-blue?style=for-the-badge"/>

<br>

<!-- Concepts -->

<img src="https://img.shields.io/badge/Galaxy_Schema-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Star_Schema-0052CC?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Row_Level_Security-red?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Semantic_Model-6A1B9A?style=for-the-badge"/>

<br>

<!-- Domain -->

<img src="https://img.shields.io/badge/Domain-Business_Intelligence-success?style=for-the-badge"/>

<br>

<!-- Status -->

<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge"/>
<img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge"/>

</p>

### Transforming a Complex OLTP Database into an Enterprise-Ready Galaxy Schema for Scalable Analytics

This project demonstrates the complete process of converting a messy transactional database into a clean, scalable **Power BI Semantic Model** using modern dimensional modeling techniques, Power Query transformations, DAX, and enterprise data modeling best practices.

⭐ **If you found this project valuable, consider starring the repository!**

</div>

---

# 📖 Executive Summary

Modern transactional databases (OLTP) are optimized for data entry, not analytical reporting. Their highly normalized structure often results in complex relationships, duplicate data, and poor query performance when used directly in BI tools.

This project demonstrates how to transform a complex OLTP dataset containing **23 interconnected tables** into an enterprise-grade semantic model using **Power BI**.

The final solution implements a **Galaxy Schema**, where multiple fact tables share common conformed dimensions, creating a scalable, reusable, and high-performance analytical model suitable for business intelligence and reporting.

Throughout the project, industry-standard dimensional modeling principles were applied, including:

- Star Schema
- Galaxy Schema
- Shared (Conformed) Dimensions
- Junk Dimension
- Role-Playing Dimensions
- Factless Fact Tables
- Accumulating Snapshot Fact Tables
- Dedicated Measures Table
- Row-Level Security (RLS)

The result is a semantic model that is easier to maintain, improves query performance, reduces redundancy, and provides a reliable foundation for enterprise reporting.

---

# 🎯 Business Problem

Transactional databases are designed to efficiently process business operations but are rarely suitable for analytics.

Using an OLTP model directly in Power BI often introduces several challenges:

- Highly normalized table structures
- Complex relationships
- Duplicate business logic
- Slow report performance
- Difficult DAX development
- Poor scalability
- Inconsistent business metrics

The objective of this project is to redesign the underlying data model into a semantic layer that follows enterprise data warehousing best practices while remaining intuitive for report developers and business users.

---

# 🚀 Objectives

This project focuses on designing an enterprise-ready semantic model capable of supporting scalable reporting and cross-functional analytics.

| Objective | Description |
|-----------|-------------|
| Transform OLTP into Analytics Model | Convert normalized transactional tables into dimensional structures |
| Build Enterprise Galaxy Schema | Design multiple fact tables connected through shared dimensions |
| Improve Performance | Remove unnecessary complexity and optimize relationships |
| Standardize Business Logic | Centralize reusable DAX measures |
| Enable Secure Reporting | Implement Row-Level Security (RLS) |
| Enhance Maintainability | Organize Power Query and apply consistent naming conventions |
| Ensure Data Integrity | Validate model totals throughout the transformation process |

---

# 🗂 Source Dataset Overview

The project uses a fictional enterprise transactional database containing **23 operational tables** representing multiple business processes.

The raw source data includes information related to:

- Customers
- Products
- Orders
- Sales
- Inventory
- Promotions
- Campaigns
- Geography
- Suppliers
- Returns
- Budgets

These operational tables were transformed into a dimensional model suitable for analytical reporting.

---

# 🛠️ Important Links & Tools

The project was built using the following technologies:

- **Power BI Desktop** - Semantic modeling and report development
- **Power Query** - Data extraction, cleaning, and transformation
- **DAX** - Business calculations and reusable measures
- **Excel** - Source dataset
- **GitHub** - Version control and documentation

---

# 🏗 Architecture / Workflow

```text
Raw OLTP Database (23 Tables)
            │
            ▼
Power Query (ETL)
            │
            ├── Stage Queries
            ├── Dimension Tables
            ├── Fact Tables
            └── Support Tables
            │
            ▼
Enterprise Galaxy Schema
            │
            ▼
Power BI Semantic Model
            │
            ├── Relationships
            ├── Measures
            ├── Row-Level Security
            └── Validation
            │
            ▼
Interactive Power BI Reports
```

---

# 📁 Repository Structure

```bash
Enterprise-PowerBI-Data-Modeling/
│
├── Dashboard/
│   └── Enterprise Data Modeling.pbix
│
├── Dataset/
│   └── raw_tables.xlsx
│
├── Docs/
│   ├── Images/
│   │   ├── 01_Original_OLTP_Model.png
│   │   ├── 02_Galaxy_Schema.png
│   │   ├── 03_Query_Groups.png
│   │   ├── 04_Measures_Table.png
│   │   ├── 05_Dashboard.png
│   │   └── 06_RLS_Demo.png
│   │
│   ├── Data_Modeling_Principles.md
│   ├── Data_Model_Architecture.md
│   ├── Power_Query_Organization.md
│   ├── Naming_Standards.md
│   ├── Measures.md
│   └── Row_Level_Security.md
│
├── README.md
│
└── LICENSE
```

---

# 📊 Project Phases

The project follows a structured development approach to transform the raw transactional database into a scalable semantic model.

| Phase | Description |
|--------|-------------|
| **Phase 1** | Preparation and business understanding |
| **Phase 2** | Dimension table creation |
| **Phase 3** | Fact table creation and relationship modeling |
| **Phase 4** | Security implementation, validation, and model polishing |

Detailed documentation for each phase is available throughout the repository.

---

# 🔄 Before vs After

The original dataset was structured as an **OLTP (Online Transaction Processing)** database optimized for transactional operations. While efficient for day-to-day business processes, this structure was not suitable for analytical reporting.

The model was redesigned into an **Enterprise Galaxy Schema**, providing a clean semantic layer optimized for performance, scalability, and business intelligence.

| Before (OLTP Model) | After (Galaxy Schema) |
|---------------------|-----------------------|
| Highly normalized tables | Dimensional model |
| Complex joins | Simplified relationships |
| Difficult reporting | Analytics-ready semantic model |
| Duplicate business logic | Centralized business logic |
| Limited scalability | Enterprise-ready architecture |
| Performance bottlenecks | Optimized query performance |

### Original OLTP Model

<img src="Docs/Images/01_Original_OLTP_Model.png" width="100%"/>

---

### Final Enterprise Galaxy Schema

<img src="Docs/Images/02_Galaxy_Schema.png" width="100%"/>

---

# 🏛 Final Semantic Model

The completed model follows a **Galaxy Schema**, where multiple business processes are represented through independent fact tables connected via shared dimensions.

Unlike a traditional star schema, this architecture enables enterprise reporting across multiple subject areas while maintaining a single source of truth for common business entities.

### Shared Dimensions

- Customers
- Products
- Geography
- Date
- Campaign
- Order Flags

### Fact Tables

- fact_sales
- fact_inventory
- fact_sales_target
- fact_campaign_spend
- fact_promotion_coverage
- fact_order_process *(Accumulating Snapshot Fact)*

The semantic model supports cross-functional reporting without requiring direct fact-to-fact relationships.

---

# 📊 Dashboard Preview

Although the primary focus of this project is **enterprise data modeling**, a lightweight Power BI report was developed to validate relationships, DAX calculations, filter propagation, and security implementation.

<img src="Docs/Images/05_Dashboard.png" width="100%"/>

The report demonstrates:

- Correct relationship behavior
- Shared dimension filtering
- Reusable DAX measures
- Accurate aggregation across multiple fact tables
- Validation of the semantic model

---

# 📐 Data Modeling Principles

This project follows industry-standard dimensional modeling techniques commonly used in enterprise data warehouses and modern Business Intelligence solutions.

Implemented concepts include:

- ⭐ Star Schema
- 🌌 Galaxy Schema
- 🔗 Shared (Conformed) Dimensions
- 🗂 Junk Dimension
- 📅 Role-Playing Dimensions
- 📊 Factless Fact Tables
- 📦 Accumulating Snapshot Fact Tables
- 📏 Grain Definition
- 🧮 Dedicated Measures Table

Each concept is documented in detail with practical implementation examples.

📖 **Learn more:**

➡️ **[Data Modeling Principles](Docs/Data_Modeling_Principles.md)**

---

# ⚙️ Power Query Organization

To improve maintainability and collaboration, Power Query was organized into logical folders instead of a flat query list.

```
01_Stage
02_Dimensions
03_Facts
04_Support
Other Queries
```

This organization separates raw source tables from transformed analytical tables, making large semantic models significantly easier to maintain.

<img src="Docs/Images/03_Query_Groups.png" width="100%"/>

📖 **Complete documentation:**

➡️ **[Power Query Organization](Docs/Power_Query_Organization.md)**

---

# 📝 Naming Standards

A consistent naming convention improves readability, collaboration, and long-term maintainability across enterprise BI projects.

The project follows conventions such as:

- English naming
- snake_case
- `dim_` prefix for dimensions
- `fact_` prefix for facts
- `_key` suffix for surrogate keys

Following standardized naming makes semantic models easier to understand, maintain, and extend.

📖 **Complete naming standards:**

➡️ **[Naming Standards](Docs/Naming_Standards.md)**

---

# 📦 Measures Table

Rather than scattering measures across multiple tables, all DAX calculations are centralized within a dedicated **Measures** table.

This provides:

- Single source of truth for business calculations
- Improved discoverability
- Consistent KPI definitions
- Easier maintenance
- Cleaner field list for report developers

Examples include:

- Total Orders
- Total Customers
- Active Products
- Total Inventory
- Order-to-Pay Days
- Average Delivery Time
- Inventory Value
- Sales vs Target
- Campaign ROI

<img src="Docs/Images/04_Measures_Table.png" width="100%"/>

📖 **Complete measure documentation:**

➡️ **[Measures Documentation](Docs/Measures.md)**

---

# 🔒 Row-Level Security (RLS)

Role-Level Security was implemented to ensure users only access data relevant to their assigned region.

Example access:

| User | Region |
|------|--------|
| User A | Europe |
| User B | North America |
| User C | Middle East |

This enables secure, scalable reporting without maintaining multiple datasets.

<img src="Docs/Images/06_RLS_Demo.png" width="100%"/>

📖 **Implementation details:**

➡️ **[Row-Level Security](Docs/Row_Level_Security.md)**

---

# 💼 Business Value Delivered

Transforming the transactional database into a semantic model provides several business benefits.

### Performance

- Faster report rendering
- Simplified DAX calculations
- Reduced model complexity

### Scalability

- Easily supports additional fact tables
- Reusable dimensions
- Modular architecture

### Governance

- Consistent business definitions
- Centralized measures
- Standardized naming conventions

### Security

- Row-Level Security implementation
- Secure data access
- Shared semantic model

### Maintainability

- Organized Power Query structure
- Documented modeling standards
- Enterprise-ready design
- Easier onboarding for new developers

The resulting semantic model is suitable for enterprise reporting, self-service BI, and future business expansion.

---

# 🧹 Data Cleaning & Transformation

Extensive data preparation was performed in Power Query to ensure the final semantic model was accurate, consistent, and optimized for analytics.

The transformation process included:

- Removed unnecessary columns to reduce model size
- Standardized data types across all tables
- Created surrogate keys where required
- Eliminated duplicate records
- Merged and reshaped related tables into dimensions
- Built conformed dimensions shared across multiple fact tables
- Created a dedicated Junk Dimension for low-cardinality attributes
- Implemented Role-Playing Date relationships
- Designed an Accumulating Snapshot Fact (`fact_order_process`)
- Organized queries into logical folders for maintainability
- Optimized relationships following Star and Galaxy Schema principles

---

# ✅ Model Validation

Maintaining data integrity was a critical part of the modeling process.

Validation activities included:

- Verified row counts after each transformation
- Compared source totals with transformed totals
- Validated relationship cardinality
- Confirmed filter propagation across dimensions
- Tested DAX measures against expected results
- Validated Row-Level Security behavior
- Ensured every fact table had a clearly defined grain
- Confirmed there were no direct fact-to-fact relationships

This iterative validation process ensured that every transformation preserved business accuracy while improving analytical performance.

---

# 🛠 Skills Demonstrated

This project showcases practical Business Intelligence and data modeling skills commonly required for Power BI Developer, BI Engineer, Analytics Engineer, and Data Analyst roles.

### Business Intelligence

- Power BI
- Power Query
- DAX
- Semantic Modeling
- Data Visualization

### Data Modeling

- Star Schema
- Galaxy Schema
- Dimensional Modeling
- Shared (Conformed) Dimensions
- Junk Dimension
- Role-Playing Dimensions
- Factless Facts
- Accumulating Snapshot Facts
- Grain Definition
- Surrogate Keys

### Data Engineering Concepts

- ETL
- Data Transformation
- Data Validation
- Relationship Modeling
- Query Optimization
- Enterprise Semantic Models

### Governance & Security

- Row-Level Security (RLS)
- Measures Table
- Naming Standards
- Model Documentation

---

# 📚 Key Learnings

This project strengthened my understanding of enterprise semantic modeling and dimensional design beyond dashboard development.

Key takeaways include:

- Designing scalable semantic models for analytics
- Transforming OLTP databases into dimensional models
- Applying Kimball dimensional modeling techniques
- Building reusable shared dimensions
- Modeling multiple business processes using a Galaxy Schema
- Implementing secure reporting with Row-Level Security
- Organizing large Power Query projects for maintainability
- Centralizing business logic through a dedicated Measures table
- Validating data integrity throughout the transformation lifecycle

---

# 🚀 Future Improvements

Potential enhancements for this project include:

- Incremental Refresh implementation
- Calculation Groups using Tabular Editor
- Metadata documentation using Bravo for Power BI
- Deployment Pipelines
- Automated refresh through Power BI Service
- Source control integration using Fabric Git
- Performance optimization using DAX Studio
- Best Practice Analyzer (BPA) validation
- CI/CD workflow for semantic model deployment

---

## 🌟 About Me

Hi there! I'm **Kaustubh Sutar**, a data enthusiast and aspiring **Data Analyst & Data Engineer** skilled in **Power BI, SQL, Python, Excel, PySpark, and Databricks**. I enjoy building scalable data pipelines, designing enterprise semantic models, and creating analytics solutions that transform raw data into meaningful business insights.

I also have growing interests in **Data Engineering, Machine Learning, and AI**, continuously exploring modern technologies to expand my analytical and engineering capabilities.

Let's stay connected!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kaustubh-sutar-814134340/)

---

## ⭐ Support This Project

If you found this project insightful:

- ⭐ Star the repository
- 🍴 Fork the project
- 📢 Share it with others
- 💼 Connect for analytics collaborations

---

## 🛡️ License

This project is licensed under the **MIT License**.

You are free to use, modify, and share this project with proper attribution.

---
