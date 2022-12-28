# (Azure) Creating Java CI pipeline:

To start off I head over to Azure DevOps website, create project and give name some what referencing the name of the project I forked over a SCM in which one I am using is GitHub.→


Give name and select public → 

![Untitled](https://user-images.githubusercontent.com/42151912/209808363-f30c316e-4a64-4410-ad25-46e2170f8d52.png)


Then I head over to Pipelines/Pipelines on the dashboard → 

![Untitled 1](https://user-images.githubusercontent.com/42151912/209808530-8292214f-68ea-4a50-92bf-796ad58f67de.png)


I would click create pipeline and choose the SCM system we want to use, the application we are using is available on GitHub, I click on Use Classic editor without YAML and click GitHub → 

![Untitled 2](https://user-images.githubusercontent.com/42151912/209808644-a98ba7cb-29b6-4031-be24-2c98d12e9309.png)


Choose my forked repo for GitHub underneath and leave branch on master → 

![Untitled 3](https://user-images.githubusercontent.com/42151912/209808689-0202ace8-c4b8-4171-9752-64577bb17d59.png)


Then my template will be Maven → 

![Untitled 4](https://user-images.githubusercontent.com/42151912/209808806-dce63482-2400-4fbe-ab10-418f61d9a0b0.png)


Now I’ll select what agent I what to use, this means choosing the virtual machine to run our pipeline, in this case it needs a virtual machine that can handle Java environment, Java, JDK, and GRG etc →  

![Untitled 5](https://user-images.githubusercontent.com/42151912/209808840-4a22cfda-58c9-4a42-b7d9-2f07c1c07184.png)


I go over to parameters and browse for my path for the `pom.xml` file → 

![Untitled 6](https://user-images.githubusercontent.com/42151912/209808932-ff86ee3b-a573-4731-9788-13c6c6f15ccd.png)


Once I selected the file it will change path to that one I selected → 

![Untitled 7](https://user-images.githubusercontent.com/42151912/209808979-2327acca-f33e-408c-a714-56704e139c83.png)


In the side window for maven: 

I use Corbertura for my coverage tool and leave everything else as default → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%208.png)

So this task will run Maven, clean package and generate the jar file. Then that jar file needs to be past through those two different tasks. 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%209.png)

The first one is to copy the jar files or the artifacts into a folder called Build or Artifact Staging. 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%2010.png)

Publish build artifact Then when published into the artifact, into another folder called drop. This means the Artifact I have a folder called drop inside of it and have my jar file for the application → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%2011.png)
