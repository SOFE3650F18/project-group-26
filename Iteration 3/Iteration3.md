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

                            
