# Azure-Data-Pipeline
Project Flow:

Raw Data source ----> Data ingestion in Data Factory ----> Raw Data Store (Azure Data Lake gen2) ---> Tranformed the data (Azure databricks) ----> Dashboard (Tableau)

1.	Created a Storage account with a new Resource group, check the hierarchical namespace box, so that the files in the storage account will be available in a hierarchical format just like how it is in the disk storage(folder structure)

  ![image](https://github.com/snehamathur01/Azure-Data-Pipeline/assets/51332122/4c2b5252-470b-4fe6-9ce1-973154ce4075)

 
2.	Created a new container inside the resource group, a container is nothing but a place where data is stored as an object
   ![image](https://github.com/snehamathur01/Azure-Data-Pipeline/assets/51332122/eb0c6b30-b834-4686-81a0-0a5a4ff15148)
The container has 2 directories raw data and transformed data

 ![image](https://github.com/snehamathur01/Azure-Data-Pipeline/assets/51332122/f0fb3e1a-63af-4ebb-a3dd-8573b4bf9375)

 3.	Created a Data Factory for the current resource group for copying the data from github to Azure Data Lake Gen2
    For Atheletes.csv - Defined the source(HTTP) and Sink(ADLS)

    ![image](https://github.com/snehamathur01/Azure-Data-Pipeline/assets/51332122/3bb7e3f0-8191-40e3-877d-ec7048c0fc71)

    
Repeated the same for Coaches.csv, EntriesGender.csv, Medals.csv, Teams.csv
![image](https://github.com/snehamathur01/Azure-Data-Pipeline/assets/51332122/d5ae715c-008a-43aa-ab83-cbe64bab2e76)
![image](https://github.com/snehamathur01/Azure-Data-Pipeline/assets/51332122/a915b28e-8229-4424-9ae8-3dfe31aabb27)

Now we have all the 5 files in the Raw Folder of our container,
![image](https://github.com/snehamathur01/Azure-Data-Pipeline/assets/51332122/9e018a42-8a5d-4bab-b070-6ef4c83a0192)

4. Then I created a databricks workspace and wrote transformation logic for the all 5 files. (The databricks notebook has been uploaded)
   
5. From the cleaned file I created a dashboard to extract valuable insights from the Olympics data





