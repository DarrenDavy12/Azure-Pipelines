# Azure Repo - Migrate, Commit, Push and Merge Code


Code Management with Azure Repos

Azure Repos - It is a version control tool that you could use to manage your code, whether you’re a software engineer working in a single team or working individually, you need a version control system to track the changes you made. As you edit and start building a project, you need version control, in Azure DevOps is built on top of Git which is the most common version control used today and becoming the factory standard for version control. 


First I make a new repository

![Untitled](https://user-images.githubusercontent.com/42151912/210071970-23386459-1509-4068-8aff-16cd806a9915.png)

![Untitled 1](https://user-images.githubusercontent.com/42151912/210071981-cfc232a6-1f4f-4e51-8d13-19a196fa62ba.png)


Then I pull my code, by going to clone and because I’m using macOS I will pick SSH and copy it.

Paste it inside visual studio code. 


1. To find RSA token - run `cat ~/.ssh/id_rsa.pub` and copy the whole key.
 
2. Head to ‘manage ssh keys’ under the git clone link on Azure DevOps 

![Untitled 2](https://user-images.githubusercontent.com/42151912/210072023-0c64d586-1f27-433a-bdd3-88ae48e7cafd.png)


3. Hit add and give name and paste key and save. 

![Untitled 3](https://user-images.githubusercontent.com/42151912/210072069-6aca40b5-acc5-437d-897b-9b9b0ef8f44d.png)



I ran git clone command and it successfully pulled out the repo.

![Untitled 4](https://user-images.githubusercontent.com/42151912/210072113-1c9267bf-21d1-4f6f-8bed-c69f2f0a65d4.png)



Open up the repo we pulled that contains a [README.md] file. 

![Untitled 5](https://user-images.githubusercontent.com/42151912/210072127-b3e3704e-c804-4624-8fae-faf03d624bfe.png)



I make some changes to the [README.md] file, by adding integration test and unit test. Then I go to source tab in VSCode.

![Untitled 6](https://user-images.githubusercontent.com/42151912/210072174-6315c4ec-6f64-4f75-98d0-bdb8c986ddc6.png)

![Untitled 7](https://user-images.githubusercontent.com/42151912/210072180-f233ff1a-cee2-48d6-807d-9eaa01e2c1cf.png)



I head back to the terminal and run a git status inside the repo directory and it has recognised my change. 

![Untitled 8](https://user-images.githubusercontent.com/42151912/210072196-1fb4f6a4-c6e6-4ec8-a64d-4545724a3615.png)



To see all the branches - run `git branch` for 1 branch and `git branch -a` for all branches.

![Untitled 9](https://user-images.githubusercontent.com/42151912/210072207-8a36783c-04fe-47f6-ab6a-364ca799834c.png)

![Untitled 10](https://user-images.githubusercontent.com/42151912/210072225-c475447b-d517-411e-b169-17f2dc028623.png)


To create a new branch run `git branch feature/darren` and then run `git branch -a` again.

![Untitled 11](https://user-images.githubusercontent.com/42151912/210072273-2698c9af-c237-4293-9d09-5fd77efe5bd7.png)

Afterwards I run `git add .` and after a `git commit -m <message>` the message can be a work item ID number from my azure DevOps project for example. 

![Untitled 12](https://user-images.githubusercontent.com/42151912/210072412-49cada92-5e6d-489d-aefc-f7890da16f81.png)

![Untitled 13](https://user-images.githubusercontent.com/42151912/210072422-d8624b6a-40f5-4ef1-9ca9-281a65cf615c.png)


Then a `git push` 

![Untitled 14](https://user-images.githubusercontent.com/42151912/210072437-1f1c4ccd-4d0b-4ffc-a370-69bf71f8a130.png)

![Untitled 15](https://user-images.githubusercontent.com/42151912/210072449-d35f05da-08cb-4f7f-a7eb-5535eca751f6.png)



If I got back to Azure DevOps repo tab and go in history, we can see our comment and see the changes made inside.

![Untitled 16](https://user-images.githubusercontent.com/42151912/210072470-279b6d4a-682c-4c73-94fd-2be7bb01efe9.png)

![Untitled 17](https://user-images.githubusercontent.com/42151912/210072482-89e29be7-2fa9-44d5-93b8-90b5552a5d33.png)



By click on [README.md] file in Repos/Files I can also edit files within Azure Repos by clicking on edit.

![Untitled 18](https://user-images.githubusercontent.com/42151912/210072509-a721aa24-822f-4ab7-a1ce-52ec10934988.png)

![Untitled 19](https://user-images.githubusercontent.com/42151912/210072520-f407af11-909c-4125-9705-c9acaff36dc4.png)


After applying a change, click commit to save the change. 

![Untitled 20](https://user-images.githubusercontent.com/42151912/210072552-8115fdfb-efa1-423c-9257-a7e50e10a1af.png)


Once I click commit, I can link other work items and click commit. 

![Untitled 21](https://user-images.githubusercontent.com/42151912/210167051-06a927c2-3e2e-4dd2-bf1b-3785d186f6c7.png)


If I go back to work items under Boards, I can see on the right hand side under development my commits. Now the commit from my local system is now linked with my story.

![Untitled 22](https://user-images.githubusercontent.com/42151912/210167057-4fcf10c4-e912-480e-b724-0472d6e90f2a.png)


Somebody can look at my store changes and wants to make a comment along with what story. 

![Untitled 23](https://user-images.githubusercontent.com/42151912/210167062-67cfa4d5-d60a-4f6f-b27c-91b268e7ff53.png)


Migrate Repo from GitHub - Commit Code from Local

First I do a `git pull` 

![Untitled 24](https://user-images.githubusercontent.com/42151912/210167066-36d58201-0ff4-4713-9ee7-df1863aab2a9.png)

![Untitled 25](https://user-images.githubusercontent.com/42151912/210167090-c2999a41-3315-4731-ac9e-c15ecf21fdaf.png)


Then I switch branch using `git checkout feature/<name>`

![Untitled 26](https://user-images.githubusercontent.com/42151912/210167098-982359ce-6437-4931-8a38-a7c96f73a23c.png)


I run `git branch` it should now be pointing to the feature branch.

![Untitled 27](https://user-images.githubusercontent.com/42151912/210167103-73618e1b-62e0-4cc4-9a6d-567b4fe4bed6.png)


Now, whatever changes I made, if I add a new file called `[main.tf](http://main.tf)` for example. 

Generally everything is not pushed on the master branch, that why we make our own branch. You want to make sure that we do the development first. Then test the code on your local system or some else’s server and once we are fully confident with the changes not breaking anything on production we can push to master branch.

So I added an terraform file and made a resource with some values.

![Untitled 28](https://user-images.githubusercontent.com/42151912/210167105-adc1efb7-b74a-4871-84cf-2aa5742ee2dc.png)


Then if go to source control on vscode and see the changes. I can also make git commits in the little text box on the upper left hand side and reference a work item ID with some text for the commit. 

![Untitled 29](https://user-images.githubusercontent.com/42151912/210167111-1b24f3a7-a906-4432-9941-8b45ec3acdd4.png)

![Untitled 30](https://user-images.githubusercontent.com/42151912/210167117-c6bc8cc3-97f8-49a1-8945-09d70ac1df7e.png)


Afterwards I ran a `git push` , since it is not my master branch I must run `git push --set-upstream origin feature/<name>` 

![Untitled 31](https://user-images.githubusercontent.com/42151912/210167150-b9fd1e96-3726-4955-a832-fa62e54e89e8.png)

![Untitled 32](https://user-images.githubusercontent.com/42151912/210167160-39a11bd2-b331-4314-8eaf-246df4439dc3.png)


Now I go back to my repo in Azure DevOps and click on main at the top, we see that has appeared. 

![Untitled 33](https://user-images.githubusercontent.com/42151912/210167195-306eb941-a8c9-4087-aec5-c5f6171661bc.png)


I can also make a pull request under tags, make a new pull request, add a description and add a reviewer. Afterwards I hit create. 

Pull request is for when you don’t want to work on a master branch, it lets others know about the changes you pushed to your branch. When you open a new pull request, which we’re going to do right now, you can discuss and review potential changes you’ve made with the other team members.


![Untitled 34](https://user-images.githubusercontent.com/42151912/210167203-72bbb697-e032-4a7c-8f99-b77dd538c9f0.png)

![Untitled 35](https://user-images.githubusercontent.com/42151912/210167209-4a67ac51-00b6-49f5-95cc-b44374c35007.png)


I can also head over to commits tab next to updates and any changes we are not happy with, we can go ahead and make the comment as well. 

![Untitled 36](https://user-images.githubusercontent.com/42151912/210167214-f4f9c892-f52f-4bf6-a81d-a997eb581813.png)


Then I head back to VSCode and create a `[var.tf](http://var.tf)` for my variables.

![Untitled 37](https://user-images.githubusercontent.com/42151912/210167220-cb6f637e-39f0-45dc-8a93-72b2892ce571.png)


In the [main.tf](http://main.tf) next to name put the variable and commit changes.

![Untitled 38](https://user-images.githubusercontent.com/42151912/210167231-f35d4e69-0c24-437c-9f45-ac68bf21ecf6.png)


Run a `git pull` 

![Untitled 39](https://user-images.githubusercontent.com/42151912/210167236-bf97363c-6337-4ada-a778-089ce3db8494.png)


Then I go to source control on the left hand side and make a commit.

![Untitled 40](https://user-images.githubusercontent.com/42151912/210167242-ff4505a8-9d88-4b23-8b31-fcd0d0aac822.png)


Run a `git push` afterwards.

![Untitled 41](https://user-images.githubusercontent.com/42151912/210167249-a1fbf1a6-27ce-4b35-8144-7afc7d1fad46.png)


Back on pull requests on Azure DevOps, we can view the commit. I can also have approve and rejection options. 

![Untitled 42](https://user-images.githubusercontent.com/42151912/210167256-58869e82-2095-4e12-81e1-65266de8a440.png)

![Untitled 43](https://user-images.githubusercontent.com/42151912/210167283-77eb8442-eb20-45bf-a7f1-3a75bf199645.png)


Then I go back and select master branch under repos/files, head back to pull request, click on request and click complete. This will merge it back with the main branch.

![Untitled 44](https://user-images.githubusercontent.com/42151912/210167290-e9544b8f-319a-41c1-81c9-2142bae917f3.png)

![Untitled 45](https://user-images.githubusercontent.com/42151912/210167294-09a1b0c1-9c80-46fd-9ccd-c960f595eec0.png)

![Untitled 46](https://user-images.githubusercontent.com/42151912/210167296-c12c29e3-d39b-49b4-a0c9-ab7be388e9c2.png)

![Untitled 47](https://user-images.githubusercontent.com/42151912/210167299-ae2624b1-33c9-4724-9a4b-1eb0922024a8.png)


If I head back to files, we can see that [main.tf](http://main.tf) and [var.tf](http://var.tf) have been added.

![Untitled 48](https://user-images.githubusercontent.com/42151912/210167308-f5b09946-025e-4098-9e4a-5cd628ef3575.png)

![Untitled 49](https://user-images.githubusercontent.com/42151912/210167310-f58bbc9c-f228-407e-af32-9cb34f5f0312.png)


Then I run a `git pull`

![Untitled 50](https://user-images.githubusercontent.com/42151912/210167331-6aa121e5-8426-4af9-8bc8-0462d80c9d94.png)

