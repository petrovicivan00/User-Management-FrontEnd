# User Management Web Application

This is a web application for managing users and their permissions. It provides support for CRUD (Create, Read, Update, Delete) operations on users and ensures proper authorization based on a defined set of permissions.

## Features

- **User Management:** Create, read, update, and delete user records.
- **Authentication:** Authenticate users using JWT (JSON Web Tokens).
- **Unique Email:** Ensure that email addresses are unique; multiple users cannot have the same email.
- **Password Security:** Store passwords securely using a hash algorithm (not as plain text).
- **Permission System:** Implement a permission system with the following permissions:
  - `can_create_users`
  - `can_read_users`
  - `can_update_users`
  - `can_delete_users`
- **Frontend Pages:** Implement four frontend pages:
  - Login Page
  - User Listing Page: Display a table of all users with their name, last name, email, and permissions.
  - User Creation Page: Create a new user with required fields and permissions.
  - User Edit Page: Edit user details including name, last name, email, and permissions.
- **Frontend Authorization:** Control frontend behavior based on user permissions. Users with appropriate permissions will see relevant links and actions.
- **Error Handling:** Properly handle errors, including notifying users of unauthorized actions.
- **JWT Storage:** After login, store the JWT token in local storage and send it with each subsequent request for authentication.

## Frontend Technology

- Framework: Angular 2+

## Backend Technology

- Framework: Spring or JBoss
- Database: Relational Database (Specify your choice)

## Getting Started

1. Clone the repository to your local machine.
2. Set up the backend server (Spring or JBoss) and configure the database.
3. Set up the frontend by navigating to the Angular project directory and installing dependencies.
4. Configure the frontend to connect to the backend server.
5. Start both the backend and frontend servers.

## Permissions and Behavior

- **`can_read_users` Permission:** Allows access to the user listing page. If the user doesn't have this permission, they will see a message indicating lack of access.
- **`can_create_users` Permission:** Displays a link to the user creation page. Allows access to the user creation page. If the user lacks this permission, the link is hidden, and access to the creation page is forbidden.
- **`can_update_users` Permission:** Makes email addresses in the user listing clickable, allowing access to the user edit page. If the user doesn't have this permission, email addresses are not clickable, and access to the edit page is denied.
- **`can_delete_users` Permission:** Adds a delete button for each user in the listing. If the user lacks this permission, the delete button is hidden.

# Angular

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 14.2.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
