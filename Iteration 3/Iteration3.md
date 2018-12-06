# Iteration 3

**Step 1: Review Inputs**

 [Add Step 1: Review Inputs](https://github.com/SOFE3650F18/project-group-26/blob/master/ADD/ADD%20Step%201:%20%20Review%20Inputs.md)

**Step 2: Establish iteration goal by selecting drivers**

  For this iteration, we are focusing on QA-1: availability- Notice of system maintenance, ease of access to the system. Problem with certain programming languages or operating system due to precise programming. The management system will enable for usage and enables other platform to use

**Step 3: Choose one or more elements of the sytem to refine**

  For this availability scenario, the elements that are being refined would be the client side and the server side mentioned in the first iteration

**Step 4: Choose one or more design concept that satisfy the selected drivers**

| Design Decisions and location                                            | Rationale and Assumption                                                                                                                     |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Introduce the active redundancy tatic by replicating the database server | By replicating the critical elements, the system can withstand the failure of one of the replicated elements without affecting functionality |
| Introducing a running time                                               | By continuously running server side at a minimal and accessing it from the client side when called                                           |
| Alternative versions/platforms                                           | Web application available for different types of platforms (MacOS, Linux, windows, android, IOS)(QA-1)                                       |

**Step 5: Instantiate architectural elements, allocate responsibilities, and define interfaces**

| Design decisions and location                                                                                               | Rationale                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Implement software element to backup system data                                                                            | Implementation of a backup system will allow the system to restore from a backup image if an issue occurs which causes the server process to be interrupted or hit a fatal error. This will allow the server process to be restored with information loss(UC-8). |
| Introduce active redundancy tactic by replicating the application server and other critical components such as the database | The implementation of replicated application servers and critical components will allow for system backup and prevent the loss of critical components (UC-8).                                                                                                    |
| Use active redundancy and load balancing in the application server                                                          | A load balancer can be used to route users to different instances of the replicated servers to reduce stress on a single server. This tactic can be used to achieve Load-Balanced Cluster pattern to relieve server stress.                                      |
| Implement load balancing and redundancy using technology support                                                            | There are many technology options for load balancing and redundancy which can be implemented without having to develop an ad hoc solution                                                                                                                        |

**Step 6: Sketch views and record design decisions**

The following deployment diagram shows the implementation of replicated servers with active redundancy and load balancing

![alt Deployment Diagram](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%203/deployment.PNG)   

*Figure 3.1: Refined Deployment Diagram*

![alt Sequence Diagram](https://github.com/SOFE3650F18/project-group-26/blob/master/Iteration%203/UC-8%20Sequence%20Diagram.png)

*Figure 3.2: Sequence diagram visually showing the interaction between a backup server and the main server (UC-8)*

**Step 7: Perform analysis of current design and review iteration goal and achienvement of design purpose**

| Not Addressed | Partially Addressed | Completely Addressed | Design Decisions Made during the Iteration                                                                                                                      |
|---------------|---------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
|               |                     | UC-1                 | No relevant decisions made                                                                                                                                      |
|               |                     | UC-2                 | No relevant decisions made                                                                                                                                      |
|               |                     | UC-4                 | Records and files will be replicated among multiple servers to address issues of data loss server errors                                                        |
|               | UC-7                |                      | No relevant decisions made                                                                                                                                      |
|               |                     | UC-8                 | Visualization of the use case; implementation of its response and request interaction between the backup server and the web server                              |
|               |                     | QA-1                 | Implementation of new technologies to allow the increase in availability of services through the use of load balancing, active redundancy and backups           |
|               | QA-2                |                      | No relevant decisions made                                                                                                                                      |
|               | QA-3                |                      | The implementation of load balancing and replicated servers will increase performance by distributing traffic among multiple servers to relieve the server load |
|               |                     | QA-4                 | No relevant decisions made                                                                                                                                      |
|               |                     | QA-5                 | Increase in usability through implementation of backup servers as well as load balancing to reduce signs of stress on the server by the user                    |
|               | CON-1               |                      | No relevant decisions made                                                                                                                                      |
|               |                     | CON-2                | No relevant decisions made                                                                                                                                      |
|               |                     | CON-3                | No relevant decisions made                                                                                                                                      |
|               |                     | CON-5                | The server will be able to synchronize with backup servers in the case of major issues                                                                          |
|               |                     | CON-6                | Introduced a variety of software platforms and web clients, the server will be able to adapt differing functionality                                            |
|               | CON-7               |                      | No relevant decisions were made                                                                                                                                 |
|               |                     | CRN-1                | Additional technologies and architectures were selected to advance the systems overall structure                                                                |
|               | CRN-3               |                      | Implementation of a backup server in order to safely achieve new technology (QA-1)                                                                              |
|               |                     | CRN-4                | No relevant decisions were made                                                                                                                                 |
                            
