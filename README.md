# Mini go! Fresh-Fruit Cold-Chain Optimization Dataset

This package is a complete prototype input dataset for the multi-objective cold-chain distribution network model.

## Dataset structure
01_Assumptions.csv
02_Supplier_Data.csv
03_Store_Data.csv
04_DC_Data.csv
05_Vehicle_Data.csv
06_Product_Freshness.csv
07_Cost_Emission_Parameters.csv
08_Historical_Supplier_Store_Flow.csv
09_Node_Master.csv
10_Network_Arc_Data.csv
11_Model_Config.csv
12_Algorithm_Settings.csv
13_Data_Dictionary.csv
14_Dataset_Summary.csv

## Data scope
- Product category: Fresh Fruit, aggregated for optimization.
- Stores: 10 selected Mini go! stores.
- Suppliers: 12 selected suppliers, including 6 direct-capable suppliers.
- Existing DC: DC901 (Sojitz Kokubu, Duc Hoa).
- Candidate DCs: 3 planning locations.
- Fleet: 8 refrigerated vehicles.
- Historical study period: 20 June 2026 to 20 August 2026.
- Planning horizon: one week.

## Quantity convention
The source files do not provide a reliable common kilogram conversion for every fruit SKU.
For the prototype, quantities are therefore normalized as kg-equivalent units.
The parameter KgEq_per_Historical_Unit is initially set to 1.00 and can be replaced when confirmed product-weight data become available.

## Data status
Observed:
- supplier identities
- historical order/reception quantities
- historical store coverage
- historical direct/via-DC quantities

Derived:
- average weekly demand
- average weekly supplier volumes
- historical channel shares
- geodesic/road-distance and travel-time proxies

Planning inputs:
- supplier capacities
- candidate DC capacities and costs
- vehicle/fuel parameters
- freshness parameters
- emissions factor
- algorithm settings
- planning coordinates where exact operational coordinates are unavailable

The package is designed so these planning inputs can be replaced later without changing the dataset structure.
