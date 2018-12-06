# Use Cases


| Use Case | Name                                | Requirements                              | Explanation                                                                                                        |
|----------|-------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| 1        | Account system                      | Roles                                     | Allows the system to handle request based upon the users role                                                      |
| 2        | Display User's information           | 1-7, 19, 20                               | Displays information on the web application (UI)                                                                   |
| 3        | Allows for system modifiability     | 8, 21-23, 48-50, 68, 70-72, 74-77, 79, 82 | Allows for the system's program to change accordingly based changes to the system variables by differing roles      |
| 4        | Student's files/ record              | 9-18, 53                                  | Records holding the students progress in school and their activities, including school information such as courses |
| 5        | Grades/ marks inputted              | 26, 73, 80, 81                            | Records the students marks given the lecturer                                                                      |
| 6        | Calculations of grades              | 54, 110-116                               | Calculations of lump sum of the students marks                                                                     |
| 7        | Allows the admin to bypass policies | 52                                        | Enables admins to work against policies setted                                                                     |
| 8        | Software backup                     | 88, 89                                    | Allows for the program to backup in case of emergency                                                              |
| 9        | System constraints                  | 55-58, 60-65, 90, 91                      | Stops system from overloading and/or crashing                                                                      |
| 10       | Student evaluation                  | 59, 117                                   | Allows for unbiased communication                                                                                  |
| 11       | User registrations                  | 51, 78                                    | Allows system to add more data into its database                                                                   |
| 12       | Security                            | 66                                        | Protects entire system from malware or viruses, and protects from unauthorized user access                         |
| 13       | Announcement/notice                 | 24, 25, 67, 69                            | Displays' system's notifications, lecturers notifications, admin's notifications                                      |

# Quality Attributes

| Quality Attributes | Scenario                                                                                                  | Associated Use case |
|--------------------|-----------------------------------------------------------------------------------------------------------|---------------------|
| 1- Availability    | Notice of system maintenance, ease of access to the system                                                | All                 |
| 2- Modifiability   | Allows Users to alter/ change the system easily and allows the system to easily be updated (Backup)       | 2, 3, 4, 5, 6, 7    |
| 3- Performance     | Response time and allows for multiple events to occur at the same time                                    | All                 |
| 4- Security        | Provides confidential information allowing only certain stakeholders to view, change, add or remove       | All                 |
| 5- Usability       | Allows anyone and/or everyone to access with ease and provides users with an easy way of using the system | All                 |

# Constraints


| Constraints | Explaination                                                              |
|-------------|---------------------------------------------------------------------------|
| CON-1       | System must be able to be modified                                        |
| CON-2       | System must be able to deliver and store precise information              |
| CON-3       | System must be user friendly                                              |
| CON-4       | System must satisfy certain policies given                                |
| CON-5       | System must be able to safely synchronize with other databases            |
| CON-6       | System must be able to adapt to multiple systems                          |
| CON-7       | System must be able to be altered/ changed according to the administrator |
| CON-8       | System must contain limits and boundaries accordingly                     |

# Concerns

| ID    | Concern                                                       |
|-------|---------------------------------------------------------------|
| CRN-1 | Creation of initial system structure                          |
| CRN-2 | Work allocation among members of development team             |
| CRN-3 | Utilize knowledge of Web technologies to implement the system |
| CRN-4 | Modules should be tested                                      |

# Use case Diagram

