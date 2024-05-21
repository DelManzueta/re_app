### Project Summary

#### Project: Property Management App

#### Objective:

To develop a comprehensive property management application for a real estate
investor. The app aims to streamline property management operations, improve
tenant communications, track financial performance, manage maintenance requests,
and facilitate document handling.

#### Why:

Currently, the investor manages properties using a combination of spreadsheets,
emails, and disparate software solutions, leading to inefficiencies and data
inconsistencies. A centralized app will:

-   Enhance operational efficiency.
-   Provide a unified platform for managing all aspects of property management.
-   Improve data accuracy and accessibility.
-   Facilitate better communication between tenants, managers, and admins.
-   Integrate financial data seamlessly with QuickBooks.

#### How:

The app will be built using Next.js with TypeScript for the frontend, and
various AWS services for backend infrastructure. Key features will include:

-   User authentication and authorization with Amazon Cognito.
-   Tenant management with detailed profiles and lease agreements.
-   Financial tracking and integration with QuickBooks.
-   Maintenance request management linked with inventory tracking.
-   Document and image management with e-signature capabilities.
-   Real-time communication via in-app chat.
-   Admin overhead calculation and loan amortization functionalities.
-   Deployment on AWS with continuous integration and delivery (CI/CD)
    pipelines.
-   Comprehensive monitoring and logging to ensure app reliability and
    performance.

---

### 1. Project Setup

#### Scope:

-   Initialize the project with Next.js and TypeScript from scratch.
-   Set up the project structure.
-   Configure necessary development tools and libraries.
-   Ensure basic project configurations are in place.

#### Summary:

The initial phase involves setting up the foundational aspects of the property
management app. This includes creating a new Next.js project with TypeScript
from scratch, organizing the folder structure, and installing essential
dependencies. The aim is to establish a solid base for subsequent development,
ensuring all necessary tools and configurations are properly set up.

#### Tasks:

1. **Initialize Next.js Project with TypeScript:**

    - Create a new directory for the project and initialize it with a
      `package.json` file.
    - Install Next.js and TypeScript as dependencies.
    - Set up initial configuration files for Next.js and TypeScript.

2. **Set Up Project Structure:**

    - Create the following directories:
        - `src/components/atoms`: For basic UI components like buttons and
          inputs.
        - `src/components/molecules`: For more complex components composed of
          atoms, like form fields.
        - `src/components/organisms`: For larger components that comprise
          molecules and atoms, like headers and footers.
        - `src/components/templates`: For layout templates.
        - `src/pages`: For Next.js pages.
        - `src/pages/api`: For API routes.
        - `src/styles`: For global and component-specific styles.
        - `src/hooks`: For custom hooks.
        - `src/lib`: For utility functions and libraries.
        - `src/types`: For TypeScript type definitions.
        - `src/utils`: For utility functions.

3. **Install Essential Dependencies:**

    - Install React and Next.js for building the user interface.
    - Install Axios for handling API requests.
    - Install Zustand or Redux for state management.
    - Install Material-UI for styling (or choose another CSS framework/library
      as per preference).
    - Install AWS Amplify for authentication and other backend services.

4. **Configure TypeScript:**

    - Create and configure a `tsconfig.json` file to set up TypeScript in the
      project.

5. **Set Up ESLint and Prettier:**

    - Install ESLint and Prettier along with necessary plugins for Next.js and
      TypeScript.
    - Create and configure `.eslintrc.json` for linting rules.
    - Create and configure `.prettierrc` for code formatting rules.

6. **Initialize Git Repository:**

    - Initialize a Git repository in the project directory.
    - Set up a `.gitignore` file to exclude node_modules, build outputs, and
      other unnecessary files.

7. **Configure Environment Variables:**

    - Create a `.env.local` file for storing environment variables.
    - Add configuration settings such as API endpoints and authentication keys.

#### Deliverables:

-   A Next.js project with TypeScript set up from scratch.
-   Organized project folder structure.
-   Installed and configured essential development dependencies.
-   TypeScript, ESLint, and Prettier configurations.
-   Initialized Git repository with initial commit.
-   Configured environment variables.

---

### 2. User Authentication and Authorization

#### Scope:

-   Implement user authentication and authorization using Amazon Cognito.
-   Set up user registration, login, and password management.
-   Allow users to authenticate with their Apple ID or Gmail.
-   Enable the use of Apple Pay for automated payments based on user preference.
-   Ensure secure access to different parts of the application based on user
    roles (admin, manager, tenant).

#### Summary:

This phase focuses on implementing a robust authentication and authorization
system to manage user access securely. By leveraging Amazon Cognito, the app
will support multiple authentication methods, including traditional
email/password, Apple ID, and Gmail. Additionally, it will integrate Apple Pay
for users who opt for automated payments. The system will also enforce
role-based access control to ensure users can only access functionalities
appropriate to their roles.

#### Tasks:

1. **Set Up Amazon Cognito:**

    - Create and configure a new Cognito User Pool.
    - Define user attributes and policies for registration and login.
    - Configure multi-factor authentication (MFA) and account recovery options.

2. **Implement User Registration and Login:**

    - Develop registration and login forms.
    - Integrate Cognito's API for user registration, login, and password
      management.
    - Ensure secure storage and transmission of user credentials.

3. **Enable Social Login (Apple ID and Gmail):**

    - Configure Cognito to support OAuth providers (Apple ID and Google).
    - Set up necessary credentials and permissions in Apple Developer and Google
      Developer consoles.
    - Implement front-end components for Apple ID and Google sign-in.

4. **Integrate Apple Pay for Automated Payments:**

    - Implement a condition in the user settings for opting into automated
      payments via Apple Pay.
    - Ensure secure handling of payment information and compliance with relevant
      regulations.
    - Test Apple Pay integration for functionality and security.

5. **Role-Based Access Control:**

    - Define user roles and permissions (admin, manager, tenant).
    - Implement middleware to check user roles before accessing specific routes
      or functionalities.
    - Ensure unauthorized users cannot access restricted areas of the
      application.

6. **User Management:**

    - Create user profile pages for viewing and updating personal information.
    - Implement functionality for users to manage their authentication methods
      (e.g., linking/unlinking Apple ID or Gmail).

#### Deliverables:

-   A fully configured Amazon Cognito User Pool.
-   Registration and login forms integrated with Cognito.
-   Social login options for Apple ID and Gmail.
-   Apple Pay integration for automated payments.
-   Role-based access control ensuring secure access based on user roles.
-   User profile management functionalities.

---

### 3. Tenant Management

#### Scope:

-   Implement functionalities to manage tenant profiles and lease agreements.
-   Allow property managers to add, update, and view tenant information.
-   Enable secure storage and access to lease agreements.

#### Summary:

This phase aims to develop features for managing tenant information and lease
agreements. Property managers will be able to add new tenants, update existing
tenant profiles, and view detailed information. The system will also store lease
agreements securely, ensuring that only authorized users can access them.

#### Tasks:

1. **Set Up Tenant Management Database:**

    - Design and create database tables for storing tenant information and lease
      agreements.
    - Implement APIs for CRUD (Create, Read, Update, Delete) operations on
      tenant data.

2. **Develop Tenant Management Interface:**

    - Create forms and views for adding, updating, and viewing tenant
      information.
    - Ensure the interface is user-friendly and accessible.

3. **Secure Storage of Lease Agreements:**

    - Implement secure storage solutions for lease agreements.
    - Ensure only authorized users can access or modify lease agreements.

4. **Integrate with Authentication System:**

    - Ensure tenant management functionalities respect role-based access
      control.
    - Verify that only property managers and admins can manage tenant
      information.

#### Deliverables:

-   Tenant management database tables.
-   APIs for managing tenant information.
-   User interface for adding, updating, and viewing tenant profiles.
-   Secure storage and access controls for lease agreements.

---

### 4. Financial Tracking and Integration

#### Scope:

-   Implement financial tracking functionalities, including rent payments and
    expenses.
-   Integrate with QuickBooks for seamless financial management.
-   Enable tenants to make payments through various methods, including Apple
    Pay.

#### Summary:

This phase focuses on implementing financial tracking features and integrating
them with QuickBooks. Tenants will be able to make rent payments through
multiple methods, including Apple Pay. Property managers and admins will have
access to detailed financial reports and the ability to track expenses
efficiently.

#### Tasks:

1. **Set Up Financial Tracking Database:**

    - Design and create database tables for tracking rent payments and expenses.
    - Implement APIs for CRUD operations on financial data.

2. **Integrate with QuickBooks:**

    - Set up QuickBooks API integration.
    - Ensure data synchronization between the app and QuickBooks.

3. **Develop Payment Interface:**

    - Create a user-friendly interface for tenants to make payments.
    - Implement support for various payment methods, including Apple Pay.

4. **Financial Reporting:**

    - Develop financial reporting features for property managers and admins.
    - Ensure reports provide detailed insights into payments, expenses, and
      overall financial performance.

#### Deliverables:

-   Financial tracking database tables.
-   APIs for managing financial data.
-   Integration with QuickBooks.
-   Payment interface for tenants.
-   Financial reporting features for property managers and admins.

---

### 5. Maintenance Request Management

#### Scope:

-   Implement functionalities to manage maintenance requests.
-   Enable tenants to submit maintenance requests and track their status.
-   Allow property managers to assign and update maintenance requests.

#### Summary:

This phase aims to develop features for managing maintenance requests. Tenants
will be able to submit maintenance requests easily and track their status.
Property managers will have tools to assign tasks, update request statuses, and
ensure timely resolution of maintenance issues.

#### Tasks:

1. **Set Up Maintenance Request Database:**

    - Design and create database tables for storing maintenance requests.
    - Implement APIs for CRUD operations on maintenance request data.

2. **Develop Maintenance Request Interface:**

    - Create forms and views for tenants to submit and track maintenance
      requests.
    - Develop tools for property managers to assign and update maintenance
      tasks.

3. **Integrate with Tenant Management System:**

    - Ensure maintenance requests are linked to tenant profiles.
    - Provide visibility of request status to both tenants and property
      managers.

4. **Inventory Tracking Integration:**

    - Integrate maintenance request management with inventory tracking.
    - Ensure property managers can track and manage inventory items needed for
      maintenance tasks.

#### Deliverables:

-   Maintenance request database tables.
-   APIs for managing maintenance requests.
-   User interface for tenants and property managers to handle maintenance
    requests.
-   Integration with tenant management and inventory tracking systems.

---

### 6. Document and Image Management

#### Scope:

-   Implement functionalities for managing documents and images.
-   Enable secure storage, sharing, and e-signature capabilities.
-   Allow users to upload, view, and manage documents and images.

#### Summary:

This phase focuses on developing features for document and image management.
Users will be able to upload, view, and manage documents and images securely.
The system will also support e-signature capabilities to facilitate document
signing and sharing.

#### Tasks:

1. **Set Up Document Management Database:**

    - Design and create database tables for storing documents and images.
    - Implement APIs for CRUD operations on document and image data.

2. **Develop Document Management Interface:**

    - Create forms and views for uploading, viewing, and managing documents and
      images.
    - Ensure the interface is user-friendly and accessible.

3. **Implement E-Signature Capabilities:**

    - Integrate e-signature functionality for documents.
    - Ensure secure and legally compliant e-signature processes.

4. **Secure Storage and Access Control:**

    - Implement secure storage solutions for documents and images.
    - Ensure only authorized users can access, modify, or share documents and
      images.

#### Deliverables:

-   Document management database tables.
-   APIs for managing documents and images.
-   User interface for handling documents and images.
-   E-signature functionality.
-   Secure storage and access controls.

---

### 7. Real-Time Communication

#### Scope:

-   Implement real-time communication features using in-app chat.
-   Enable tenants to communicate with property managers directly.
-   Ensure chat functionality respects user roles and permissions.

#### Summary:

This phase aims to develop real-time communication features to improve
interaction between tenants and property managers. The in-app chat will allow
tenants to communicate directly with property managers, ensuring timely
resolution of issues and better overall communication.

#### Tasks:

1. **Set Up Chat Infrastructure:**

    - Design and create database tables for storing chat messages.
    - Implement APIs for sending, receiving, and storing chat messages.

2. **Develop Chat Interface:**

    - Create a user-friendly chat interface for tenants and property managers.
    - Ensure the interface supports real-time messaging and notifications.

3. **Integrate with Authentication and Authorization:**

    - Ensure chat functionality respects user roles and permissions.
    - Implement middleware to protect chat routes and ensure secure
      communication.

4. **Notification System:**

    - Implement real-time notifications for new messages.
    - Ensure users are promptly informed of new communications.

#### Deliverables:

-   Chat infrastructure and database tables.
-   APIs for managing chat messages.
-   User interface for real-time communication.
-   Integration with authentication and authorization systems.
-   Real-time notification system.

---

### 8. Admin Overhead Calculation

#### Scope:

-   Implement functionalities to calculate and track admin overhead costs.
-   Provide tools for admins to input and manage overhead cost data.
-   Enable detailed reporting and analysis of overhead costs.

#### Summary:

This phase focuses on developing features to calculate and track admin overhead
costs. Admins will have tools to input and manage overhead data, and the system
will provide detailed reporting and analysis to help monitor and control
overhead expenses.

#### Tasks:

1. **Set Up Overhead Calculation Database:**

    - Design and create database tables for storing overhead cost data.
    - Implement APIs for CRUD operations on overhead data.

2. **Develop Overhead Calculation Interface:**

    - Create forms and views for admins to input and manage overhead costs.
    - Ensure the interface provides detailed reporting and analysis tools.

3. **Integration with Financial Tracking System:**

    - Ensure overhead data is integrated with the overall financial tracking
      system.
    - Provide comprehensive financial reports that include overhead costs.

4. **Reporting and Analytics:**

    - Develop reporting and analytics features for overhead costs.
    - Ensure reports provide detailed insights and help in decision-making.

#### Deliverables:

-   Overhead calculation database tables.
-   APIs for managing overhead cost data.
-   User interface for inputting and managing overhead costs.
-   Integration with financial tracking system.
-   Reporting and analytics features for overhead costs.

---

### 9. Loan Amortization App

#### Scope:

-   Implement a loan amortization calculator.
-   Enable users to input loan details and calculate amortization schedules.
-   Provide detailed loan summaries and schedules.

#### Summary:

This phase aims to develop a loan amortization calculator that allows users to
input loan details and calculate amortization schedules. The system will provide
detailed loan summaries and schedules, helping users understand their loan
repayment structure.

#### Tasks:

1. **Set Up Loan Amortization Database:**

    - Design and create database tables for storing loan data.
    - Implement APIs for CRUD operations on loan data.

2. **Develop Loan Amortization Interface:**

    - Create forms and views for users to input loan details.
    - Implement functionality to calculate and display amortization schedules.

3. **Loan Summaries and Schedules:**

    - Develop features to provide detailed loan summaries and schedules.
    - Ensure users can view and understand their loan repayment structure.

4. **Integration with Financial Tracking System:**

    - Ensure loan data is integrated with the overall financial tracking system.
    - Provide comprehensive financial reports that include loan data.

#### Deliverables:

-   Loan amortization database tables.
-   APIs for managing loan data.
-   User interface for inputting loan details and calculating schedules.
-   Integration with financial tracking system.
-   Features for detailed loan summaries and schedules.
