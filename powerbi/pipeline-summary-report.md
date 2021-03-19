# Create Azure DevOps Pipeline summary report for all pipelines using Power BI

Currently Azure DevOps pipeline [reports][1]. As described in the [documentation][2], Azure DevOps supports multiple authentication mechanisms to authenticate to Azure DevOps REST APIs. This tutorial show how to create a work item in Azure DevOps Boards via REST API calls using OAuth 2.0 authentication. The following diagram from [Azure DevOps documentation][3] dipicts the OAuth flow for getting an access token and invoking Azure DevOps REST APIs.

  ![oauth flow](./images/oauth-flow.png)
  
In this tutorial you will learn how to:  

  [Get OAuth access token using a sample ASP .NET web application][1]  
  [Use the access token to create a work item in Azure Boards by calling Azure DevOps REST APIs][4]

  
When you are finished, you would have successully created a work item in Azure DevOps boards with data in system and custom fields, by invoking Azure DevOps Rest APIs. Let's [dive in][1].


  

  
[1]:https://docs.microsoft.com/en-us/azure/devops/pipelines/reports/pipelinereport?view=azure-devops
[2]: https://docs.microsoft.com/en-us/azure/devops/report/powerbi/sample-pipelines-allpipelines?view=azure-devops&tabs=powerbi



