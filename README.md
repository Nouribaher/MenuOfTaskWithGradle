
# Novare : Software Development Academy | KTH => JAVA Project 






<p align="center">
<img src="https://github.com/Nouribaher/MenuOfTaskWithIntellijIDE/blob/master/SDA.png" alt="OpenJ9 logo" align="midle" width="50%" height="50%" />
<p>





# TodoList Project
Allow me to draw your attention that Java is one of the most popular programming languages, in our case the Java app simulates the Todo List according to the Menu of Task by a program (“Intellij IDEA”) to help you keep track of the Todo List and it allows you to choose what you want to do as next one:
  * [Create new tasks, assign them a title, project name and due date]
  * [Edit, mark as done or remove tasks.]
  * [Save the current task list to file]
## Mockup 
![Example1](https://github.com/Nouribaher/MenuOfTaskWithIntellijIDE/blob/master/Menu.png)
  
## UML-Class-Diagram
UML (Unified Modeling Language) means that it is a way of representing the structure of Todo lists that includes classes, objects, packages, and the relationships between those elements.
![Example2](https://github.com/Nouribaher/TodoList/blob/main/TodoList-UML-Diagram.png).

## Usage
•	Using of easyUML that is a UML diagram tool for NetBeans.

•	Class diagrams contain classes, alongside with their attributes and their behaviours.

•	Relation between different classes represented as per shown below:

![Example2](https://github.com/Nouribaher/TodoList/blob/main/Components%20and%20Relations..png)

## Getting Started
This application can be run directly via TodoList or via generated jar file.

### Run with TodoList
In the first step, we should have to  know the path of files and start the application with the  Test's Run command.
```bash
 test run 
```
#### Test.Java 
This class is part of the TodoList app. As there are some lists that help the user to choose one of the tasks, 
and then the data will be sent to other classs and recorded in the class file to be saved, updated and reviewed at any time.
## Usage
```JAVA
import mport java.io.IOException;
import java.util.ArrayList;
        Task task = new Task("Nouri","1978-10-03","ITC","Maher");
        ArrayList<Task> taskArrayList = new ArrayList<>();
        taskArrayList.add(task);
        fileHandler.WriteAsData(taskArrayList);
        fileHandler.readASData();
```
![Example3](https://github.com/Nouribaher/TodoList/blob/main/Screenshot1.png)




## Support
Please enter an issue in the repo for any questions or problems. 
<br> Alternatively, please contact me at nouri.baher19@gmail.com
