# Install SQL Server
  - Follow the [doc](https://github.com/rritec/powerbi/blob/master/Notebooks/PBI_01_01_Introduction_Installation.md#msft-sql-server-installation) and install SQL Serer database
  - Install SSMS [doc](https://github.com/rritec/powerbi/blob/master/Notebooks/PBI_01_01_Introduction_Installation.md#instal-sql-server-management-studio-ssms)
  - enable `sa` user by following [doc](https://www.top-password.com/knowledge/unlock-sql-server-sa-account.html)
  - provide password and remember it.

# Self Hosted IR
  - Perform data flows, data movement and dispatch activities to **external compute**
  - In **ADF** > Clcik on **Manage** > Under **Connections** > Click on **Integration Runtimes**
  - Click on **New**
  - Click on **Azure, Self-Hosted**
  - Click on **Self-Hosted**
  - Name it as **Self-Hosted-IR**
  - Click on **Create**
  - Click on **Express Setup** and install the software
  - Create a linked service using self-hsted IR

    ![image](https://github.com/rritec/Cloud-Data-Engineering/assets/20516321/6f237696-b51d-4463-be3e-457903482663)

  - create a dataset using above linked service

# Create Pipenine from Blob to MS Sql Server
  - Click on **Author**
  - Right click on **rritec_pipelines** folder > Click on **New Pipeline** > Name it as **p03_from Blob to MS Sql Server**
  - Under **Activities** > Expand **Move & Transform** > Drag and drop **Copy Data** activity
  - Under **General** tab > name it as **Copy_from_blob_to_MS_SQL_Server**
  - Click on **Source** tab > Select **Source Dataset** as **src_emp**
  - Click on **Sink** tab > Select **Sink dataset** as **tgt_sql_server_emp**
  - Click on **Debug**
  - Under **Output** > observe **Details**
  - ![image](https://user-images.githubusercontent.com/20516321/209775129-191c309d-ccce-4c27-9c82-6aad1e5228fa.png)
# Home Work
1. Create pipeline to copy data from Sql server to BLOB
2. Create pipeline to copy data from Sql server to Sql Server

# Questions
1. When we are trying to connect SQL server from the ADF, it is giving me the below error message :
Cannot connect to SQL Database. Please contact SQL server team for further support. Server: 'JEEVAN-SRIKANTH', Database: 'B2401DB', User: 'sa'. Check the linked service configuration is correct, and make sure the SQL Database firewall allows the integration runtime to access.
Login failed for user 'sa'., SqlErrorNumber=18456,Class=14,State=1,

What can I do for this Sir ? Where can I check the SQL firewall settings 
# Answers
1. 
