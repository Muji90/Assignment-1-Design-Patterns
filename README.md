[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/gPSRd_yy)
# <ins>SOFE3650F23-Project Deliverable 1 – Requirements Analysis</ins>

# <ins> Introduction</ins>

The Requirements Analysis phase is a pivotal step in the software development lifecycle, serving as the foundation upon which the entire project is built. Within the context of the Attribute Driven Design (ADD) process, this phase is even more crucial. It guarantees that the architecture of the system is customized to satisfy the unique requirements and limitations mentioned in the specifications. We may create well-informed architectural decisions that are in line with the objectives of the project and the expectations of stakeholders by carefully examining the requirements.

# Use Case Models

__<ins> Overview</ins>__

Use cases are an effective technique in system design because they offer an organized method of capturing the many ways that different actors engage with the system. From the viewpoint of the user, they provide an understandable and succinct depiction of the system's functionality. We can guarantee that the system is made to meet the real demands of its users and is both functional and user-friendly by establishing use cases.

__Use Case Model__

![image](https://github.com/Muji90/Assignment-1-Design-Patterns/assets/145510715/9409bc95-265a-4a0e-9848-8637c0fbbe25)

• Main Use Cases: Course Enrollment, View Grades, Upload Course Material, Manage Grades.

• Actors: Students, Lecturers, Administrators.

• Interactions: Interactions: Enrollment and grade viewing are available to students. Instructors have the ability to upload and manage course materials. Administrators are in charge of creating courses and maintaining professor data.

__<ins> Detailed Use Cases</ins>__

__<ins> UC 1: Course Enrollment </ins>__

__• Name:__ Course Enrollment

__• Actors:__ Students, Administrators

__• Preconditions:__ The student is included in the database. Enrollment in the course is open.

__• Post conditions:__ The student is enrolled in the desired course.

__Main Flow:__

1. The student logs into the CMS.

2. The student browses available courses.

3. The student selects a course for enrollment.

4. The system confirms the enrollment.

__Alternative Flows:__ If the course is full, the system notifies the student.

__Exceptions:__ If there's a system error, the enrollment process is halted.


__<ins> UC 2: View Grades <</ins>>__

__• Name:__ View Grades

__• Actors:__ Students

__• Preconditions:__ The student has completed courses with graded assignments/exams.

__• Post conditions:__ The student views their grades for selected courses.

__Main Flow:__

1. The student logs into the CMS.

2. The student navigates to the "Grades" section.

3. The system displays the grades for the student's courses.

__Exceptions:__ If there's a system error, the grade viewing process is halted.


__<ins> UC 3: Upload Course Material <</ins>>__

__• Name:__ Upload Course Material

__• Actors:__ Lecturers

__• Preconditions:__ The lecturer is assigned to a course.

__• Post conditions:__ Course material is uploaded and available for students.

__Main Flow:__

1. The lecturer logs into the CMS.

2. The lecturer navigates to their assigned course.

3. The lecturer selects the option to upload course material.

4. The system confirms the successful upload.

__Exceptions:__ If the file size exceeds the limit, the system notifies the lecturer


__<ins> UC 4: Manage Grades </ins>__

__• Name:__ Manage Grades

__• Actors:__ Lecturers

__• Preconditions:__ Students have submitted assignments/exams.

__• Post conditions:__ Grades are updated in the system.

__Main Flow:__

1. The lecturer logs into the CMS.

2. The lecturer navigates to the "Grades" section of their course.

3. The lecturer updates grades for assignments/exams.

4. The system confirms the grade updates.

__Alternative Flows:__ The lecturer can choose to calculate the final grade based on grading policy.

__Exceptions:__ If there's a system error, the grade management process is halted


__<ins> UC 5: Course Creation </ins>__

__• Name:__ Manage Grades

__• Actors:__ Administrators, Lecturers

__• Preconditions:__ The administrator/lecturer has the necessary permissions.

__• Post conditions:__ A new course is added to the CMS.

__Main Flow:__

1. The actor logs into the CMS.

2. Navigates to the "Create Course" section.

3. Inputs course details and saves.

4. The system confirms the course creation.

__Exceptions:__ If there's a system error, the course creation process is halted.


__<ins> UC 6: Student Profile Management </ins>__

__• Name:__ Student Profile Management

__• Actors:__ Students

__• Preconditions:__ The student has an account on the CMS.

__• Post conditions:__ The student's profile is updated.

__Main Flow:__

1. The student logs into the CMS.

2. Navigates to the "Profile" section.

3. Edits and updates personal details.

4. The system confirms the profile update.

__Exceptions:__ If there's a system error, the profile update process is halted.


__<ins> UC 7: Course Feedback and Evaluation </ins>__

__• Name:__ Course Feedback and Evaluation

__• Actors:__ Students

__• Preconditions:__ The student has completed the course.

__• Post conditions:__ Feedback is submitted.

__Main Flow:__

1. The student logs into the CMS.

2. Navigates to the completed course.

3. Submits feedback and evaluation.

4. The system confirms the submission.

__Exceptions:__ If there's a system error, the feedback submission process is halted.


__<ins> UC 8: News and Announcements Posting </ins>__

__• Name:__ News and Announcements Posting

__• Actors:__ Lecturers, Administrators

__• Preconditions:__ The actor has the necessary permissions.

__• Post conditions:__ News or announcement is posted.

__Main Flow:__

1. The actor logs into the CMS.

2. Navigates to the "News/Announcements" section.

3. Creates a new post and publishes.

4. The system confirms the post publication.

__Exceptions:__ If there's a system error, the posting process is halted.


__<ins> UC 9: Course Deletion </ins>__

__• Name:__ Course Deletion

__• Actors:__ Administrators

__• Preconditions:__ The course exists in the CMS.

__• Post conditions:__ The course is removed from the CMS.

__Main Flow:__

1. The administrator logs into the CMS.

2. Navigates to the course list.

3. Selects a course and opts for deletion.

4. The system confirms the course deletion.

__Exceptions:__ If there's a system error, the course deletion process is halted.


__<ins> UC 10: Manage Course Schedule </ins>__

__• Name:__ Manage Course Schedule

__• Actors:__ Lecturers, Administrators

__• Preconditions:__  The course exists in the CMS

__• Post conditions:__ The course schedule is updated.

__Main Flow:__

1. The actor logs into the CMS.

2. Navigates to the desired course.

3. Edits the course schedule.

4. The system confirms the schedule update.

__Exceptions:__ If there's a system error, the schedule update process is halted.


__<ins> UC 11: Manage Team Members </ins>__

__• Name:__ Manage Team Members

__• Actors:__ Lecturers

__• Preconditions:__  The course has team-based assignments or projects.

__• Post conditions:__ Team members are managed.

__Main Flow:__

1. The lecturer logs into the CMS.

2. Navigates to the "Teams" section of the course.

3. Adds or removes students from teams.

4. The system confirms the team update.

__Exceptions:__ If there's a system error, the team management process is halted.


__<ins> UC 12: Password Reset Request </ins>__

__• Name:__ Password Reset Request

__• Actors:__ Students, Lecturers, Administrators

__• Preconditions:__  The actor has an account on the CMS.

__• Post conditions:__ A password reset link is sent to the actor's email.

__Main Flow:__

1. The actor navigates to the CMS login page.

2. Clicks on "Forgot Password".

3. Inputs registered email.

4. The system sends a password reset link to the email.

__Exceptions:__ 

• If the email is not registered, the system notifies the actor.

• If there's a system error, the password reset process is halted.



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

• __Improved Communication:__ Facilitates better communication between students and lecturers, enhancing the learning experience.

• __Enhanced Learning Experience:__ Provides a platform for interactive learning materials and online assessments, catering to different learning styles.

• __Cost-Effective:__ Reduces the cost of printing and distributing physical course materials.

• __Data-Driven Decisions:__ Allows for the collection and analysis of data to make informed decisions about course design and delivery.

• __Compliance:__ Ensures compliance with educational regulations and standards.

__6.5 Risks and Challenges__

• __Data Breaches:__ Like all online systems, there's a risk of data breaches. This can be mitigated with robust security protocols and regular security audits.

• __System Downtime:__ Any system downtime can disrupt academic processes. Regular maintenance and a reliable hosting solution can minimize this risk.

• __Resistance to Change:__ Staff and students accustomed to older systems might resist transitioning to the CMS. Training sessions and user-friendly design can help in smooth adoption.

• __Integration Issues:__ Integrating with other university systems might pose challenges. Adopting standard integration protocols and thorough testing can address this.

• __Incomplete Adoption:__ There's a risk that not all features of the CMS will be utilized, reducing its effectiveness. This can be mitigated by providing comprehensive training and support.

• __Technical Problems:__ The CMS could experience malfunctions or other technical problems that limit its functioning. This can be handled with regular upgrades and a committed support staff.

• __Limited Customization:__ Users may become dissatisfied if the CMS is unable to meet their unique requirements. Offering customisation alternatives can lessen this danger.

• __Legal and Ethical Concerns:__ The CMS must abide by ethical norms and data protection rules, or it risked legal repercussions.

• __Internet dependence:__  The CMS depends on internet connectivity, which could be problematic in remote or sparsely populated locations.

• __Cultural and linguistic barriers:__ The CMS might not be inclusive due to the cultural and linguistic diversity of its users.

# 7.0 Conclusion

In order to ensure that the proposed Course Management System meets the demands of the stakeholders and tackles the problems that contemporary educational institutions are facing, it is essential to complete the Requirements Analysis phase. We establish a strong basis for the succeeding design and implementation phases by having a thorough understanding of the use cases, quality attributes, limitations, and architectural considerations. The business case makes a strong case for the adoption of the CMS by emphasizing further the commercial and operational value of the system.
