# Programmer-Take-Home-Evaluation-Advanced
This document will list the steps a candidate for the Programming Team Lead position will perform to evaluate skill level, proficiency, and ability to deliver a solution meeting the requirements in a timely manner.

## Requirements
- Microsoft SQL Server 2022 Express Edition (or later)
- Visual Studio 2022 or Visual Studio Code

## Setup
- Download and unzip GOLF_WAREHOUSE.7z
- Attach the GOLF_WAREHOUSE.mdf file to the SQL server instance on your machine

## Task
- Task #1:
	- Create a .NET Core Web API (MVC or Micro API) that takes a JSON payload with fields that are required to build a Point-of-Sale transaction. Keep in mind that not all fields should be passed in the payload but calculated and/or obtained from related tables in the database.
- Task #2:
	- Create a trigger on PS_DOC_LIN that evaluates the minimum quantity by location (IM_INV.MIN_QTY) vs the quantity sold (PS_DOC_LIN.QTY_SOLD) and generates a record in a custom table called USER_SUGGESTED_REPLINESHMENT that suggest the quantity that should be ordered from the vendor when a record is inserted, updated or deleted in PS_DOC_LIN.
		- Note: **Columns are not given but should be generated **
- Task #3:
	- Place the results in a Repository on your GitHub account along with a ReadMe containing your full name and which method or job site you used to reach this repository. Send an invitation to your repository to Rapid POS at `recruiting.programmer@rapidpos.com`

## Notes
- Table descriptions
	- AR_CUST – Customers
	- AR_SHIP_ADRS – Customers shipping address
	- IM_ITEM – Item/Products
	- IM_BARCOD – Item barcodes
	- IM_LOC – Item stocking locations
	- IM_INV – Item stocking location values
	- IM_INV_CELL – Item stocking locations grid dimension values
	- IM_SER – Item serial numbers
	- IM_PRC – Item prices by location and grid dimensions
	- IM_CATEG_COD – Item category
	- IM_SUBCATEG_COD – Item subcategory
	- PS_DISC_COD – Point of sale discount definitions
	- PS_DOC_HDR – Point of sale header
	- PS_DOC_HDR_MISC_CHRG – Point of sale miscellaneous charges
	- PS_DOC_HDR_DOC_STAT – Point of sale header status
	- PS_DOC_AUDIT_LOG – Point of sale transaction audit log
	- PS_DOC_CONTACT – Point of sale billing and shipping contacts
	- PS_DOC_LIN – Point of sale line items
	- PS_DOC_PMT – Point of sale payments
	- PS_DRW – Point of sale cash drawer definitions
	- PS_DRW_SESSION – Point of sale cash drawer session
	- PS_STA – Point of sale station definitions
	- PS_STR – Point of sale store definitions

- The following will be taken into consideration for evaluation.
	- Completeness
	- Complexity (Discount applied, Price override, usage of Serialized, Grid dimension (DIM), etc.)
	- Code Design
	- Logging
	- Error Handling
	- Multi-threading
	- Database Interaction
	- Usage of stored procedures, triggers, indexes, etc.
	- Naming Structure
	- Data Validation
	- Code Commenting
	- Performance
	- Object Oriented Concepts used

