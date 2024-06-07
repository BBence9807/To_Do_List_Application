## To Do List Application Project Overview

The ToDo List application will allow users to create, read, update, and delete (CRUD) tasks. It will feature user authentication, synchronization across devices, and notifications.

### Functional Requirements
| Name |  Details |
|----------|----------|
| **User Authentication**    | Users should be able to register for an account using an email and password. Users should be able to log in using their email and password. Users should be able to log out.|
| **Task Management**    | Users should be able to create a new task. Users should be able to view a list of their tasks. Users should be able to edit an existing task. Users should be able to delete a task. Users should be able to mark a task as completed or uncompleted.Users should be able to set a due date for a task. |
| **User Profile Management**    | Users should be able to update their profile information (e.g., email, password). Users should be able to view their account details.   |
| **Notifications**   | Users should receive real-time notifications for task updates. Users should receive push notifications for task reminders on the mobile app.   |
| **Search and Filter**    | Users should be able to search for tasks by title or description. Users should be able to filter tasks based on status (completed, uncompleted) and due date.|
| **Real-time Synchronization**   | Changes made on one device (web or mobile) should be reflected in real-time on other devices.   |
| **Offline Mode (Mobile App)**   | Users should be able to access and manage tasks offline. Changes made offline should be synced when the device is back online.  |

### Non Functional Requirements
| Name |  Details |
|----------|----------|
| **Performance**    | The application should load within 2 seconds on both web and mobile platforms. The application should handle at least 1000 concurrent users without performance degradation.|
| **Scalability***    | The backend should be able to scale horizontally to handle increased load. The application should be able to handle a growing number of users and tasks without requiring major architectural changes. |
| **Security**    | User data should be encrypted in transit (TLS/SSL) and at rest.  Passwords should be hashed and salted before storing in the database. The application should implement protection against common vulnerabilities such as SQL injection, XSS, and CSRF attacks. |
| **Notifications**    | Users should receive real-time notifications for task updates. Users should receive push notifications for task reminders on the mobile app.   |
| **Search and Filter**    | Users should be able to search for tasks by title or description. Users should be able to filter tasks based on status (completed, uncompleted) and due date.|
| **Real-time Synchronization**   | Changes made on one device (web or mobile) should be reflected in real-time on other devices.   |
| **Offline Mode (Mobile App)**   | Users should be able to access and manage tasks offline. Changes made offline should be synced when the device is back online.  |
| **Usability**   |The UI should be intuitive and easy to navigate. The application should follow accessibility standards (WCAG) to ensure it is usable by people with disabilities. |
| **Reliability**   | The application should have an uptime of 99.9%. There should be mechanisms for backup and recovery to prevent data loss. |
| **Maintainability** | The codebase should be modular and well-documented to facilitate easy maintenance and updates. Automated tests should be in place to ensure that new changes do not break existing functionality. |
| **Compatibility** | The web application should be compatible with modern browsers (Chrome, Firefox, Safari, Edge). The mobile application should support the latest versions of iOS and Android.|
| **Internationalization and Localization** | The application should support multiple languages. Date and time formats should be adaptable based on the user’s locale. |


### Microservices Architecture

#### Service Components
| Name |  Details |
|----------|----------|
| Auth Service    | Handles user authentication (login, token generation, and verification).|
| User Service    | Manages user registration, profile management, and user-related data. |
| Task Service    | Handles task creation, retrieval, updating, and deletion.|
| Notification Service    | Manages sending real-time and push notifications to users.|
| Search Service    | Provides search and filtering functionality for tasks.|
| Gateway Service   | Acts as an entry point to route requests to the appropriate microservice. |
| Synchronization Service   | Ensures real-time synchronization of data across devices. |


#### Architecture diagram
![Architecture Diagram](/assets/microservice_architecture.png)