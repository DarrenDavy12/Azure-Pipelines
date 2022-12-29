# (Azure) CI/CD Classic Pipelines

1. Deploy python app on Azure Web App:

In the Azure DevOPs site, I create a new project and pipeline, classic editor and then click on Azure repo Git and in down in the repository drop down menu below select the python project from my GitHub. 

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled.png)

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%201.png)

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%202.png)

1. On the next page I click empty job just below the ‘Select a template’ title. 

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%203.png)

1. Then for the first job, I will add Azure CLI, to run some azure commands. Bring up the resource group. 

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%204.png)

1. Connection was already created and next I want a batch script type along with Inline script. 

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%205.png)

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%206.png)

1. After that, I add another job with again Azure CLI for my Plan, with the same config as the the resource group job, with a different command for the inline script. 

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%207.png)

1. For the last job is for the web app using Azure CLI again, same config as the other two jobs before but a different command for the inline script. 

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%208.png)

1. Give it a name at the top of the page, and then I click Save and Queue, choose the specific agent specs and once done I click Save and Run. Now it will trigger the pipeline and see if there’re any errors.

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%209.png)

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%2010.png)

![Untitled]((Azure)%20CI%20CD%20Classic%20Pipelines%20ee46ad1cdab045928e6062e17235f5d8/Untitled%2011.png)

Back on Microsoft Azure, under resource groups I refresh the table and the new app service has been created.