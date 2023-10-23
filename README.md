[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/gPSRd_yy)
# SOFE3650F23-Project Deliverable 1 – Requirements Analysis

# 1.0 Introduction

The Requirements Analysis phase is a pivotal step in the software development lifecycle, serving as the foundation upon which the entire project is built. Within the context of the Attribute Driven Design (ADD) process, this phase is even more crucial. It guarantees that the architecture of the system is customized to satisfy the unique requirements and limitations mentioned in the specifications. We may create well-informed architectural decisions that are in line with the objectives of the project and the expectations of stakeholders by carefully examining the requirements.

# 2.0 Use Case Models

__2.1 Overview__

Use cases are an effective technique in system design because they offer an organized method of capturing the many ways that different actors engage with the system. From the viewpoint of the user, they provide an understandable and succinct depiction of the system's functionality. We can guarantee that the system is made to meet the real demands of its users and is both functional and user-friendly by establishing use cases.

__2.2 Use Case Model__

![image](https://github.com/Muji90/Assignment-1-Design-Patterns/assets/145510715/9409bc95-265a-4a0e-9848-8637c0fbbe25)



• Main Use Cases: Course Enrollment, View Grades, Upload Course Material, Manage Grades.

• Actors: Students, Lecturers, Administrators.

• Interactions: Enrollment and grade viewing are available to students. Instructors have the ability to upload and manage course materials. Administrators are in charge of creating courses and maintaining professor data

__2.3 Detailed Use Cases__

__Use Case 1: Course Enrollment__

• Name: Course Enrollment

• Actors: Students, Administrators

• Preconditions: The student is included in the database. Enrollment in the course is open.

• Post conditions: The student is enrolled in the desired course.

• Main Flow:

1. The student logs into the CMS.

2. The student browses available courses.

3. The student selects a course for enrollment.

4. The system confirms the enrollment.

• Alternative Flows: If the course is full, the system notifies the student.

• Exceptions: If there's a system error, the enrollment process is halted.

__Use Case 2: View Grades__

• Name: View Grades

• Actors: Students

• Preconditions: The student has completed courses with graded assignments/exams.

• Post conditions: The student views their grades for selected courses.

• Main Flow:

1. The student logs into the CMS.

2. The student navigates to the "Grades" section.

3. The system displays the grades for the student's courses.

• Exceptions: If there's a system error, the grade viewing process is halted.

__Use Case 3: Upload Course Material__

• Name: Upload Course Material

• Actors: Lecturers

• Preconditions: The lecturer is assigned to a course.

• Post conditions: Course material is uploaded and available for students.

• Main Flow:

1. The lecturer logs into the CMS.

2. The lecturer navigates to their assigned course.

3. The lecturer selects the option to upload course material.

4. The system confirms the successful upload.

• Exceptions: If the file size exceeds the limit, the system notifies the lecturer.

__Use Case 4: Manage Grades__

• Name: Manage Grades

• Actors: Lecturers

• Preconditions: Students have submitted assignments/exams.

• Post conditions: Grades are updated in the system.

• Main Flow:

1. The lecturer logs into the CMS.

2. The lecturer navigates to the "Grades" section of their course.

3. The lecturer updates grades for assignments/exams.

4. The system confirms the grade updates.

• Alternative Flows: The lecturer can choose to calculate the final grade based on grading policy.

• Exceptions: If there's a system error, the grade management process is halted.

# 3.0 Quality Attributes for the Application

__3.1 Overview__

Quality attributes are the non-functional requirements of a system, defining how the system operates rather than what it does. They play a vital role in shaping the system's architecture, ensuring it meets certain standards of performance, security, usability, and more. By identifying and prioritizing these attributes, we can design a system that not only fulfills its functional requirements but also delivers a high-quality user experience.

__3.2 List of Quality Attributes__

• __Name:__ Performance

1. __Description:__ The system's ability to respond quickly to user requests.

2. __Rationale__: To ensure users can access course information and perform tasks without delays.

• __Name:__ Security

1. __Description:__ Protecting user data and ensuring unauthorized access is prevented.

2. __Rationale:__ To safeguard sensitive student and course information and maintain user trust.

• __Name:__ Usability

1. __Description:__ The system's interface is intuitive and user-friendly.

2. __Rationale:__ To ensure users can easily navigate and utilize the system without facing challenges.

• __Name:__ Availability

1. __Description:__ Ensuring the system is accessible and operational when users need it.

2. __Rationale:__ Students, lecturers, and administrators rely on the CMS for various tasks. Downtime can disrupt academic processes and schedules.

• __Name:__ Scalability

1. __Description:__ The system's ability to handle increased loads, whether more users, courses, or data entries.

2. __Rationale:__ As the institution grows and more students enroll, the CMS should be able to accommodate this growth without performance degradation.

• __Name:__ Interoperability

1. __Description:__ The system's capability to interact and exchange data seamlessly with other university systems.

2. __Rationale:__ The CMS might need to integrate with other institutional systems like registration platforms, library systems, or payment gateways.

• __Name:__ Modifiability

1. __Description:__ The ease with which the system can be modified to accommodate changes or additions.

2. __Rationale:__ Educational requirements and technologies evolve. The CMS should be adaptable to these changes without extensive overhauls.

• __Name:__ Reliability

1. __Description:__ The system's ability to operate without failure under specified conditions.

2. __Rationale:__ Users should be able to trust that the CMS will function consistently, especially during critical periods like enrollment or exam grading.

• __Name:__ Portability

1. __Description:__ The ease with which the system can be transferred from one environment to another.

2. __Rationale:__ If there's a need to migrate the CMS to a different server or platform, the process should be straightforward.

• __Name:__ Maintainability

1. __Description:__ The architecture of the system should make it simple to update, repair bugs, and make enhancements without impairing its general operation.

2. __Rationale:__ Frequent maintenance keeps the CMS current and free of problems that might impair its functionality.

• __Name:__ Privacy

1. __Description:__ Safeguarding the private data of educators, administrators, and students.

2. __Rationale:__ Users should feel secure knowing that their academic and personal information is protected and out of the hands of unauthorized individuals.

# 4.0 System Constraints for the Application

__4.1 Overview__

The limitations or restrictions placed on a system's functionality and design are referred to as system constraints. These limitations may be the result of a number of factors, such as budgetary constraints, stakeholder demands, legal obligations, or technical limitations. It is essential to comprehend and deal with these limitations as they have a big impact on the system's overall architecture and design choices.

__4.2 List of Constraints__

1. Platform Independence: Users should be able to access the CMS from a variety of devices and operating systems without experiencing any compatibility problems if it is platform-independent.

2. Data Storage: The system has to have a strong database with a set storage limit because of the volume of course materials, student information, and grades.

3. Security Protocols: Strict security guidelines must be followed by the CMS to safeguard user data, particularly private and sensitive data like grades.

4. Integration: The system has to support common data interchange formats and protocols in order to be compatible with other university systems.

5. Regulatory Compliance: In order to guarantee that user data is treated properly and ethically, the CMS must abide by legislation pertaining to data protection and education.

6. Accessibility: The system must to comply with online accessibility guidelines and be usable by those with impairments.

# 5.0 Architectural Concerns

__5.1 Overview__

Architectural concerns encompass the various considerations and challenges that arise during the design and implementation of a system's architecture. These concerns can influence the system's structure, behavior, and evolution. Addressing these concerns is crucial to ensure that the system meets its functional requirements while also satisfying non-functional requirements like performance, security, and maintainability.

__5.2 List of Architectural Concerns__

1. __Name:__ Scalability

• __Description:__ The system's capacity to manage higher loads, such additional users or data input.

• __Implications:__ Whether there are more users, courses, or students at once, the architecture should be able to grow with them.

3. __Name:__ Modularity

• __Description:__ Dividing the system up into separate parts or sections that are capable of working alone.

• __Implications:__ Modular designs facilitate updates and maintenance and guarantee that modifications to one element don't negatively impact other modules.

4. __Name:__ Performance

• __Description:__ making sure the system loads material quickly and satisfies user demands.

• __Implications:__ Poor performance may turn off users. Retrieving and processing data efficiently should be the top priority in the architecture.

5. __Name:__ Security

• __Description:__ Ssafeguarding the system against hostile activity, data breaches, and unauthorized access.

• __Implications:__ A breach may jeopardize user confidence and result in legal action. The design should incorporate security features like authentication and encryption.

6. __Name:__ Maintainability

• __Description:__ The ease with which the system can be updated, debugged, or enhanced.

• __Implications:__ A system that's hard to maintain can become obsolete quickly. The architecture should be designed with future updates in mind.

7. __Name:__ Integration

• __Description:__ The system's ability to seamlessly connect and exchange data with other systems.

• __Implications:__ Poor integration can lead to data silos and inefficiencies. The architecture should support standard integration protocols.

# 6.0 Business Case

__6.1 Overview__

A business case provides a justification for a proposed project based on its expected commercial benefits. It serves as a bridge between the technical and business aspects of a project, ensuring that the proposed solution aligns with organizational goals and delivers value.

__6.2 Problem Statement__

Modern educational institutions handle vast amounts of data, from course materials to student grades. Managing this data efficiently, ensuring its accessibility while maintaining security, and providing an intuitive interface for both educators and students have become pressing challenges.

__6.3 Proposed Solution__

A centralized platform is provided by the Course Management System (CMS) for lecturers to post course materials, handle grades, and interact with students. Students get access to course materials, may register for classes, and can see their grades. To ensure efficient academic operations, administrators can supervise the design of courses and manage the information of lecturers and students.

__6.4 Benefits__

• __Efficiency:__ Having all course administration in one place cuts down on duplication and simplifies the academic process.

• __Accessibility:__ Makes course materials and grades available to instructors and students around-the-clock.

• __Security:__ Assures the protection of sensitive data, such as student grades and private information.

• __Scalability:__ The capacity to handle an increase in users and courses without seeing a drop in performance.

• __Integration:__ Consistent data and easy integration with other university systems.

__6.5 Risks and Challenges__

• __Data Breaches:__ Like all online systems, there's a risk of data breaches. This can be mitigated with robust security protocols and regular security audits.

• __System Downtime:__ Any system downtime can disrupt academic processes. Regular maintenance and a reliable hosting solution can minimize this risk.

• __Resistance to Change:__ Staff and students accustomed to older systems might resist transitioning to the CMS. Training sessions and user-friendly design can help in smooth adoption.

• __Integration Issues:__ Integrating with other university systems might pose challenges. Adopting standard integration protocols and thorough testing can address this.

# 7.0 Conclusion

The Requirements Analysis phase is crucial in ensuring that the proposed Course Management System aligns with the needs of the stakeholders and addresses the challenges faced by modern educational institutions. By understanding the use cases, quality attributes, constraints, and architectural concerns, we lay a solid foundation for the subsequent design and implementation phases. The business case further underscores the commercial and operational value of the CMS, making a compelling argument for its adoption.
