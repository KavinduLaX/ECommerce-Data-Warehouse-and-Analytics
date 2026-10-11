# E-Commerce Data Warehouse & Business Intelligence

An end-to-end Data Warehousing and Business Intelligence solution that transforms e-commerce operational data into a dimensional data warehouse, an OLAP cube, and analytical reports.

## Project Overview

This academic project demonstrates a data pipeline from source-file ingestion to dimensional modelling, multidimensional analysis, and business reporting. It combines Microsoft SQL Server data warehousing technologies with Excel and Power BI analytics.

## Architecture

```text
CSV and TXT Source Files
          |
          v
    Staging Database
          |
          v
     SSIS ETL Packages
          |
          v
 SQL Server Data Warehouse
       (Star Schema)
          |
          v
 SSAS Multidimensional Cube
          |
          +------------------+
          |                  |
          v                  v
   Excel OLAP Analysis   Power BI Reports
```

## Key Features

### Data Integration and ETL
- Ingestion of e-commerce data from CSV and TXT source files.
- Staging and transformation using SQL Server Integration Services (SSIS).
- ETL workflows for staging, dimension loading, fact loading, and transaction lifecycle updates.
- Data type conversion, data cleansing, and derived-field processing.

### Dimensional Data Warehouse
- Star-schema-based analytical modelling.
- `FactSales` measures including quantity, item price, and item total.
- Customer, product, and date dimensions.
- Slowly Changing Dimension (SCD) Type 2 to maintain customer history.
- Accumulating snapshot modelling for transaction progress and processing duration.

### OLAP and Business Intelligence
- Multidimensional cube developed with SQL Server Analysis Services (SSAS).
- Customer, product, and date dimensions.
- Excel PivotTable analysis connected to the OLAP cube.
- Power BI analysis supporting interactive filtering, comparisons, drill-down, and drill-through.

## Technologies Used

- Microsoft SQL Server
- SQL Server Integration Services (SSIS)
- SQL Server Analysis Services (SSAS)
- SQL Server Management Studio (SSMS)
- Microsoft Excel
- Power BI Desktop
- Visual Studio / SQL Server Data Tools (SSDT)

## Repository Structure

```text
ECommerce-Data-Warehouse-BI/
├── CubeProject/       # SSAS cube and dimensional model files
├── ECommerce/         # SSIS project files (some temporarily excluded)
├── ExcelReport/       # Excel OLAP workbook (temporarily excluded)
├── PowerBIReports/    # Power BI report (temporarily excluded)
├── DataWarehouse/     # Database backup (excluded from Git)
├── .gitignore
└── README.md
```

## Setup Notes

This project requires a compatible Windows environment with the relevant SQL Server components and development tools installed.

1. Configure SQL Server and the required database connections.
2. Prepare the required source CSV and TXT files.
3. Configure and run the SSIS packages in the appropriate order.
4. Deploy the data warehouse and SSAS cube using the relevant SQL Server tools.
5. Connect Excel and Power BI to the configured analytical data source.

The original project contains environment-specific connection settings. These must be reviewed and configured before running the solution on another machine. This repository does not promise a one-click deployment.

## Concepts Demonstrated

- ETL pipeline development
- Data warehouse architecture
- Star schema and dimensional modelling
- Fact and dimension tables
- Slowly Changing Dimensions (Type 2)
- Accumulating snapshot fact modelling
- OLAP cube development
- Roll-up and drill-down
- Slice, dice, and pivot
- Interactive business intelligence reporting

## Data and Configuration

Database backups, generated build artifacts, local IDE settings, and environment-specific configuration are excluded or reviewed separately before publication. Never commit credentials, private datasets, or personal information.

## Project Context

Developed as an academic Data Warehousing and Business Intelligence project. The repository documents the solution architecture, technical implementation, and analytical capabilities.

## Publication Note

Some original project files, including SSIS packages, local connection configurations, the Excel OLAP workbook, and the Power BI report, are temporarily excluded while their portability and publication safety are reviewed. Not every original project artifact is included in this initial repository version.