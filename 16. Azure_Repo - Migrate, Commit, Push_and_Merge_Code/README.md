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

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2021.png)

If I go back to work items under Boards, I can see on the right hand side under development my commits. Now the commit from my local system is now linked with my story.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2022.png)

Somebody can look at my store changes and wants to make a comment along with what story. 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2023.png)

Migrate Repo from GitHub - Commit Code from Local

First I do a `git pull` 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2024.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2025.png)

Then I switch branch using `git checkout feature/<name>`

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2026.png)

I run `git branch` it should now be pointing to the feature branch.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2027.png)

Now, whatever changes I made, if I add a new file called `[main.tf](http://main.tf)` for example. 

Generally everything is not pushed on the master branch, that why we make our own branch. You want to make sure that we do the development first. Then test the code on your local system or some else’s server and once we are fully confident with the changes not breaking anything on production we can push to master branch.

So I added an terraform file and made a resource with some values.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2028.png)

Then if go to source control on vscode and see the changes. I can also make git commits in the little text box on the upper left hand side and reference a work item ID with some text for the commit. 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2029.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2030.png)

Afterwards I ran a `git push` , since it is not my master branch I must run `git push --set-upstream origin feature/<name>` 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2031.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2032.png)

Now I go back to my repo in Azure DevOps and click on main at the top, we see that has appeared. 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2033.png)

I can also make a pull request under tags, make a new pull request, add a description and add a reviewer. Afterwards I hit create. 

Pull request is for when you don’t want to work on a master branch, it lets others know about the changes you pushed to your branch. When you open a new pull request, which we’re going to do right now, you can discuss and review potential changes you’ve made with the other team members.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2034.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2035.png)

I can also head over to commits tab next to updates and any changes we are not happy with, we can go ahead and make the comment as well. 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2036.png)

Then I head back to VSCode and create a `[var.tf](http://var.tf)` for my variables.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2037.png)

In the [main.tf](http://main.tf) next to name put the variable and commit changes.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2038.png)

Run a `git pull` 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2039.png)

Then I go to source control on the left hand side and make a commit.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2040.png)

Run a `git push` afterwards.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2041.png)

Back on pull requests on Azure DevOps, we can view the commit. I can also have approve and rejection options. 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2042.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2043.png)

Then I go back and select master branch under repos/files, head back to pull request, click on request and click complete. This will merge it back with the main branch.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2044.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2045.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2046.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2047.png)

If I head back to files, we can see that [main.tf](http://main.tf) and [var.tf](http://var.tf) have been added.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2048.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2049.png)

Then I run a `git pull`

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2050.png)
