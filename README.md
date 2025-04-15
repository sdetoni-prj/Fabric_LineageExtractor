# Automatic Lineage Extraction from MS Fabric

This is an Initial code implementation for automatic metadata and lineage extraction from MS Fabric.

**Please use the [Releases](https://github.com/sdetoni-prj/Fabric_LineageExtractor/releases) section link for dowloading the notebook source code (on the right side of this page)**
 
The code extracts metadata of tables, table columns, PBIR reports and pipeline Copy activity mappings from MS Fabric.
It then uploads all metadata found to MS Purview and creates a graphical attribute-level lineage.

The first screenshot shows column-level lineage display of Copy DataPipelines

<img width="797" alt="image" src="https://github.com/user-attachments/assets/6169652b-24ed-4fd0-ade9-16a3a3f2501c">

this is obtained automatically without human intervention, apart from quick configuration of the code (namely the SVC Principal auth details).

The second screenshot shows colum-level lineage display of Fabric/PowerBI reports in PBIR format, extracted using SemPY library.

<img width="804" alt="2024-12-09_ReportLineage" src="https://github.com/user-attachments/assets/3087e579-6bbf-43ba-b869-8a38dfab7fdb">

The lineage information is also formatted in the form of DataFrames, thus allowing easy reuse, for example for regulatory purposes (legal reporting on data analysis) and impact analysis ("what business data is impacted if I change one step of the data transformation process?").



Credits:

version 1: 

The Table and Colums metadata are extracted via SQL queries whose source can be found in the MS documentation [here](https://learn.microsoft.com/en-us/sql/relational-databases/system-catalog-views/querying-the-sql-server-system-catalog-faq?view=fabric#_FAQ31) 

Report sources metadata Pipeline json structures are extracted using Semantic Link Labs library by Michael Kovalsky et al. (https://github.com/microsoft/semantic-link-labs)

Upload to MS Purview is performed using examples of Pyapacheatlas by Will Johnson et al. (https://github.com/wjohnson/pyapacheatlas)
