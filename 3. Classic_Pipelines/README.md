# (Azure) CI/CD Classic Pipelines

1. Deploy python app on Azure Web App:

In the Azure DevOPs site, I create a new project and pipeline, classic editor and then click on Azure repo Git and in down in the repository drop down menu below select the python project from my GitHub. 

![Untitled](https://user-images.githubusercontent.com/42151912/209972717-ef97e639-651e-43d1-867b-50299a0bbef5.png)

![Untitled 1](https://user-images.githubusercontent.com/42151912/209972789-05565323-18a4-4c0a-975e-1d1b4d7bb507.png)

![Untitled 2](https://user-images.githubusercontent.com/42151912/209972852-558997bf-6623-4603-8c84-b109bad0cbd0.png)


2. On the next page I click empty job just below the ‘Select a template’ title. 

![Untitled 3](https://user-images.githubusercontent.com/42151912/209972927-ec5fa765-6a7c-4a53-8486-25ae4102bc73.png)


3. Then for the first job, I will add Azure CLI, to run some azure commands. Bring up the resource group. 

![Untitled 4](https://user-images.githubusercontent.com/42151912/209973030-940fc857-a738-45b7-bf56-01dc4ab2f31f.png)


4. Connection was already created and next I want a batch script type along with Inline script. 

![Untitled 5](https://user-images.githubusercontent.com/42151912/209973065-e5992e2a-6e3f-40e6-ab38-6cccb8478fae.png)


5. After that, I add another job with again Azure CLI for my Plan, with the same config as the the resource group job, with a different command for the inline script. 

![Untitled 6](https://user-images.githubusercontent.com/42151912/209973200-39ef2583-7413-4545-9c9f-c81a84b11528.png)

![Untitled 7](https://user-images.githubusercontent.com/42151912/209973253-a0694f5a-602b-45c6-b732-91f63fafe965.png)


6. For the last job is for the web app using Azure CLI again, same config as the other two jobs before but a different command for the inline script. 

![Untitled 8](https://user-images.githubusercontent.com/42151912/209973358-8ff4c821-8d8d-4bb0-8a72-63f798fb498a.png)


7. Give it a name at the top of the page, and then I click Save and Queue, choose the specific agent specs and once done I click Save and Run. Now it will trigger the pipeline and see if there’re any errors.

![Untitled 9](https://user-images.githubusercontent.com/42151912/209973399-5a276ce5-204c-4edf-8bc2-b7a597087a8c.png)

![Untitled 10](https://user-images.githubusercontent.com/42151912/209973431-534aa77f-19b0-413b-a572-3c7f55af7bfe.png)

![Untitled 11](https://user-images.githubusercontent.com/42151912/209973759-df210c52-b730-4084-918e-9b3c8ae6c09f.png)


Back on Microsoft Azure, under resource groups I refresh the table and the new app service has been created.
