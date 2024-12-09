Automatic Lineage Extraction from MS Fabric

This is an Initial code implementation for automatic metadata and lineage extraction from MS Fabric.

The code extracts metadata of tables, table columns, PBIR reports and pipeline Copy activity mappings from MS Fabric.
It then uploads all metadata found to MS Purview and creates a graphical attribute-level lineage.

The first screenshot shows column-level lineage display of Copy DataPipelines

<img width="797" alt="image" src="https://github.com/user-attachments/assets/6169652b-24ed-4fd0-ade9-16a3a3f2501c">

this is obtained automatically without human intervention, apart from configuration of the code.

The second screenshot shows colum-level lineage display of Fabric/PowerBI reports in PBIR format, extracted using SemPY library.

<img width="804" alt="2024-12-09_ReportLineage" src="https://github.com/user-attachments/assets/3087e579-6bbf-43ba-b869-8a38dfab7fdb">

The lineage information is also formatted in the form of DataFrames, thus allowing easy reuse, for example for regulatory purposes (legal reporting on data analysis) and impact analysis ("what business data is impacted if I change one step of the data transformation process?").

