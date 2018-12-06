# Iteration 2

**Step 1: Review Inputs**

 [Add Step 1: Review Inputs](https://github.com/SOFE3650F18/project-group-26/blob/master/ADD/ADD%20Step%201:%20%20Review%20Inputs.md)

**Step 2: Establish iteration goal by selecting drivers**


In the second iteration, besides CRN-1 (Create and define the overall system), we are considering the system’s primary use cases:
 * UC-1: User system with specified roles
 * UC-4: Synchronize User information with university database information


**Step 3: Choose one or more elements of the sytem to refine**


  The elements that will be refined in this iteration would be the bottom layered or the server and database side of the system. In general, the support of the functionality in this system requires the collaboration of components associated with modules that are located in the different layers
  
  
**Step 4: Choose one or more design concept that satisfy the selected drivers**

| Design Decisions and Location                               | Rationale and Assumptions                                                                                                                                                                                                                                                                                                       |  
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Create a Domain Model for the application                   | Before we start functional decomposition, it’s necessary to create an initial domain model for the system, to identify the major entities in the domain.  Since there are no good alternatives, a domain model must be made or it will be created in least optimal manner which in turn will be hard to maintain and understand |
| Identify Domain Objects that map to functional requirements | Each distinct functional element of the application needs to be encapsulated in a self-contained building block - a domain object.  Directly composing layers increases the risk of not considering a requirement                                                                                                               |
| Decompose Domain Objects into layered components            | Domain objects represent complete sets of functionality, but this functionality is supported by finer-grained elements located within the layers. The “components” in this pattern are what are referred to as modules                                                                                                          |

**Step 5: Instantiate architectural elements, allocate responsibilities, and define interfaces**

| Design and decision location                                                                                 | Rationale and assumption  |
|-----------------------------------------------|-------------------|
| Create only an initial domain model          | The entities that participate in the primary use cases need to be identify and modeled but only an initial domain model is create in order to accelerate the design phase |      
| Map the system use cases to domain objects               | Analyzing the system's use case allows us to identify the domain objects. To address the CRN-3 we identify the domain objects shown in the deliverable 1.         |
| Decompose the domain objects across the layers to identify layer-specific modules with an explicit interface | This technique ensures that modules that support all of the functionalities are identified. The architect will perform this task for the primary use cases mentioned in step 2. After establishing the set of modules the architect realizes that the need to test these modules also satisfy the concern: CRN-4- Most modules should be tested |
| Connect components associated with modules| This framework uses an inversion of control approach that allows different aspects to be supported and the modules to be tested  The framework also allows for accuracy checks and safety checks between modules and components (CRN-4)                 
| Associate frameworks with a module in the data layer     | ORM mapping is encapsulated in the modules that are contained in the data layer |



**Step 6: Sketch views and record design decisions**

![alt Initial Domain Model](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%202/InitialDomainModel.PNG)   

*Figure 2.1: Initital Domain Model*

![alt Domain Objects](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%202/DomainObjectsAssociatedWithUseCases.PNG)   

*Figure 2.2: Domain Objects Associated with Use Cases*

![alt Primary Use Case Modules](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%202/PrimaryUseCaseSupportModules.PNG)   

*Figure 2.3: Modules that support primary use cases*

The following table summarizes the elements in Figure 2.3:

| Element                   	| Responsibility                                                                                              	|
|---------------------------	|-------------------------------------------------------------------------------------------------------------	|
| RequestManager            	| Gets users request from the web client via the user interface                                               	|
| RequestService            	| The users request is handled by the request service on the server which connects the client with the server 	|
| ProcessRequest            	| Server processes the users request                                                                          	|
| RequestHandler            	| Handles the request through business logic of server                                                        	|
| DatabaseConnector         	| Responsible for connection between server and database                                                      	|
| DatabaseMapper            	| Map persistent data stored in database to operations needed to perform users request                        	|
| UniversitySystemConnector 	| Responsible for connection between server and other university systems                                      	|
| UniversitySystemMapper    	| Map data operations from secondary university systems to perform users request    


**Use Case 1: Account System**<br>
The next diagram is a sequence diagram which shows how the user will access the system based on their role within the system. Once the user launches the browser, they will be prompted for account credentials which they will use to login into the system. The account they logged into will tied to a specific role in the system which will define their permissions and access to the system.


![alt Use Case 1 Sequence Diagram](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%202/UC-1.PNG)   

*Figure 2.4:  Sequence Diagram for UC-1*

**Use Case 4: Record System**<br>
The next diagram is a sequence diagram that shows how the user will access system records within the course management. Once the users role is determined from the steps in the previous diagram, the user will be able to request information from the server. The server will respond based on the accounts role and the information they request. The user will only be prompted with available information for their specific role.


![alt Use Case 4 Sequence Diagram](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%202/UC-4.PNG)   

*Figure 2.5:  Sequence Diagram for UC-4*

**Step 7: Perform analysis of current design and review iteration goal and achienvement of design purpose**

| Not Addressed | Partially Addressed | Completely Addressed | Design Decisions Made during the Iteration                                                                                                                                                                |
|---------------|---------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|               |                     | UC-1                 | User systems are implemented through an account system which defines permissions of account based on their roles. Implementation of this through the web application will be held through server sessions |
|               |                     | UC-2                 | Information to be displayed will be decided on based on accounts role(permissions) through previously defined web technologies rendered from the server in the users client                               |
|               | UC-4                |                      | Records and files will be stored within the systems database and accessed through server protocols based on user requests and permissions                                                                 |
|               | UC-7                |                      | Differing account permissions will allow users to access and modify content based on their role in the system                                                                                             |
|               | QA-1                |                      | No relevant decisions made                                                                                                                                                                                |
|               | QA-2                |                      | Permission within the system will allow for system modification                                                                                                                                           |
|               |                     | QA-4                 | The system will restrict data access and modification based upon the users account permissions                                                                                                            |
|               |                     | QA-5                 | The usability of the system will be tightly related to account permissions                                                                                                                                |
|               | CON-1               |                      | System modification will be only accessible through accounts holding permissions for modifications                                                                                                        |
|               |                     | CON-2                | Data storage and retrieval will be implemented through the systems database through fetches on the server based on user requests                                                                          |
|               |                     | CON-3                | No relevant decisions were made                                                                                                                                                                           |
|               | CON-5               |                      | The server will act as middleware between the client and the database synchronizing the clients requests with the relevant data                                                                           |
|               |                     | CON-6                | No relevant decisions were made                                                                                                                                                                           |
|               | CON-7               |                      | Administration accounts will hold permissions to modify the system                                                                                                                                        |
|               | CRN-1               |                      | Additional technologies and architectures were selected to advance the systems overall structure                                                                                                          |
|               | CRN-3               |                      | No relevant decisions were made                                                                                                                                                                           |
|               |                     | CRN-4                | The system checks the relationship between components and modules for safety and security                                                                                                                 |




















