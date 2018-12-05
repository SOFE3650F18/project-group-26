**Step 2: Establish iteration goal by selecting drivers**

**Step 3: Choose one or more elements of the sytem to refine**

**Step 4: Choose one or more design concept that satisfy the selected drivers**

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

*Figure: Refined Deployment Diagram*

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
                            
