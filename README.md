
# <ins>1.0 Introducrion</ins>

__1.1. Brief Overview of ADD Iteration 1:__

The Attribute-Driven Design (ADD) method is a systematic approach to designing software architectures. In this first iteration of ADD, we focus on the principal use case, laying the groundwork for the architectural foundation of the Course Management System (CMS).

__1.2. Purpose and Significance of the Iteration:__

This iteration serves as the initial step in our architectural design process. By concentrating on a principal use case, we ensure that the core functionalities and interactions of the CMS are welldefined and robust. This foundational work is pivotal for subsequent iterations and the overall success of the project.

__<ins> 2. Principal Use Case Selection</ins>__

__2.1. Criteria for Selection:__

The principal use case was selected based on:

• Its centrality to the system's core functionality.

• The number of actors involved.

• Its potential impact on system performance and user experience.

__2.2. Chosen Principal Use Case Description:__

| Use Case  | Actors | Description |
| ------------- | ------------- | -----------|
| Course Enrollment  | Students, Administrators  | This use case allows students to enroll in or drop out of courses. Administrators can also manually enroll or remove students from courses.|

__2.4 Design Decision for Iteration 1:__

| Design Decision   | Justification |
| ------------- | ------------- |
| Three-Tier Architecture  | Facilitates scalability, modularity, and a clear separation of concerns. Ideal for web-based applications.  |
| Microservices for Application Server  | Enhances scalability and ease of maintenance. Allows independent development and deployment of services.  |
| RESTful APIs for Integration  | Ensures easy integration with external systems and third-party services. Promotes interoperability.  |
| Database Replication and Sharding  | Improves data availability and load distribution. Enhances performance and reliability.  |
| CI/CD Pipelines   | Enables efficient deployment and updates of system components. Supports agile development practices.  |
| Regular Data Backups and Disaster Recovery Plan  | Protects against data loss and ensures system availability in case of major incidents.  |
| Comprehensive Logging and Monitoring  | Facilitates troubleshooting and auditing. Ensures system health and performance tracking.  |
| GDPR Compliance and Robust Access Control  | Ensures data protection and privacy. Safeguards sensitive information.  |

__2.5 Design Decision for Iteration 2:__

| Design Decision   | Justification |
| ------------- | ------------- |
| Performance Optimization Techniques  | Improves system response time and efficiency. Enhances user experience  |
| Advanced Security Measures  | Strengthens system security to protect against evolving threats. Ensures data integrity and confidentiality  |
| User Interface Enhancements  | Improves usability and accessibility. Ensures a better user experience  |
| Scalability Improvements  | Prepares the system for future growth in users and data. Ensures system stability under increased load  |
| Integration of Analytics and Reporting Tools   | Provides insights into system usage and performance. Supports data-driven decisionmaking  |
| Enhanced Testability and Quality Assurance  | Ensures the reliability and correctness of the system. Facilitates easier maintenance and updates  |
| Compliance with Additional Standards and Regulations  | Ensures adherence to industry standards and legal requirements. Enhances trust and credibility  |
| Implementation of Feedback Mechanisms  | Allows for continuous improvement based on user feedback. Enhances user satisfaction and engagement  |

__2.6 Analysis of the Design Decisions for Iteration 1:__

| Design Decision   | Analysis | Progress Status |
| ------------- | ------------- | ------ |
| Three-Tier Architecture  | Chosen for its scalability and clear separation of concerns. Ideal for web applications.  | Complete |
| Microservices for Application Server  | Enhances system scalability and maintenance. Allows for independent service updates  | In Progress |
| RESTful APIs for Integration  | Facilitates easy integration and promotes interoperability.  | Complete |
| Database Replication and Sharding  | Improves data handling and system performance  | In Progress |
| CI/CD Pipelines   | Supports agile practices and efficient system updates.  | Complete |
| Regular Data Backups and Disaster Recovery Plan  | Essential for data integrity and system resilience.  | Complete |
| Comprehensive Logging and Monitoring  | Crucial for system health tracking and troubleshooting.  | Complete |
| GDPR Compliance and Robust Access Control  | Ensures data privacy and security. | Complete |

__2.7 Analysis of the Design Decisions for Iteration 2:__

| Design Decision   | Analysis | Progress Status |
| ------------- | ------------- | ------ |
| Performance Optimization  | Aims to enhance system efficiency and user experience  | In Progress |
| Advanced Security Measures  | Addresses evolving security threats and protects data  | In Progress |
| User Interface Enhancements  | Focuses on improving usability and accessibility  | In Progress |
| Scalability Improvements  | Prepares the system for future growth and stability  | In Progress |
| Analytics and Reporting Tools   | Provides valuable insights for datadriven decisions  | In Progress |
| Testability and Quality Assurance  | Ensures system reliability and correctness  | In Progress |
| Compliance with Additional Standards  | Adheres to industry standards and legal requirements  | In Progress |
| Feedback Mechanisms  | Facilitates continuous improvement based on user input | In Progress |

__<ins>3. ADD Iteration 1 Artifacts</ins>__

__<ins>3.1. Reference Architecture</ins>__

__3.1.1. Overview:__

Three tiers—the Presentation, Logic, and Data tiers—make up the CMS's selected reference design. Scalability, modularity, and a distinct separation of concerns are supported by this design.

__3.1.2. Justification for Choice:__

Web-based applications such as the CMS are a good fit for the three-tier design. It permits:

__• Scalability:__ Can easily handle an increasing number of users.

__• Flexibility:__ Each tier can be developed and scaled independently.

__• Security:__ Sensitive data in the Data tier is isolated from the Presentation tier.

__<ins>3.2. Deployment Diagram</ins>__

__CMS Deployment Diagram:__

![image](https://github.com/Muji90/Assignment-1-Design-Patterns/assets/145510715/4cdaab35-1809-4138-af5f-31d25ad6b31a)

__Application Deployment Diagram:__

![image](https://github.com/Muji90/Assignment-1-Design-Patterns/assets/145510715/b8535750-ee1e-4654-b8d9-fb20db69c542)

__3.2.1. Overview of the Deployment Structure__

The Web Server (Presentation Tier), Application Server (Logic Tier), and Database Server (Data Tier) are the three primary servers on which the CMS is installed.

__3.2.2. Components and Their Interactions__

| Components  | Interactions |
| ------------- | ------------- |
| Web Server  | Hosts the CMS's user interface. Reaches out to the Application Server in order to receive or send data  |
| Application Server  | Includes the business reasoning. Communicates with the Database Server, processes requests from the Web Server, and returns information  |
| Database Server  | Retains grades, user information, course information, and other pertinent data  |

__3.2.3. Security and Performance Considerations__

__• Web Server Security:__ To ensure secure data transfer, use SSL/TLS. To prevent unwanted access, make use of intrusion detection systems and firewalls.

__• Load Balancing:__ Use load balancers to split up traffic across servers in an equitable manner, guaranteeing great dependability and availability.

__• Caching Mechanisms:__ To enhance response speeds and lessen the strain on the Application Server, use caching on the Web Server.

__<INS>3.3. Major Components of the Architecture</INS>__

__3.3.1. Component Descriptions and interactions:__

| Component  | Descriptions | Interactions |
| ------------- | ------------- | -----------|
| User Interface (UI) Component | Gives consumers access to an interactive interface. Includes sites for managing profiles, examining grades, and enrolling in courses.  | Gathers and presents data, interacts with the Business Logic Component, and records user input |
| Business Logic Component  | Manages data operations, applies business rules, and processes user requests  | Checks for accuracy, handles user input, and communicates with the Data Access Component |
| Data Access Component  | Ensures safe and effective data operations via interfaces with the database  | Handles database CRUD (Create, Read, Update, Delete) actions and provides the Business Logic Component with the results |

__3.3.2. Scalability and Maintenance__

__• Microservices Architecture:__ For the Application Server, thinking about using a micro services architecture to improve scalability and maintenance-friendliness.

__• Database Replication:__ For better data availability and load dispersion, use database replication and sharding.

__• Continuous Integration/Continuous Deployment (CI/CD):__ For effective system component changes and deployment, use CI/CD pipelines.

__3.3.3. Integration and Extensibility__

__• APIs for Integration:__ Create RESTful APIs for the Application Server to help with third-party service or external system integration.

__• Modular Design:__ Make sure the business logic and user interface are modular so that you can simply add more features or modify them later.

__3.3.4. Disaster Recovery and Data Backup__

• Regular Backups: To avoid data loss, do regular backups of the database server.

• Disaster Recovery Plan: Create a disaster recovery strategy to guarantee data integrity and system availability in the event of significant events.

__3.3.5. Monitoring and Logging__

__• System Monitoring:__ Track each server's health and performance using monitoring tools.

__• Logging:__ Establish thorough logging for auditing and troubleshooting needs.

__3.3.7. Compliance and Data Privacy__

__• Data Protection:__ When processing user data, make sure that data protection laws like the GDPR are followed.

__• Access Control:__ To protect sensitive data, put strong access control measures in place in the business logic component.

__<ins>3.4. Interface Specification</ins>__

__3.4.1. Internal Interfaces__

__• UI to Business Logic Interface:__ outlines the protocol for communication between the levels of business logic and user interface. This covers error-handling procedures, request/response data structures, and RESTful API endpoints.

__• Business Logic to Data Access Interface:__ describes the data formats and querying techniques for updating and querying the database. Data integrity restrictions, transaction management, and database query interfaces are all included in this.

__3.4.2. External Interfaces__

__• Third-Party Integration APIs:__ Describes the interfaces for integrating external services, such as authentication providers, email services, or analytics tools. This includes API endpoint URLs, request/response formats, and authentication methods.

__<ins>3.5. Domain Specific Models</ins>__

__3.5.1. Data Models:__

| Data Models  | Rationale |
| ------------- | ------------- |
| Course Model  | Represents the structure and attributes of a course, including course ID, name, description, and associated credits  |
| Student Model | Defines the properties of a student, such as student ID, name, enrolled courses, and academic records  |
| Enrollment Model  | Manages the relationship between students and courses, including enrollment status, grades, and attendance records  |

__3.5.2. Entity Relationship Diagram (ERD)__

• An ERD will be provided to illustrate the relationships between the different entities in the CMS. This diagram will include cardinality and key constraints to show how courses, students, and enrollments are interconnected.

__<ins>3.6. Architectural Diagram for Iteration 2</ins>__

![image](https://github.com/Muji90/Assignment-1-Design-Patterns/assets/145510715/0fb0c553-d236-4711-8b99-2411e6b99294)

| Element  | Description |
| ------------- | ------------- |
| User  | Represents the end-users of the CMS, such as students, lecturers, and administrators  |
| CMS Interface  | The front-end user interface through which users interact with the CMS  |
| Database  | Stores all the data related to courses, users, enrollments, grades, etc  |
| Backend server  | Handles the business logic of the CMS, processing requests and interacting with the database  |
| Analytics Engine  | Analyzes data to provide insights, such as course popularity, student performance, etc  |
| Report Generator | Creates reports based on the analytics provided by the Analytics Engine  |

__1. User:__ This represents the end-users of the CMS, such as students, instructors, and administrators. They interact directly with the CMS interface.

__2. CMS Interface:__ This is the front-end part of the system where users interact with the application. It could include web pages, forms, and other user interface elements. The CMS Interface fetches data from the database as per user requests and displays it.

__3. Database:__ All of the CMS's data, including user profiles, enrollment information, and course details, are stored in this component. In response to queries received from the CMS Interface, it transmits data to the Backend Server for processing.

__4. Backend Server:__ This is the part of the server-side software that handles data that comes in from the database. It manages the application's business logic, which includes updating course information and enrolling students in classes.

__5. Analytics Engine:__ This part is in charge of examining the data that the Backend Server processes. It may provide information about learning objectives, course popularity, user behavior.

__6. Report Generator:__ The Report Generator generates reports based on the insights that are produced by the Analytics Engine. These reports may include user activity data, course statistics, or other pertinent information.

__7. Data Flow:__ The data flow and component interactions are shown by the arrows. For instance, the CMS Interface is used by the User to interact, and this causes the Database to get data.

__<ins>3.7. Sequence Diagrams for Iteration 2</ins>__

![image](https://github.com/Muji90/Assignment-1-Design-Patterns/assets/145510715/f1e663a5-2c7d-4f91-943a-a5d6e15ebb27)

| Element  | Method Description |
| ------------- | ------------- |
| Student | Initiates the process by requesting to view course materials  |
| CMS  | Receives the request from the student and fetches course materials from the database  |
| Database  | Responds to the CMS's request by returning the requested course materials  |

__<ins>3.8. Methods and Interfaces Description</ins>__

__• UploadMaterial():__ Allows lecturers to upload new materials.

__• ModifyMaterial():__ Enables lecturers to make changes to existing materials.

__• DeleteMaterial():__ Grants lecturers the ability to remove materials.

__• DownloadMaterial():__ Used by students to download course materials.

__<ins>3.9. Architectural Decisions and Rationale</ins>__

The choice to keep the Course Material Manager and Access Controller apart guarantees a distinct division of responsibilities, improving maintainability and security. Students may use the Material Database efficiently since it is designed for speedy retrievals.
