# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Student Name

## Scenario Chosen:
Hospital Database

## ER Diagram:
![image (2)](https://github.com/user-attachments/assets/5586b2fd-e508-45c8-9072-0fe278afdccf)

## Entities and Attributes:
 Student
 1. StudentID (Primary Key)
 2. FirstName
 3. LastName
 4. DateOfBirth
 5. Email
 6. PhoneNumber
 7. EnrollmentDate
 8. DepartmentID (Foreign Key)
 Faculty
 1. FacultyID (Primary Key)
 2. FirstName
 3. LastName
 4. Email
 5. PhoneNumber
 6. HireDate
 7. DepartmentID (Foreign Key)
 Department
 1. DepartmentID(Primary Key)
 2. DepartmentName
 3. Location
 Course
 1. CourseID (Primary Key)
 2. CourseName
 3. CourseCode
 4. Credits
 5. DepartmentID (Foreign Key)
 Enrollment
 1. EnrollmentID (Primary Key)
 2. StudentID (Foreign Key)
 3. CourseID (Foreign Key)
 4. EnrollmentDate
 5. Grade
Class
 1. ClassID (Primary Key)
 2. CourseID (Foreign Key)
 3. FacultyID (Foreign Key)
 4. Semester
 5. Year
 6. Schedule
 Advising
 1. AdvisingID (Primary Key)
 2. StudentID (Foreign Key)
 3. FacultyID (Foreign Key)
 4. AdvisingDate
 Prerequisite
 1.Course name (Foreign Key)
 2.Course code code (primary Key)
 3.Year
 4.Credits

## Relationships and Constraints:
 Student- Department
 1. "Belongs to" Relationship
 2. Astudent belongs to one department.
 3. Adepartment can have multiple students.
 Faculty- Department
 1. "Belongs to" Relationship
 2. Afaculty member belongs to one department.
 3. Adepartment can have multiple faculty members.
 Course- Department
 1. "Offered by" Relationship
 2. Acourse isoffered by one department.
 3. Adepartment can offer multiple courses.
 Enrollment- Student
 1. "Enrolled in" Relationship
 2. Astudent can enroll in multiple courses.
 3. Eachenrollment record is associated with one student.
 Enrollment- Course
 1. "Includes" Relationship
 2. Acourse can havemultiple students enrolled.
 3. Eachenrollment record is associated with one course.
Class- Course
 1. "Teaches" Relationship
 2. Aclass is based on one course.
 3. Acourse can havemultiple classes.
 Class- Faculty
 1. "Taughtby" Relationship
 2. Aclass is taught by one faculty member.
 3. Afaculty member can teach multiple classes.
 Advising- Student
 1. "Advises" Relationship
 2. Afaculty member advises multiple students.
 3. Eachadvising record is associated with one student.
 Advising- Faculty
 1. "Provides" Relationship
 2. Astudent is advised by one faculty member.
 3. Eachadvising record is associated with one faculty member
## Extension (Prerequisite):
The PREREQUISITE entity models the relationship between courses and their required prerequisites. Here's how it's designed:

Entity Name: PREREQUISITE

Attributes:

Course Code: Refers to the main course.

Prerequisite Code: Refers to the required prerequisite course.

Credits: May refer to the credit requirement for the prerequisite.

Year: Could indicate the academic year the prerequisite is tied to.

Relationships:

"requires" relationship connects the COURSE and PREREQUISITE entities.

This implies that a course requires the course listed in Prerequisite Code to be completed before enrollment.
## Design Choices:
When selecting entities, relationships, and assumptions for a specific task or concept in Unreal Engine, I focus on the following key points:

Entities: These are the core components involved in the task. For example, when discussing Physical Material, I chose this entity because it directly relates to defining how objects behave in terms of physics—whether they are bouncy, slippery, or heavy. The material properties like friction and density are fundamental for interaction in a 3D environment.

Relationships: The relationship between entities is crucial for understanding how they interact with each other. For instance, Physical Material and surfaces/objects have a relationship where the material defines how an object behaves physically when it collides, slides, or interacts with other objects. This relationship helps define real-world-like interactions in a virtual scene.

Assumptions: Assumptions are used to simplify complex systems or to fill in gaps where more specific details aren't provided. For example, when selecting the impact of a Physical Material, I assumed that users might be looking for how it affects objects' physical interactions in the scene, as this is the primary function in Unreal Engine, which focuses on realistic simulations.
## RESULT
Those the ER DIAGRAM is implemented successfully

