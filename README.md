1. Functional Requirements
User Authentication and Authorization

Users must be able to register, login, and logout.
Users should have different roles: Admin, Teacher, and Student.
Manage Courses

Admins can create, read, update, and delete course information.
Teachers can view courses they are assigned to and update course content.
Students can view courses they are enrolled in.
Manage Disciplines

Admins and Teachers can create, read, update, and delete disciplines.
Each discipline should be associated with a specific course.
Upload and Manage Educational Materials

Teachers can upload and manage educational materials for their courses.
Students can view and download educational materials for the courses they are enrolled in.
Course Enrollment

Students can enroll in available courses.
Admins can manage student enrollments in courses.
Class Schedules

Admins and Teachers can create, read, update, and delete class schedules.
Students can view the class schedule for the courses they are enrolled in.
Notifications and Announcements

Teachers can send announcements to students enrolled in their courses.
Students receive notifications about new materials, schedule changes, and announcements.
Assessment Management

Teachers can create, read, update, and delete assessments for their courses.
Students can view and submit assessments.
Grade Management

Teachers can assign grades to student submissions.
Students can view their grades for the courses they are enrolled in.
User Profile Management

Users can view and update their profile information.
2. Mockups
Since I cannot draw images, I will describe the mockups textually. You can use these descriptions to create visual mockups with any design tool.

Login Page

Fields: Username, Password
Buttons: Login, Register
Dashboard (Different views for Admin, Teacher, Student)

Admin: Overview of users, courses, disciplines
Teacher: My Courses, Announcements, Schedule
Student: My Courses, Notifications, Schedule
Courses Management Page (Admin)

List of courses with actions: Create, Edit, Delete
Form: Course Name, Description, Assigned Teacher
Disciplines Management Page

List of disciplines with actions: Create, Edit, Delete
Form: Discipline Name, Course, Description
Course Details Page

Course Name, Description, List of Disciplines, Educational Materials, Announcements
Educational Materials Page

List of materials with actions: Upload, Edit, Delete
Form: Material Title, Description, File Upload
Enrollment Page (Student)

List of available courses with an enroll button
Class Schedule Page

Calendar view with scheduled classes
Actions: Create, Edit, Delete (for Admin/Teacher)
Assessments Page

List of assessments with actions: Create, Edit, Delete (for Teachers)
Form: Assessment Title, Description, Due Date
Profile Page

Fields: Username, Email, Password, Profile Picture
Actions: Update Profile
3. System Behavior and REST API Endpoints
User Authentication and Authorization

POST /api/auth/register: Register a new user
POST /api/auth/login: Authenticate a user
POST /api/auth/logout: Logout a user
Course Management

GET /api/courses: Get all courses
POST /api/courses: Create a new course
GET /api/courses/{id}: Get details of a specific course
PUT /api/courses/{id}: Update a specific course
DELETE /api/courses/{id}: Delete a specific course
Discipline Management

GET /api/disciplines: Get all disciplines
POST /api/disciplines: Create a new discipline
GET /api/disciplines/{id}: Get details of a specific discipline
PUT /api/disciplines/{id}: Update a specific discipline
DELETE /api/disciplines/{id}: Delete a specific discipline
Educational Materials Management

GET /api/materials: Get all materials
POST /api/materials: Upload a new material
GET /api/materials/{id}: Get details of a specific material
PUT /api/materials/{id}: Update a specific material
DELETE /api/materials/{id}: Delete a specific material
Enrollment Management

POST /api/enrollments: Enroll a student in a course
DELETE /api/enrollments/{id}: Unenroll a student from a course
