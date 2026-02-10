# Restaurant Management System

A web-based Restaurant Management System built using Java Servlets, JSP, and MySQL. This application is designed to streamline restaurant operations, allowing admins to manage the menu and customers to make reservations easily.

## 📋 Features

### Admin Role
- **Dashboard**: View high-level metrics and system status.
- **Manage Food Menu**:
    - Add new food items with ingredients and status.
    - Delete food items from the menu.
    - Update food availability.
- **Reservation Management**: View customer reservations.

### Customer Role
- **User Accounts**: Register and Login functionality.
- **Search Food**: Browse the menu and view food details.
- **Direct Reservation**: Reserve food items directly from the search results.

## 🛠 Technology Stack

- **Backend**: Java EE (Servlets, MVC Pattern)
- **Frontend**: JSP (JavaServer Pages), HTML, CSS
- **Database**: MySQL
- **Build System**: Ant (NetBeans Standard)
- **Server**: Apache Tomcat (Requires Servlet Containers)

## 📂 Project Structure

```text
restaurant-management-system/
├── src/java/
│   ├── controller/   # Servlets for handling requests (FoodServlet, LoginServlet, etc.)
│   ├── dao/          # Data Access Objects for database interactions
│   ├── model/        # Java Beans representing database entities (Food, User, etc.)
│   └── util/         # Utility classes, specifically DBConnection
├── web/              # Public web resources
│   ├── WEB-INF/      # Web configuration
│   ├── *.jsp         # View pages (login, dashboard, searchFood, etc.)
│   └── *.css/images  # Static assets
├── Sql File/         # Contains the database schema script
├── nbproject/        # NetBeans project configuration
└── build.xml         # Ant build script
```

## 🚀 Setup & Installation

### Prerequisites
1.  **Java Development Kit (JDK)** (Version 8 or higher).
2.  **Apache Tomcat Server** (Version 8.5/9.0 recommended).
3.  **MySQL Database Server**.
4.  **IDE**: NetBeans is recommended as the project structure is optimized for it, but Eclipse or IntelliJ IDEA can also be used.

### step 1: Database Setup
1.  Open your MySQL client (e.g., PHPMyAdmin, MySQL Workbench).
2.  Create a database named `librarydbnew` (or update the name in `src/java/util/DatabaseUtil.java` if you choose a different name).
3.  Import the provided SQL script:
    -   File Location: `Sql File/librarydbnew.sql`
4.  Verify the tables (`users`, `foods`, `reservations`) are created.

### Step 2: Application Configuration
1.  Open the project in your IDE.
2.  Navigate to `src/java/util/DatabaseUtil.java`.
3.  Verify the database credentials match your local setup:
    ```java
    private static final String URL = "jdbc:mysql://localhost:3306/librarydbnew";
    private static final String USER = "root";     // Default XAMPP/MySQL user
    private static final String PASSWORD = "";     // Default XAMPP/MySQL password
    ```
4.  **Important**: Ensure the MySQL JDBC Driver (connector jar) is added to your project's libraries or Tomcat's `lib` folder.

### Step 3: Run the Application
1.  Clean and Build the project.
2.  Run the project on Apache Tomcat.
3.  The application will be accessible at: `http://localhost:8080/restaurant-management-system`

## 🔑 Default Credentials

The system comes with pre-configured users (based on the SQL dump):

| Role | Username | Password |
|------|----------|----------|
| **Admin** | `admin` | `admin123` |
| **Customer** | `customer` | `customer123` |

## 📝 Usage Guide

1.  **Login**: Access the login page to sign in as an Admin or Customer.
2.  **Register**: New customers can create an account via the registration page.
3.  **Admin Actions**: Log in as admin to access the dashboard. Use the navigation to add foods or manage existing listings.
4.  **Customer Actions**: Log in as a customer to search for food using keywords. Click "Reserve" on any available item.

## 📄 License

This project is open-source and available for educational and personal use.
