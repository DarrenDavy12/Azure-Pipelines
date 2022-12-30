# Create YAML pipeline in Azure DevOps:


First I logged into my Azure DevOps account and made a new project called “Test” 

![Untitled](https://user-images.githubusercontent.com/42151912/210068113-38e114b2-ce6b-450d-8408-fe837d0e9ef0.png)



Then headed to pipelines → pipelines and created a new pipeline 

![Untitled 1](https://user-images.githubusercontent.com/42151912/210068132-77d0e0bf-7d33-4aa2-b4a0-9daaf7782b15.png)



Once on the next page, I went to repos → File → new repository and gave a name then I clicked create including a ReadMe file. 

![Untitled 2](https://user-images.githubusercontent.com/42151912/210068181-ab3dc15c-b9d4-4259-a297-423d47725951.png)

![Untitled 3](https://user-images.githubusercontent.com/42151912/210068240-3fdb5128-dc34-4246-9e2f-6ef52b5aa0a4.png)



Then I go back to pipeline, create a pipeline and I clicked on Azure repo → 

![Untitled 4](https://user-images.githubusercontent.com/42151912/210068261-aca9d785-f72a-442c-9dd8-551f36e7820f.png)



Then I clicked on starter pipeline for our configuration → 

![Untitled 5](https://user-images.githubusercontent.com/42151912/210068276-aae2da03-fd66-437a-b194-7d2047c37b81.png)



Now that the YAML is up for review and save and run, normally I avoid “commit directly to the main branch” and choose create a new branch because we are just creating it now then merge to main branch after it is working well for best practices, after I hit run → 

![Untitled 6](https://user-images.githubusercontent.com/42151912/210068300-a65b1d27-a446-483f-842f-897db5fe829b.png)



The CI pipeline is successful → 

![Untitled 7](https://user-images.githubusercontent.com/42151912/210068313-87952533-ff41-4950-bc06-bd79e40917c3.png)

![Untitled 8](https://user-images.githubusercontent.com/42151912/210068329-0320ab4a-7e06-47e2-a562-cb84f173daf2.png)



If I go back to edit pipeline → more actions → we can see the options of downloading this full YAML file or validate the pipeline for last minute changes in code to the YAML file: 

![Untitled 9](https://user-images.githubusercontent.com/42151912/210068355-e2ebeb61-2a33-4003-83cb-0ba26fd15ed5.png)
