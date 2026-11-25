##Pre-Mid Semester Exam Mockup Questions##

1. Choosing the Right SDLC Model

For Project B, which is a food-delivery mobile application for a startup, I would recommend the Agile/Scrum model.

The main reason is that startups usually operate in rapidly changing markets, where customer needs and requirements can change frequently. Agile allows developers to build the application in small stages, test each feature, and collect feedback from users. This makes it easier to introduce changes without restarting the entire development process.

Another advantage is that testing happens regularly throughout development, allowing developers to identify and fix problems early. Since a food-delivery application is not as safety-critical as aircraft control software, Agile provides a suitable balance between development speed, flexibility, and quality.


2. The Hidden Trade-offs of Rapid Application Development (RAD)

RAD focuses on developing software quickly by using prototypes and reducing extensive upfront planning. However, this can create problems when an application becomes larger.

When developers focus mainly on making a working prototype quickly, they might ignore important architectural decisions, security, and long-term performance. As more features are added, the application can become difficult to maintain and expand.

For example, a small application might work perfectly for 100 users, but when thousands of users start using it, poor architecture and database design may cause performance problems.

Therefore, RAD can save time initially, but without proper planning and design, it can create reliability and scalability problems in the future.


3. Balancing Software Development Principles

Yes, following DRY and Separation of Concerns too strictly can sometimes violate KISS and YAGNI.

For example, imagine a developer creating a simple calculator application. Instead of writing a few straightforward functions, the developer creates multiple classes, interfaces, and complex abstractions just to avoid repeating a small amount of code.

Although the developer is trying to follow DRY, the program becomes unnecessarily complicated.

KISS encourages developers to keep solutions simple, while YAGNI reminds them not to implement features or structures that are not currently needed.

Therefore, developers should understand that these principles are guidelines, not strict rules. The goal is to write clean, maintainable, and simple code without unnecessary complexity.

4. The Economics of Testing and Code Quality

The cost of correcting an error is lowest during the early stages of software development because fewer parts of the system depend on the incorrect requirement or design.

If an error is discovered during the requirements or design stage, it can usually be corrected with little effort. However, if the same error is discovered after deployment, developers may need to modify the code, database, and other connected components.

TDD helps reduce this cost by encouraging developers to write tests before implementing the actual code. This helps identify problems early.

Code reviews also help because other developers examine the code and identify mistakes, weaknesses, or poor practices before the code becomes part of the final application.

Therefore, early testing and regular code reviews help reduce development costs and improve software quality.


5. MSIL, JIT, and the Platform Independence Paradox

MSIL (Microsoft Intermediate Language) is CPU-independent because it is not directly written for a specific processor. Instead, it is an intermediate language that can be converted into native machine code by the JIT compiler.

However, traditional .NET Framework applications are platform-dependent because they rely on the CLR and libraries designed specifically for Windows.

This means that even though MSIL is CPU-independent, the application still needs a compatible runtime and operating system to execute.

Technologies like Mono helped solve this limitation by providing a .NET-compatible runtime for other operating systems, including Linux and macOS. This allowed developers to run certain .NET applications outside Windows.


6. Managed vs. Unmanaged Code & Language Interoperability

Managed code runs under the supervision of the Common Language Runtime (CLR), which provides services that improve program safety and reliability.

For example, the CLR provides automatic memory management through Garbage Collection, type safety, and array bounds checking. These features help prevent common programming errors and reduce memory-related problems.

Unmanaged code, on the other hand, runs outside the direct control of the CLR and requires developers to manage resources more manually.

MSIL and the Common Type System (CTS) also allow different .NET programming languages to work together.

For example, one developer can write part of an application in C# while another writes a different part in VB.NET. The CTS ensures that both languages use compatible data types. For instance, a string in C# and a String in VB.NET represent the same underlying .NET type.

This makes communication between different .NET languages possible without major data compatibility problems.

7. Solving DLL Hell: Assemblies, Manifests, and Namespaces

DLL Hell happened when installing or updating one application could overwrite a shared DLL file and cause another application to stop working.

.NET helps solve this problem through assemblies, manifests, strong names, and the Global Assembly Cache (GAC).

An assembly is a compiled unit of deployment, usually an EXE or DLL file. It contains code, metadata, and other resources required by the application.

The manifest contains important information about the assembly, including its name, version, and dependencies.

Strong names provide a unique identity to assemblies using information such as the assembly name, version, culture, and public key.

The Global Assembly Cache (GAC) stores shared assemblies so that multiple applications can use them. It also allows different versions of an assembly to exist side by side.

A namespace is different from an assembly. A namespace is used to logically organize classes and avoid naming conflicts, while an assembly is the physical compiled file used for deployment.

Therefore, they are not interchangeable because they serve different purposes.


8. Abstraction in Data Access: ADO.NET vs. Entity Framework & LINQ

Working directly with ADO.NET can be error-prone because developers have to manually manage database connections, write SQL queries, handle DataSets, and convert database results into application objects.

This requires more code and increases the possibility of mistakes, especially in large applications.

Entity Framework provides a higher level of abstraction through Object-Relational Mapping (ORM). It allows developers to work with database records as normal C# objects instead of manually handling every database operation.

For example, instead of manually writing queries to retrieve student records, developers can work with Student objects and let Entity Framework handle much of the database interaction.

LINQ also makes querying easier because it provides a common way to query different types of data, including databases, XML, and collections.

The main advantage is reduced code, easier maintenance, and faster development. However, Entity Framework can sometimes have performance overhead and gives developers less direct control over SQL queries compared to raw ADO.NET.


9. Under the Hood of Event-Driven Programming*

A Console application normally executes instructions sequentially, starting from the Main() method until the program finishes.

A Windows Forms application works differently because it uses event-driven programming. Instead of executing everything sequentially, it waits for user actions such as clicking a button, typing text, or selecting an option.

When a user clicks a button, the operating system detects the action and sends an event to the application. The Windows Forms event system then identifies the appropriate event handler associated with that button.

The event handler executes the code written by the developer to respond to that action.

For example, when a user clicks a Login button, the Click event handler can read the username and password and check whether they are correct.

After handling the event, the application returns to waiting for other user interactions.

This process is managed through an event loop, which allows Windows Forms applications to remain interactive while waiting for user input.