# <ins>Introducrion</ins>

In the Agile Development Design (ADD) process, Iteration 1 serves as the foundational phase, focusing on defining project scope, identifying key requirements, and establishing a basic development framework. It sets the groundwork for subsequent iterations, providing clarity on project goals and ensuring a solid foundation. Iteration 2 follows, building upon the initial work by further developing features, addressing issues, and refining the project structure based on feedback from the first iteration. This iterative approach is integral to Agile methodologies, emphasizing incremental progress, a feedback loop for continuous improvement, adaptability to changing requirements, and early risk mitigation. Each iteration contributes to the overall project evolution, allowing teams to respond to emerging insights and stakeholder feedback, ensuring a more flexible and resilient development process.

# Iteration 1
### Step 1 - Review Inputs
| Category | Details |
|---|---|
| Design Purpose | This is a greenfield system from a mature domain |
| Primary Functional Requiremenst | UC-1: Login (A User logs into the system after entering User ID/password. Upon successful login, the user is given appropriate permissions), UC-4: Course Enrolment (Student Selects course and is able to subscribe/unsubscribe and view course information), UC-7: Create Course (Lecturers create courses and sent to the administration for confirmation), UC-13: Search (Users enter course codes or name into the system, system replies with courses that match the input) |
#### Quality Attribute scenarios
|Scenario ID| Importance to User| Diccuulty of Implementation|
|---|---|---|
|QA-1|High|Easy|
|QA-2|High|Hard|
|QA-3|High|Medium|
|QA-4|High|Easy|
|QA-5|Medium|Easy|
|QA-6|Low|Hard|

QA-1, QA-2, QA-3 are included as drivers
#### Constraints
| ID | Constraint |   
|---|---|
| CON-1 | The system should be easily verifiable, capable of scaling, and straightforward to maintain |
| CON-2 | The system must have bilingual support |
| CON-3 | Access to the system should be possible through contemporary web browsers across various operating systems |
| CON-4 | The system should include a mobile version accessible on both Android and iOS platforms |
| CON-5 | The system must ensure that users can access any content within a maximum of three clicks |
#### Architectural Concerns
### Architectural Concerns
| ID | Concern |
|---|---|
| CRN-1 | Setting up the initial structures for the overall system |
| CRN-2 | Utilize the collective expertise of teams in various programming languages |
| CRN-3 | Allocate work to developement team |

### Step 2 - Establish Iteration Goal by Selecting Drivers
The iteration goal is to achieve CNR-1  
![image](https://github.com/SOFE3650F23/project-delivery-1-gp-31/assets/145510715/509e9189-ac70-4a73-b72c-74047a76d003)



### Step 3 - Choose one or more Elements to refine
The element to refine is the entire CMS system, this is due to the fact that the system to be developed is a greenfield system

### Step 4 - Choose one or more design concepts to work with
| Design Decisions and Location | Rationale |
|---|---|
| Organize the client component of the system logically by employing a web application framework |The selection was made because web applications are simpler to create, readily available across various devices, scalable, and easy to maintain  |
| Logically structure the server part of the system using service application | This was chosen due to the fact that the alternatives would not meet the requirements when it comes to service applications  |
| Physically structure the application using the three tiered deployment pattern | Due to the fact that the system involves a user accessing a browser and through that to access a data base it was found that the three tier deployment pattern is ideal |

### Step 5 - Instantiate Architectural Elements, Allocate Responsibilities
| Design Decisions and Location | Rationale |
|---|---|
| Create a user interface | This will help the completion of QA-1 |
| Create a module dedicated to accessing time servers | This will help the completion of QA-3 |
| Create a database to store course information | This will help the completion of QA-1 and QA-2 |

### Step 6 - Sketch Views and record design decisions

__<ins>Layer</ins>__

![image](https://github.com/SOFE3650F23/project-delivery-1-gp-31/assets/145510715/20d699b2-9f17-4fce-ab67-b3abfa372e86)

__<ins>The following table breaks down the elements and responsibilities of the diagram:</ins>__

| Element | Responsibility |
|---|---|
|Client Presentation| This layer encompasses the modules that manage the user interface|
|Business Logic CS| This layer houses the modules that execute client-side business logic|
|Data Layer CS| Within this layer are the modules responsible for interfacing with the server|
|Browser| This layer facilitates user interaction|
|Browser Process Module| This module oversees the control flow of the system|
|Login CS| This layer contains a module utilized for client-side login functionality|
|Search CS| This layer hosts a module employed for course searching on the client side|
|Create CS| This layer includes a module used for course creation on the client side|
|Communication Module| This module is employed to establish connectivity between the client side and the server side|
|Services SS| This layer consists of modules that manage interactions with the server|
|Business Logic SS| Modules within this layer handle server-side business logic|
|Data Layer SS| This layer encompasses modules responsible for data access and communication with the time server|
|Service Interface| This interface allows server modules to interact with the client side|
|Login SS| This layer comprises a module used for server-side login functionality|
|Search SS| This layer includes a module used for course searching on the server side|
|Create SS| This layer contains a module used for course creation on the server side|
|Access Module| This module ensures correct access to the database|
|Time Server Access Module| This module is responsible for communicating with the time servers|
|Security| Ensures the security of the server side|
|Operation Management Module| This module ensures proper handling of client-side operations|

__<ins>Deployment Diagram</ins>__

![image](https://github.com/SOFE3650F23/project-delivery-1-gp-31/assets/145510715/b1927120-a25c-400c-be33-92d1239bfda2)

__<ins>The following table breaks down the elements and responsibilities of the diagram:</ins>__

| Element | Responsibility |
|---|---|
|User Workspace| The users device that accesses the client side logic of the website|
|Application Server|Hosts the server side logic of the web application|
|Database Server| Contains the relation database of the system|
|Time Server| External Time Servers|

__<ins>The relationships and their descriptions:</ins>__

| Relationship | Description |
|---|---|
| Between Application Server and Database server|  Communication with the data base will be conducted using MySQL|
|Between Application Server and Time Server| Uses the Simple Network Management Protocol (SNMP) | 


### Step 7 - Perform Analysis of current Iteration

The Following Table summarizes the design procress in this iteration

|Not Addressed| Partially Addressed|Completly Addressed|Design Made during Iteration|
|---|---|---|---|
| | UC-1 | | The chosen reference architecture includes modules supporting this functionality |
| | UC-4 | | The selected reference architecture incorporates modules for supporting this functionality |
| | UC-13 | | The chosen reference architecture provides modules to support this functionality |
| | UC-7 | | Modules supporting this functionality are integrated into the selected reference architecture |
| | QA-1 | | Introduction of a browser module for communicating account details with the user |
| | QA-2 | | Introducing an access module for communication with the database enables course creation |
| | QA-3 | | Introduction of Time server module and access module for creating backups |
| | | CON-1 | Structuring the system with the three-tier architecture allows developers to adapt, update, and maintain without impacting other areas of the application |
| CON-2 | | | No relevant decision was made |
| | | CON-3 | The selected reference architecture provides compatibility and accessibility on any device |
| | | CON-4 | The selected reference architecture does not cater to mobile apps for Android and iOS devices, as the system can be accessed with only an internet connection |
| CON-5 | | | No relevant decision was made |
| | | CRN-1 | Selection of reference architecture and deployment pattern |
| | CRN-2 | | Modules that have been considered require knowledge from developers |
| CRN-3 | | | No relevant decision was made |


# Iteration 2
### Step 1 & 2 - Establish Iteration Goal by Selecting Drivers

The goal of this iteration 2 is to address the gengeral architectural concerns to support primary functionality of CMS
The primary Use Cases will be considered in this iteration are:

| Use Cases  | Use case description |
| ------------- | ------------- |
| UC-1: Login  | A User logs into the system after entering User ID/password. Upon successful login, the user is given appropriate permissions  |
| UC-4: Course Enrolment  | Student Selects course and is able to subscribe/unsubscribe and view course information  |
| UC-7: Create Course   | Lecturers create courses and sent to the administration for confirmation  |
| UC-13: Search  | Users enter course codes or name into the system, system replies with courses that match the input  |

### Step 3 - Choose One of More Elements of the System to Refine

The elements of system that this iteration will refine are the modules identified in the reference architectures in the previous interation

### Step 4 - Choose One of More Design Concepts That Satisfy the Selected Drivers
|Design Decisions and Location|Rationale and Assumptions|
|---|---|
|Create a Domain Model for the application| Creating a domain model will illustrate and identifity the important entities and relastionships in the system |
|Identifiy domain objects of function requirements| Each distinct Functional object will be encapsulated in a domain object|
| Convert Domain Objects into Components | Domain objects represent a set of Functional objects |

### Step 5 - Instantiate the Architectural Elements, Allocate Responsibilities and Define Interfaces
|Design Decisions and Location|Rationale|
|---|---|
| Create a initial domain model | The entities that relate to the use cases will be indentified and modelled, to create a initial domain model |
| Map the domain objects to the use cases| Analyze the use cases to find which domain objects are in relation to which use case |
| Place domain objects in the different layers of the system | This will be done to insure that the functionalities of each module is identified and that the module is placed in the correct layer of the system |
| Associate Modules to the data layer | Mapping the modules to the data layer encapsulating the functionality |
### Step 6 - Sketch Views and Record Design Decisions

__<ins>Domain:</ins>__

![image](https://github.com/SOFE3650F23/project-delivery-1-gp-31/assets/145510715/9d7fa8c2-b1eb-4c59-8776-e452f9a71cac)

__<ins>The following table breaks down the elements and responsibilities of the diagram:</ins>__

|Element|Responsibility|
|---|---|
|User| User login interface|
|WebClient| Specific User Interface loaded for different types of Users( Student,Lecturer,Administrator)|
|WebServer| Backend Services of the web application, responisble for handling security, hanlding time, and handling user inputs|
|Database|Stores Data|
|Security| Insures application is secure and user type and permissions are valid|

__<ins>Layer B:</ins>__

![image](https://github.com/SOFE3650F23/project-delivery-1-gp-31/assets/145510715/005e0b0c-ac48-41e4-b26d-5682d352f90b)

__<ins>The following table breaks down the elements and responsibilities of the diagram:</ins>__

|Element|Responsibility|
|---|---|
|BrowserUI|Encompasses the entire frontend of the web application, including the login interface and the Web Client interface|
|BrowerUIController|Handles the acquisition of user input data and supplies the presentation layer with necessary information|
|Request Manager|Manages communication with the server side|
|Request Services|Receives requests from the client side|
|Login Controller|Manages business logic pertaining to user logins|
|Course Controller|Manages business logic related to searching, course creation/deletion|
|AccessModule|Handles data access based on controllers in the Business Logic Server Side|
|TimeServer|Manages persistent operations related to time servers|
  
__<ins>UC-1 - Login:</ins>__
The below diagram shows the sequence of components for UC-1 where the user logs in to the system  
![image](https://github.com/SOFE3650F23/project-delivery-1-gp-31/assets/145510715/30d94b12-31a7-4eaf-9430-f7642cc6d5a2)

Browser UI  
* Boolean Initilize() - Opens the network representation so the user can interact with it  
* Validity DisplayLogin() - returns a page based on the validity of the login  

BrowserUIController  
* Validity Login(User,Pass) - Returns the reference based on the user input  

RequestManager 
* Response SendRequest() - Request the login validity from the root region  

RequestService  
* Validity requestLogin(User,Pass) - This method recieves a request, and access the service interface  

LoginController  
* Validity ValidId() -  returns the validity of the login based on the info given    

__<ins>UC-7 - Create Course:</ins>__
The below diagram shows the sequence of components for UC-7 where the user creates a course  
![image](https://github.com/SOFE3650F23/project-delivery-1-gp-31/assets/145510715/20ff5b99-0a32-432f-b222-676517d7a46c)

Browser UI  
* Boolean Initilize() - Opens the network representation so the user can interact with it  
* Boolean createcourse(course) - returns a page based on the updated courses  

BrowserUIController  
* Boolean createcourse(User,Pass) - Returns the reference based on the user input  

RequestManager 
* Response SendRequest() - sends the course info to be added  

RequestService  
* Boolean createcourse(User,Pass) - This method recieves a request, and access the service interface  

CourseController  
* Boolean addcourse() -  returns the whether a course was succesfully added

__<ins>UC-13 - Search:</ins>__
The below diagram shows the sequence of components for UC-13 where the user searchs for a course 
![image](https://github.com/SOFE3650F23/project-delivery-1-gp-31/assets/145510715/a1248344-50e6-4be1-adf5-98cee437e7c1)

Browser UI  
* Boolean Initilize() - Opens the network representation so the user can interact with it  
* SearchResults search() - returns a page based on the search results 

BrowserUIController  
* SearchResults search() - Returns the reference based on the user input  

RequestManager 
* Response SendRequest() - Request the a search of the courses  

RequestService  
* SearchResults requestSearch(User,Pass) - This method recieves a request, and access the service interface  

CourseController  
* SearchResults searchCourse() -  returns the course that is the result of the search

### Step 7 - Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose
|Not Addressed| Partially Addressed|Completly Addressed|Design Made during Iteration|
|---|---|---|---|
| | | UC-1 | Modules spanning layers and the initial interfaces to support this use case have been identified |
| | | UC-4 | Modules across layers and the preliminary interfaces to support this use case have been recognized |
| | | UC-13 | Modules across layers and the preliminary interfaces to support this use case have been pinpointed |
| | | UC-7 | Modules across layers and the preliminary interfaces to support this use case have been identified |
| | QA-1 | | The components supporting the associated use case have been identified |
| | QA-2 | | The elements supporting the associated use case have been identified |
| | QA-3 | | The elements supporting the associated use case have been identified |
| CON-2 | | | No pertinent decisions were made |
| CON-5 | | | No relevant decisions were made |
| | CRN-2 | | Knowledge of developers is required for the new modules under consideration |
| CRN-3 | | | No relevant decision was made |

