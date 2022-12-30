# Azure DevOps and Boards

Azure DevOps Organisation & Projects - Work Items


1. Login into Azure DevOps and create a new project with private access → 

![Untitled](https://user-images.githubusercontent.com/42151912/210071079-b08741e4-4bed-4f33-a254-a648c26c8d3e.png)



2. Then head over to Boards. First we get started with work item, work items are a tracker for debugs, adding defects, work being assigned to users etc.
- 3 types of work items - Epic, issue, task
- To do state
- Add description
- Add discussion
- Planning priority
- Start and Target Date
- History tab, Link tab for existing tasks and attachments tab for screenshots, architectural diagrams(right hand side)
- Follow will notify us if anything happens to the work item like changes, adding comments and new assigned users


Main tab

![Untitled 1](https://user-images.githubusercontent.com/42151912/210071101-416e7f32-b215-4e04-b138-5aa5ecd3304d.png)



History tab

![Untitled 2](https://user-images.githubusercontent.com/42151912/210071107-1c237648-c634-4183-9aee-1afd1e9f4bb9.png)



Link tab

![Untitled 3](https://user-images.githubusercontent.com/42151912/210071122-d362e809-4144-4a0a-9eee-e1dec848e737.png)



Attachment tab

![Untitled 4](https://user-images.githubusercontent.com/42151912/210071137-5a98a35d-b592-439a-a937-01283e0dd800.png)



Once I saved the work item 

![Untitled 5](https://user-images.githubusercontent.com/42151912/210071155-a4e1043c-6d05-4063-95e9-681d69549615.png)



3. Queries - queries are used for creating rules and run queries from relevant tags been used in work items. 

![Untitled 6](https://user-images.githubusercontent.com/42151912/210071175-71c6e8f9-e565-4a98-8c8f-93cfb27a354e.png)

![Untitled 7](https://user-images.githubusercontent.com/42151912/210071190-975f2920-b7dd-41e7-bc1d-c40941c0ce99.png)



Azure Boards & Backlog

4. First I will make a new project which is going to be an agile project. I select agile for my work item process and hit create. 

![Untitled 8](https://user-images.githubusercontent.com/42151912/210071213-7d737979-7366-4e16-ae46-0b3833e2687a.png)



Now inside boards/work items we have even more types of work items we can create 

![Untitled 9](https://user-images.githubusercontent.com/42151912/210071229-ce4fdde5-38cc-42e8-bea3-4f6be0976200.png)



I select user story work item, the process is similar to the other work items. I create a few user story work items.

![Untitled 10](https://user-images.githubusercontent.com/42151912/210071255-0f3455f1-cbcb-41f1-a867-a69e9e217a25.png)

![Untitled 11](https://user-images.githubusercontent.com/42151912/210071268-d180abf1-db3e-4ed7-9909-e05301f686c2.png)



The second user story work item is for the CI CD Pipeline. I add a user to this work item. 

![Untitled 12](https://user-images.githubusercontent.com/42151912/210071289-07b1ea0f-e273-4b5f-8b4f-2c2a3b6462e4.png)



Third user story work item is for testing 

![Untitled 13](https://user-images.githubusercontent.com/42151912/210071304-3fe9d8f4-05e0-4401-abff-2eee3b9a862f.png)



Then I head over to backlogs, backlogs are basically any ideas, any feature, any big, anything, any small requests you captured in a form of a work item. Within backlog you define that which work item needs to be prioritised. There can be hundred of work items I logged in, but I’ve got to reorder them. Some need to be highest priority if being more focused on. 

![Untitled 14](https://user-images.githubusercontent.com/42151912/210071349-3b675127-b23f-4dcb-a73e-9ec5dc1335d1.png)



If I go to Boards, I have multiple tasks I’ve created, this a holistic view of what the individual or team is doing, project manager or director to see who is doing what, each task can be dragged along from new, active, resolved and closed. This is how you manage multiple tasks, this is beneficial when you’re working on the sprint and have time box. 

![Untitled 15](https://user-images.githubusercontent.com/42151912/210071364-8ddd0aa5-8c4b-42fd-b8de-5bf31e708a5d.png)

![Untitled 16](https://user-images.githubusercontent.com/42151912/210071389-b5e0d72b-284f-433a-a9ce-2d7592de5599.png)


Sprints - You can time box your work items. Generally these sprints are two to four weeks, and within the two weeks you ask the developers that these are the stories which we want to complete. Any task that is being done within the sprint, you plan ahead with other sprints. Usually you start off sprint with sprint planning, you discuss with the devs, infrastructure and testers and decide which features and stories are relevant for the particular sprint based on the business needs. 

An authentication mechanism that meets the following requirements:

- Supports authentication from Git
- Minimizes the need to provide credentials during authentication

I recommend personal access tokens in Azure DevOps
