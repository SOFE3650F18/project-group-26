**Step 2: Establish iteration goal by selecting drivers**


In the second iteration, besides CRN-1 (Create and define the overall system), we are considering the system’s primary use cases:
 * UC-1: User system with specified roles
 * UC-4: Synchronize User information with university database information


**Step 3: Choose one or more elements of the sytem to refine**

**Step 4: Choose one or more design concept that satisfy the selected drivers**

| Design Decisions and Location                               | Rationale and Assumptions                                                                                                                                                                                                                                                                                                       |  
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Create a Domain Model for the application                   | Before we start functional decomposition, it’s necessary to create an initial domain model for the system, to identify the major entities in the domain.  Since there are no good alternatives, a domain model must be made or it will be created in least optimal manner which in turn will be hard to maintain and understand |
| Identify Domain Objects that map to functional requirements | Each distinct functional element of the application needs to be encapsulated in a self-contained building block - a domain object.  Directly composing layers increases the risk of not considering a requirement                                                                                                               |
| Decompose Domain Objects into layered components            | Domain objects represent complete sets of functionality, but this functionality is supported by finer-grained elements located within the layers. The “components” in this pattern are what are referred to as modules                                                                                                          |

**Step 5: Instantiate architectural elemtns, allocate responsibilities, and define interfaces**

**Step 6: Sketch views and record design decisions**

![alt Initial Domain Model](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%202/InitialDomainModel.PNG)   

*Figure: Initital Domain Model*

![alt Domain Objects](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%202/DomainObjectsAssociatedWithUseCases.PNG)   

*Figure: Domain Objects Associated with Use Cases*

![alt Primary Use Case Modules](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%202/PrimaryUseCaseSupportModules.PNG)   

*Figure: Modules that support primary use cases*

Use Case 1: Account System
The next diagram is a sequence diagram shows how the user will access the system based on their role within the system. Once the user launches the browser, they will be prompted for account credentials which they will use to login into the system. The account they logged into will tied to a specific role in the system which will define their permissions and access to the system.


![alt Use Case 1 Sequence Diagram](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%202/UC-1.PNG)   

*Figure:  Sequence Diagram for UC-1*

Use Case 4: Record System
The next diagram is a sequence diagram that shows how the user will access system records within the course management. Once the users role is determined from the steps in the previous diagram, the user will be able to request information from the server. The server will respond based on the accounts role and the information they request. The user will only be prompted with available information for their specific role.


![alt Use Case 4 Sequence Diagram](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%202/UC-4.PNG)   

*Figure:  Sequence Diagram for UC-4*

**Step 7: Perform analysis of current design and review iteration goal and achienvement of design purpose**





















