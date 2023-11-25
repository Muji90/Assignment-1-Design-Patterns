# <ins>Step 1: Review Inputs</ins>

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

| Category  | Details |
| ------------- | ------------- |
| Design Purpose  | The design purpose is to develop a comprehensive educational management system that caters to the diverse needs of students, lecturers, administrators, and maintainers by providing course information, enabling student subscriptions, facilitating lecturer functions, supporting maintenance tasks, and allowing administrative control while adhering to specific privacy, usability, and system performance requirements.  |
| Primary Functional Requirements  | Course Enrollment (UC 1): This fits the design purpose as it addresses the needs of both students (RS1) and administrators (RA3) by allowing students to enroll in courses through the CMS, aligning with the comprehensive educational management system's objective.  |
| Quality Attributes   | QA 3: Usability  |
