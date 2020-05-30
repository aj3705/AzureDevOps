# Create Azure DevOps work item using Azure DevOps REST APIs.  

**Prerequisite:** If you have not already done so, please follow the steps in [Getting access token for DevOps REST APIs][1] to get the access token for DevOps REST APIs . 

In this tutorial, you will:
- [Configure a custom process for your Azure DevOps project, and add a custom field to Azure Boards work item.](#u1)
- [Using the access token obtained in the previous tutorial, you will create a work item in Azure Boards by invoking Azure DevOps REST API](#u2)


## <a name="u1"> Add custom field(s) to your Azure Boards work items  
  
## <a name="u2"> Create work item using Azure DevOps REST API
  
  You will use Postman to invoke Azure DevOPs REST APIs. If you do not already have it, you can download it from [here][1].
  
  ### Steps  
  
  1. Open your Postman App and create a new http request by clicking on the **+** sign. 
  2. Select POST from drop down as the Request type
  3. Click on authorization and select Bearer Token from the TYPE drop down.  
     
     ![select bearer token](./images/select-bearer-token.png)  
  4. Copy paste the Azure DevOps access token that you obtained in the [tutorial][2] on how to get access token.  
      
     ![select bearer token](./images/bearer-token-entry.PNG)  
     
  5. Populate the url field as follows:
     
     ```
     https://dev.azure.com/{organization}/{project}/_apis/wit/workitems/$issue?api-version=5.1
     
     ```
  6. Populate the request body with the following JSON for creating work item in Azure DevOps Boards. Notice that 
  
     ```
      [
        {
          "op": "add",
          "path": "/fields/System.Title",
          "from": null,
          "value": "SampleWorkItem"
        },
        {
          "op": "add",
          "path": "/fields/System.Description",
          "from": null,
          "value": "This is a sample workitem created using Azure DevOps REST APIs"
        },
        {
          "op": "add",
          "path": "/fields/Activity",
          "from": null,
          "value": "Development"
        },
         {
          "op": "add",
          "path": "/fields/application",
          "from": null,
          "value": "This is a custom field"
        }
      ]
     ```
     
      ![request body](./images/req-body.PNG) 








[1]:https://www.postman.com/downloads/
[2]:https://github.com/aj3705/AzureDevOps/blob/master/restapis/ado-authentication.md











[1]:https://github.com/aj3705/AzureDevOps/blob/master/restapis/ado-authentication.md
