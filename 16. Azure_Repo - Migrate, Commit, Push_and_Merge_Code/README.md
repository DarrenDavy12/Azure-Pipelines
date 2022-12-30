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

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%202.png)

1. Hit add and give name and paste key and save. 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%203.png)

I ran git clone command and it successfully pulled out the repo.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%204.png)

Open up the repo we pulled that contains a [README.md](http://README.md) file. 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%205.png)

I make some changes to the [README.md](http://README.md) file, by adding integration test and unit test. Then I go to source tab in VSCode.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%206.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%207.png)

I head back to the terminal and run a git status inside the repo directory and it has recognised my change. 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%208.png)

To see all the branches - run `git branch` for 1 branch and `git branch -a` for all branches.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%209.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2010.png)

To create a new branch run `git branch feature/darren` and then run `git branch -a` again.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2011.png)

Afterwards I run `git add .` and after a `git commit -m <message>` the message can be a work item ID number from my azure DevOps project for example. 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2012.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2013.png)

Then a `git push` 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2014.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2015.png)

If I got back to Azure DevOps repo tab and go in history, we can see our comment and see the changes made inside.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2016.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2017.png)

By click on [README.md](http://README.md) file in Repos/Files I can also edit files within Azure Repos by clicking on edit.

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2018.png)

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2019.png)

After applying a change, click commit to save the change. 

![Untitled](Azure%20Repo%20-%20Migrate,%20Commit,%20Push%20and%20Merge%20Code%2006d22125eee14e959845a7897fed5ecd/Untitled%2020.png)

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
