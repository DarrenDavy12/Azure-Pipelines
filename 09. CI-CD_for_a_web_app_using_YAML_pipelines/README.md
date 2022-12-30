# CI/CD pipeline for a web application using YAML pipelines


## One pipeline for CI/CD:


I create a new pipeline, then I select Azure repos git, choose my repo and select starter pipeline. 

![Untitled](https://user-images.githubusercontent.com/42151912/210066074-a1867332-d453-4460-b19f-ebf5625a2bda.png)

![Untitled 1](https://user-images.githubusercontent.com/42151912/210066087-70872c16-44bb-43ff-9774-453e9a68c836.png)

![Untitled 2](https://user-images.githubusercontent.com/42151912/210066098-1e3b339b-3d4d-42de-b25d-ba851d62bddf.png)


In the YAML file, I remove the comments and set the trigger to none and remove everything else underneath. Now I put in stage 1 which will be the building stage and stage 2 is deploy, under build, I display a name and the same for the deploy stage 

![Untitled 3](https://user-images.githubusercontent.com/42151912/210066123-60d738b4-6a41-4134-91d8-a627b65cbcbe.png)


Now I need to define jobs for both stages 

![Untitled 4](https://user-images.githubusercontent.com/42151912/210066139-be577280-6644-4ba5-abd5-047c97721408.png)


Then I add the pool, variables after the building stage and I also add deployment after the deployment stage.
