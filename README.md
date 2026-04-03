# RetailOrders SSAS Cube

A comprehensive SQL Server Analysis Services (SSAS) cube for analyzing retail order data with multi-dimensional analysis capabilities.

## Overview

RetailOrders_SSAS_Cube is a business intelligence solution built with SQL Server Analysis Services that provides dimensional analysis of retail order transactions. This cube enables complex analytical queries and reporting on retail orders across multiple dimensions including customers, products, suppliers, and time.

## Project Structure

```
├── Retailorders_Cube.sln          # Visual Studio solution file
├── Retailorders_Cube.dwproj       # Data Warehouse project
├── Retailorders_Cube.database     # SSAS database configuration
├── RetailOrders_Cube.cube         # Main cube definition
├── RetailOrders_Cube.partitions   # Cube partitions for performance
├── Retail Orders DW.ds            # Data source definitions
├── Retail Orders DW.dsv           # Data source view
├── Dim Customer.dim               # Customer dimension
├── Dim Date 1.dim                 # Date dimension (primary)
├── Dim Date.dim                   # Date dimension (reference)
├── Dim Product.dim                # Product dimension
└── Dim Supplier.dim               # Supplier dimension
```

## Components

### Dimensions

- **Dim Customer** - Customer information and attributes
- **Dim Date** - Time-based dimensional analysis with temporal hierarchy
- **Dim Product** - Product catalog and categorization
- **Dim Supplier** - Supplier master data

### Cube

- **RetailOrders_Cube** - Main analytical cube combining all dimensions with retail order facts

### Data Source

- **Retail Orders DW** - Data warehouse connection and source view definitions

## Requirements

- SQL Server Analysis Services (SSAS) 2019 or later
- SQL Server Data Tools (SSDT) for Visual Studio
- Underlying data warehouse with populated dimension and fact tables

## Getting Started

1. **Open the Solution**
   - Open `Retailorders_Cube.sln` in Visual Studio with SQL Server Data Tools

2. **Configure Data Source**
   - Update the connection string in `Retail Orders DW.ds` to point to your data warehouse

3. **Deploy the Cube**
   - Build the solution
   - Deploy to your SSAS instance

4. **Process the Cube**
   - Process dimensions in order: Customer, Date, Product, Supplier
   - Process the cube

## Cube Analysis

Once deployed, the cube supports analysis across:

- **Customer Dimension** - Analyze orders by customer segments
- **Time Dimension** - Temporal analysis with year, quarter, month hierarchies
- **Product Dimension** - Product performance and category analysis
- **Supplier Dimension** - Supplier performance metrics

## Performance Optimization

The cube includes partition configuration (`RetailOrders_Cube.partitions`) to optimize query performance on large datasets.

## Development

This project uses:
- Visual Studio with SQL Server Data Tools
- SSAS Multidimensional model
- T-SQL for underlying data warehouse

## Notes

- The solution includes `.gitattributes` and `.gitignore` for proper version control of binary SSAS files
- Multiple date dimensions are included to support different temporal analysis scenarios

## License

Please refer to the project license for usage rights.

## Author

Deeghau0816