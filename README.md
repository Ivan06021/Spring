# University Academic Disciplines Management System

This project is a Java Spring application designed to manage the academic disciplines of a university. The system allows for user authentication, role-based access, and management of disciplines, schedules, grades, and notifications.

## Table of Contents
- [Functional Requirements](#functional-requirements)
- [System Behavior](#system-behavior)
- [REST API Endpoints](#rest-api-endpoints)

## Functional Requirements
1. **User Authentication**: Users can register and log into the system.
2. **Role-Based Authorization**: Different types of users (administrators, teachers, students) have different levels of access.
3. **Discipline Management**: Administrators can add, edit, and delete academic disciplines.
4. **Discipline Viewing**: Users can view a list of available disciplines.
5. **Discipline Details**: Users can view details of a specific discipline (description, teacher, schedule).
6. **Schedule Management**: Students can add disciplines to their schedule.
7. **Schedule Viewing**: Students can view their schedule with added disciplines.
8. **Grading**: Teachers can assign grades to students for disciplines.
9. **Grade Viewing**: Students can view their grades.
10. **Notifications**: The system sends notifications about changes in schedules or grades to students.

## System Behavior
1. **Registration**: Users fill out the registration form, after which a confirmation is sent to their email.
2. **Authentication**: Users log into the system using their email and password.
3. **Authorization**: Access rights are determined by the user's role.
4. **Discipline Management**: Administrators can add, edit, and delete disciplines via the admin panel.
5. **Discipline Viewing**: All users can view the list of disciplines and details for each discipline.
6. **Schedule Management**: Students can add selected disciplines to their schedule.
7. **Schedule Viewing**: Students can view their schedule in a convenient format.
8. **Grading**: Teachers can assign grades to students through the teacher panel.
9. **Grade Viewing**: Students can view their grades in the corresponding section.
10. **Notifications**: The system automatically sends notifications about changes in schedules or grades.

## REST API Endpoints

### Authentication and Authorization
- `POST /api/auth/register` - Register a new user.
- `POST /api/auth/login` - Log into the system.
- `POST /api/auth/logout` - Log out of the system.

### Discipline Management
- `GET /api/disciplines` - Get a list of disciplines.
- `POST /api/disciplines` - Add a new discipline (Admin only).
- `GET /api/disciplines/{id}` - Get information about a specific discipline.
- `PUT /api/disciplines/{id}` - Edit a discipline (Admin only).
- `DELETE /api/disciplines/{id}` - Delete a discipline (Admin only).

### Schedule
- `GET /api/schedule` - Get the student's schedule.
- `POST /api/schedule` - Add a discipline to the schedule.
- `DELETE /api/schedule/{id}` - Remove a discipline from the schedule.

### Grades
- `GET /api/grades` - Get the student's grades.
- `POST /api/grades` - Assign a grade (Teachers only).
- `GET /api/grades/{id}` - Get detailed information about a grade.

### Users
- `GET /api/users` - Get a list of users (Admin only).
- `GET /api/users/{id}` - Get information about a specific user.
- `PUT /api/users/{id}` - Edit user information (Admin only).

### Notifications
- `GET /api/notifications` - Get a list of notifications.
- `POST /api/notifications` - Send a new notification (Admin only).

