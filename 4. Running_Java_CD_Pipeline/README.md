# (Azure) Running Java CD pipeline:

Click create release, leave default and click create→ 

![Untitled](https://user-images.githubusercontent.com/42151912/209975510-57619129-001e-4b0a-ac18-866eef1d44c5.png)


Open link in new tab of the release, now I can see the production is in process → 

![Untitled 1](https://user-images.githubusercontent.com/42151912/209975534-53e8308e-0e0d-427c-a4d2-1db63a925484.png)

![Untitled 2](https://user-images.githubusercontent.com/42151912/209975559-c071ba56-e7da-42cf-9ed5-d333b4d8dbd2.png)


Now I click on logs →

![Untitled 3](https://user-images.githubusercontent.com/42151912/209975644-c4422f7f-0f91-4fae-a824-7663327d2e5b.png)


And here we can see that Azure DevOps has found an agent to run my pipeline, it started by downloading the artifacts that contains my drop folder that contains my .jar file, then it started performing the deploy azure app service task, this task is the one that will connect to my Azure account. The package to app service tells me it successfully deployed a package to the app service. 

![Untitled 4](https://user-images.githubusercontent.com/42151912/209976025-a49c42b3-b6b9-44c4-848e-78153b51e339.png)

![Untitled 5](https://user-images.githubusercontent.com/42151912/209976101-417411b8-70eb-4d68-ac01-19eb7dbe7647.png)


The App Service Application URL: <url> is where my .jar file has deployed to, so I open a new tab with this URL → 

![Untitled 6](https://user-images.githubusercontent.com/42151912/209976224-76b3f62d-c1b3-4374-813c-fa4fd559d7b4.png)

  
And here we see the message coming from my Springwood application → 

![Untitled 7](https://user-images.githubusercontent.com/42151912/209976355-3e0ae17a-dc4b-499a-bfad-ef9b990d8dde.png)

  
Now I will go over to our CI pipeline deploy URL we connected to earlier, refresh that page and should see the same page → 

![Untitled 8](https://user-images.githubusercontent.com/42151912/209976408-7ec4afca-cd90-4f63-bcc8-525fa351d79e.png)
