
**Step 1: Review Inputs**

 

**Step 2: Establish Iteration Goal by Selecting Drivers**

  The main iteration goal of this section is CRN-1, to create and define the overall system structure. This iteration is driven by general architecture of the system, but all drivers in step 1 are being considered as influence within this iteration as it will create the underlying structure of the system.

**Step 3: Choose One or More Elements of the System to Refine**



**Step 4: Choose One or More Design Concepts That Satisfy the Selected Drivers**



**Step 5: Instantiate Architectural Elements, Allocated Responsibilities and Define Interfaces**

**Step 6: Sketch Views and Record Design Decisions**

| Element                  | Responsibility |                                                                                           
|--------------------|----------------------|
| Presentation CS          | This layer controls the flow and the user input (User interface)  |                               
| Business logic CS        | This layer performs operations based on business operations   |                                              | Cross-cutting CS         | "This layer access different modules across the CS in order to provide security logging and I/O files" |   
| UI module                | This module displays user's inputs |                                                             
| UI Process modules       | This module controls the flow of the user's input |                    
| Business modules CS      | This module controls the user input with relation to the Business |            
| Business entities CS     | This module is the foundation of the client side contains all interfaces required for the user |         
| Communication modules CS | This module provides services and connections between the client side and the server side|          
| Services SS              | This layer interacts with the client side and opens up the server side for the client side to use|    
| Business logic SS        | This layer performs logical operation based on the client side business layer|                            
| Data SS                  | This layer is responsible for containing data and for returning data we asked for|                        
| Cross- cutting SS        | "This layer access different modules across the SS in order to provide security logging and I/O files" |
| Service interface SS     | This module takes input from the client side and organizes it in the server side| 
| Business modules SS      | This module implements operations |    
| Business entities SS     | This module is made up of entities |           
| DB access module         | This module is responsible for the storing of data and its relational information as well as protecting valuable data |

**Step 7: Perform Analysis of Current Design and Review Iteration**

