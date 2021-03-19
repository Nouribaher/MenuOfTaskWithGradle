## Novare:Software Development Academy|KTH => JAVA Project 






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

### Structs
I would say one of the simplest things that we do as a programmer is pass data from the application to save it to a file and do it in the Intellij IDEA software as follows:

```JAVA
/*
* FileInputMenuOftask is used to create a file and write data of the   task class  into it.
* This writer.close() method closes the file, Releases any system resources associated with the file and throws an IOException.
* This writer.write methods writes the specified byte to the file.
*@author   Nouri Baher
*@Softwear Intellij IDEA
*@version 2020.3
* @since  Mon, Feb 22, 2021 till Fri, Mar 19, 2021
*/

class FileInputMenuOftask {
    private String path = "src/TodoList/";
    private Object String;
  // Allow the user to save of the data task to the file
    public void WriteAsData (ArrayList<Task> list){
        try {
            FileWriter fileWriter = new FileWriter(new File (path + "OutOfTheFile.txt"));
            BufferedWriter writer = new BufferedWriter(fileWriter);
            for ( Task a : list){
                writer.write(a.toString()+"\n");
                writer.write("..................................................................................\n");
            }

            writer.close();
        }
        /*
         * @throws IOException  If an input or output
         *                      exception occurred
         */
        catch(IOException e) {
            System.out.println("Menu Of task doesn't found"+e);
        }

    }
    // Allow the user to read the data task from the file
    public ArrayList<Task> readASData(){
        ArrayList<Task> readerList = new ArrayList<>();
        try {
            File fileReader = new File (path+ "OutOfTheFile.txt");
            Scanner reader = new Scanner(fileReader);
            while (reader.hasNextLine()) {
                String data = reader.nextLine();
                System.out.println(data);
            }
            reader.close();

        }
        /*
         * @throws IOException  If an input or output
         *                      exception occurred
         */
        catch(IOException e) {
            System.out.println("Menu Of task error occurred." + e);
            e.printStackTrace();
        }
        return readerList;

    }
}
```
#### Usage 

![Example3](https://github.com/Nouribaher/TodoList/blob/main/Screenshot1.png)

### Testing
Testing is critical to your software. These packages help make it easier.
![Example4](https://github.com/Nouribaher/MenuOfTaskWithIntellijIDE/blob/master/TestTodoList.png) 
## Tools

### IntelliJ IDEA

**Good alternatives**: Eclipse and Netbeans 

The best Java IDE is IntelliJ IDEA . It has a ton of awesome
features, and is really the main thing that makes the verbosity of Java
bareable. Autocomplete is great.
The free community edition is good enough for me, but there are loads of great
features in the Ultimate edition like database tools, Spring Framework support
and Chronon.

## Support
Please enter an issue in the repo for any questions or problems. 
<br> Alternatively, please contact me at nouri.baher19@gmail.com
