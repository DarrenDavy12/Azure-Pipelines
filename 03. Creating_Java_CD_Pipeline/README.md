# (Azure) Creating Java CD pipeline:

To create a CD pipeline, I head over to Azure DevOps website and go to `pipelines` → `releases` and open in a new tab, create a new release pipeline → 

![Untitled](https://user-images.githubusercontent.com/42151912/209974361-38907855-fcc2-47b3-aa5d-2f0f3b923aa1.png)


I choose Azure App service deployment and hit apply → 

![Untitled 1](https://user-images.githubusercontent.com/42151912/209974386-cea4cbfe-14fd-4afd-bb79-93c9af597483.png)

Give the stage name `production` →  

![Untitled 2](https://user-images.githubusercontent.com/42151912/209974516-66b8c550-302d-4f75-b326-ea7d3afe7c00.png)


For the workflow I will start getting the artifact that will be deployed inside the production environment, with the artifact being the .jar file already generated during the CI pipeline, so I select the artifact → 

In this case we are going to stick with the build source type for this CD pipeline. 

Then I select my CI pipeline for the (build pipeline) underneath. 

After that hit Add.

![Untitled 3](https://user-images.githubusercontent.com/42151912/209974587-26077950-42eb-4374-9815-56f13326381e.png)

![Untitled 4](https://user-images.githubusercontent.com/42151912/209974618-0945cd02-bffd-48f1-a577-968806d8febd.png)


Now I will click on production, because I want to deploy into Azure App service, I need to connect Azure DevOps into my Azure subscription, once selected, it will ask me for email and password of my Azure account then hit Authorize → 

![Untitled 5](https://user-images.githubusercontent.com/42151912/209974730-e713f89c-0d59-4acf-b41f-85efdae09b54.png)

![Untitled 6](https://user-images.githubusercontent.com/42151912/209974767-f3839d58-5290-462f-8639-f7277a09c6a5.png)


After that I select web app on Linux → 

![Untitled 7](https://user-images.githubusercontent.com/42151912/209974817-d4b91e4b-a6d5-4f55-99cf-a7a1fe7cd102.png)

![Untitled 8](https://user-images.githubusercontent.com/42151912/209974841-1b2702c2-2e02-4308-af2b-5cd4887d40f5.png)


App service name as our resource → 

![Untitled 9](https://user-images.githubusercontent.com/42151912/209974860-d5232101-14eb-475a-9e34-7bc5d0f3c6d3.png)


Now I click on Run on agent and pick whatever pool , at this point all of the pools have Azure CLI → 

![Untitled 10](https://user-images.githubusercontent.com/42151912/209974903-e2b15dc1-ae15-488f-becd-4a32e7282d63.png)


If I head back to the Deploy Azure App service, the package I need to browse and select my .jar file → 

![Untitled 11](https://user-images.githubusercontent.com/42151912/209974939-470c24c5-51a1-434e-a76d-c8299b748733.png)

![Untitled 12](https://user-images.githubusercontent.com/42151912/209974961-1b0eda54-a543-4dde-81a2-25f59d15d65b.png)


I pick Tomcat 9.0 on Deploy Azure App Service and head over to Production → startup command as `java -jar /home/site/wwwroot/gs-spring-boot-0.1.0.jar --server.port=80`

![Untitled 13](https://user-images.githubusercontent.com/42151912/209975072-8758fb0a-1aa6-40ab-b18d-25f0b9079c1b.png)

![Untitled 14](https://user-images.githubusercontent.com/42151912/209975098-68015990-b201-4d8f-9968-c99dc24f2bdf.png)


Then save release above → 

![Untitled 15](https://user-images.githubusercontent.com/42151912/209975155-8bf2100b-eff0-4e46-9d03-2058c61166f0.png)

