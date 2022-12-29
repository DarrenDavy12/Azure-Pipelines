# (Azure) CI/CD Classic Pipelines

1. Deploy python app on Azure Web App:

In the Azure DevOPs site, I create a new project and pipeline, classic editor and then click on Azure repo Git and in down in the repository drop down menu below select the python project from my GitHub. 

![Untitled](https://user-images.githubusercontent.com/42151912/209976750-450989f7-c7a9-4df4-a124-cfbcb7594383.png)

![Untitled 1](https://user-images.githubusercontent.com/42151912/209976772-331d24d3-ca90-4f2b-a430-046518b48ae1.png)

![Untitled 2](https://user-images.githubusercontent.com/42151912/209976794-ddd8f634-ccb3-4a2a-bfa8-51ad54c2d270.png)


2. On the next page I click empty job just below the ‘Select a template’ title. 

![Untitled 3](https://user-images.githubusercontent.com/42151912/209976846-8cc69f87-ce45-4261-84d5-4519315a9290.png)


3. Then for the first job, I will add Azure CLI, to run some azure commands. Bring up the resource group. 

![Untitled 4](https://user-images.githubusercontent.com/42151912/209976903-8e7690ec-5502-46ec-89cb-f5c1c21727d2.png)


4. Connection was already created and next I want a batch script type along with Inline script. 

![Untitled 5](https://user-images.githubusercontent.com/42151912/209976926-1238b325-9f46-422f-ae78-c84466b0ff8d.png)

![Untitled 6](https://user-images.githubusercontent.com/42151912/209976955-3c41029e-ee9b-49a5-8dc3-81c7c79754d0.png)


5. After that, I add another job with again Azure CLI for my Plan, with the same config as the the resource group job, with a different command for the inline script. 

![Untitled 7](https://user-images.githubusercontent.com/42151912/209976981-388febf0-3748-4f64-94d6-f7c666911037.png)


6. For the last job is for the web app using Azure CLI again, same config as the other two jobs before but a different command for the inline script. 

![Untitled 8](https://user-images.githubusercontent.com/42151912/209976999-3c94fbc9-ddd6-4487-ab04-23f35f8ce4cb.png)


7. Give it a name at the top of the page, and then I click Save and Queue, choose the specific agent specs and once done I click Save and Run. Now it will trigger the pipeline and see if there’re any errors.

![Untitled 9](https://user-images.githubusercontent.com/42151912/209977021-7f0bd086-99ab-4772-884c-4c97cf6518c1.png)

![Untitled 10](https://user-images.githubusercontent.com/42151912/209977044-9e8ef9f6-d2aa-4860-bd0d-42acf8390e45.png)

![Untitled 11](https://user-images.githubusercontent.com/42151912/209977069-534b4dd4-9eb6-40c4-ad08-79bf10db9b86.png)


Back on Microsoft Azure, under resource groups I refresh the table and the new app service has been created.
