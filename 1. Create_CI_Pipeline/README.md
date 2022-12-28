# (Azure) Creating Java CI pipeline:

To start off I head over to Azure DevOps website, create project and give name some what referencing the name of the project I forked over a SCM in which one I am using is GitHub.→

Give name and select public → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled.png)

Then I head over to Pipelines/Pipelines on the dashboard → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%201.png)

I would click create pipeline and choose the SCM system we want to use, the application we are using is available on GitHub, I click on Use Classic editor without YAML and click GitHub → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%202.png)

Choose my forked repo for GitHub underneath and leave branch on master → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%203.png)

Then my template will be Maven → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%204.png)

Now I’ll select what agent I what to use, this means choosing the virtual machine to run our pipeline, in this case it needs a virtual machine that can handle Java environment, Java, JDK, and GRG etc →  

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%205.png)

I go over to parameters and browse for my path for the `pom.xml` file → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%206.png)

Once I selected the file it will change path to that one I selected → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%207.png)

In the side window for maven: 

I use Corbertura for my coverage tool and leave everything else as default → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%208.png)

So this task will run Maven, clean package and generate the jar file. Then that jar file needs to be past through those two different tasks. 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%209.png)

The first one is to copy the jar files or the artifacts into a folder called Build or Artifact Staging. 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%2010.png)

Publish build artifact Then when published into the artifact, into another folder called drop. This means the Artifact I have a folder called drop inside of it and have my jar file for the application → 

![Untitled]((Azure)%20Creating%20Java%20CI%20pipeline%20ebe0f4a368da4c2bb8287780e416de41/Untitled%2011.png)
