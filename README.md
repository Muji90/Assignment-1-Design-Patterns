
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

__2.5 Analysis of the Design Decisions for Iteration 1:__

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

__<ins>3. ADD Iteration 1 Artifacts</ins>__

__<ins>3.1. Reference Architecture</ins>__

__3.1.1. Overview:__

Three tiers—the Presentation, Logic, and Data tiers—make up the CMS's selected reference design. Scalability, modularity, and a distinct separation of concerns are supported by this design.

__3.1.2. Justification for Choice:__

Web-based applications such as the CMS are a good fit for the three-tier design. It permits:

• Scalability: Can easily handle an increasing number of users.

• Flexibility: Each tier can be developed and scaled independently.

• Security: Sensitive data in the Data tier is isolated from the Presentation tier.

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

• Web Server Security: To ensure secure data transfer, use SSL/TLS. To prevent unwanted access, make use of intrusion detection systems and firewalls.

• Load Balancing: Use load balancers to split up traffic across servers in an equitable manner, guaranteeing great dependability and availability.

• Caching Mechanisms: To enhance response speeds and lessen the strain on the Application Server, use caching on the Web Server.

__<INS>3.3. Major Components of the Architecture</INS>__

__3.3.1. Component Descriptions and interactions:__

| Component  | Descriptions | Interactions |
| ------------- | ------------- | -----------|
| User Interface (UI) Component | Gives consumers access to an interactive interface. Includes sites for managing profiles, examining grades, and enrolling in courses.  | Gathers and presents data, interacts with the Business Logic Component, and records user input |
| Business Logic Component  | Manages data operations, applies business rules, and processes user requests  | Checks for accuracy, handles user input, and communicates with the Data Access Component |
| Data Access Component  | Ensures safe and effective data operations via interfaces with the database  | Handles database CRUD (Create, Read, Update, Delete) actions and provides the Business Logic Component with the results |

__3.3.2. Scalability and Maintenance__

• Microservices Architecture: For the Application Server, thinking about using a micro services architecture to improve scalability and maintenance-friendliness.

• Database Replication: For better data availability and load dispersion, use database replication and sharding.

• Continuous Integration/Continuous Deployment (CI/CD): For effective system component changes and deployment, use CI/CD pipelines.

__3.3.3. Integration and Extensibility__

• APIs for Integration: Create RESTful APIs for the Application Server to help with third-party service or external system integration.

• Modular Design: Make sure the business logic and user interface are modular so that you can simply add more features or modify them later.

__3.3.4. Disaster Recovery and Data Backup__

• Regular Backups: To avoid data loss, do regular backups of the database server.

• Disaster Recovery Plan: Create a disaster recovery strategy to guarantee data integrity and system availability in the event of significant events.
