### [Data Model, Entities, and Attributes](https://cocoacasts.com/data-model-entities-and-attributes/)

#### Author: Bart Jacobs

The data model is a key component of the Core Data stack and an integral part of every Core Data application. In this tutorial, we explore the data model and learn about entities and attributes.

## Setting Up the Project

The best way to learn is by doing. Open Xcode and create a new project, choosing the **Single View Application** template. Name the project **Data Model** and tell Xcode to populate the project with boilerplate code for Core Data by checking the **Use Core Data** checkbox.

![Data Model, Entities, and Attributes | Setting Up the Project](https://cocoacasts.s3.amazonaws.com/data-model-entities-and-attributes/figure-project-setup-1.jpg)

![Data Model, Entities, and Attributes | Setting Up the Project](https://cocoacasts.s3.amazonaws.com/data-model-entities-and-attributes/figure-project-setup-2.jpg)

Take a quick look at **AppDelegate.swift** to refresh your memory. The application delegate creates an instance of the `NSPersistentContainer` class, which is responsible for setting up and managing the Core Data stack.

## Exploring the Data Model

When the application sets up the Core Data stack, the managed object model loads the data model from the application bundle. The file that's loaded from the application bundle is named **Data_Model** and has a **.momd** extension. The extension stands for **managed object model document**.

If you open the **Project Navigator** on the left, you should see a file named **Data_Model**. The file's extension, **.xcdatamodeld**, doesn't match, though. And yet if you run the application, the Core Data stack is set up without issues. How is that possible?

When the application is built, the data model file you see in the **Project Navigator** is compiled into a **.momd** file. Why is that necessary? Why does the data model need to be compiled?

The **.xcdatamodeld** file is the file we edit in Xcode during development. We use it for defining the application's data model. It shows us a visual representation of the data model as we will see in a moment. Much of the information in the **.xcdatamodeld** file is not needed for Core Data to do its work. At compile time, Xcode collects the data it needs from the **.xcdatamodeld** file and creates a **.momd** file. It is the **.momd** file that is included in the application bundle. The resulting **.momd** file is much smaller, containing only what is absolutely essential for Core Data to infer the data model.

**Read this article on [Cocoacasts](https://cocoacasts.com/data-model-entities-and-attributes/)**.
