# Fintech Data Migration Project

### Introduction
The purpose of this Project is to migrate the data from SQL database in azure to Azure Data lake storage. By the medium of this excersice we will be able to store data in raw files which can be accessible by multiple data sources

### Tech Stack
1. Azure SQL database
2. Azure Synapse
3. Logic apps

### Block Diagram

### Data Flow
- The data is present in a SQL database in form of multiple tables as mentioned below
  - Customers
  - Account
  - Loans
  - Payment
  - Transaction
- Synapse Pipeline
  - We need to create a generic code to pick all the files data automatically and load the data to ADLS.
    - For this purpose we use the lookup transformation which will extract the metadata of the tables and pull the data
  - The ForEach transformation is used to load the data for each of the table
  - We have implemented Pyspark to load the data from Bronze to silver and then from Silver to gold layers
  - Post that by the use of Logic App we etablish a notification email for success and failure 

#### Azure data lake storage
![image](https://github.com/user-attachments/assets/cf401bc4-6d70-45e9-a41e-b837d528df1b)  

![image](https://github.com/user-attachments/assets/d5db8c0f-6c96-457a-9f49-226ccfb57b74)

### Synapse Pipeline
![image](https://github.com/user-attachments/assets/c1ada86c-88d7-456e-82f2-4896176f4ad9)


### SQL Database
![image](https://github.com/user-attachments/assets/3cdeab79-c234-4044-b3b6-6cb40281e303)





