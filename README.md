Suspend Or Pause Azure SQL Data Warehouse
=========================================

            
Suspend / Pause Azure SQL Data Warehouse

This is a simple runbook that will allow you to see if there are queries currently running on your Azure SQL Data Warehouse before you Suspend/Pause the service.

Why you want to see if Queries are Running

It is common that a team will work on and be access data from an Azure SQL Data Warehouse. What commonly happens is one or more sessions will be loaing or quering data from the warehouse which is causing data movment. While these operations are happening,
 someone else will pause the serivce from the portal or call Suspend-AzureRmSqlDatabase aginst the service. At this point, all running actions will be canceled. Those data movement operations that were happening need to be rolled back to ensure data consistancy.
 Rollback operations can take hours depending on what was happening. The service will keep running and incuring compute use while the rollback is running.


Calling this runbook to Suspend or Pause the Azure SQL Data Warehouse service help to try and prevent this rollback from happening. Also, many times if you do have long running operation happening and pause the service, that work that was running is now
 lost and will have to be retried at a later time.


This is designed to be used from an Azure Automation Account, but can be altered to be ran from other locations.


 




 




        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
