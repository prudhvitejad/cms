# Campus Management System

Campus Management System is a web-based application built using Node.js, Express.js, and EJS templates. It allows users to manage facility-related requests for different departments such as Civil, Electrical, and Plumbing. The system provides functionalities for users to submit maintenance requests, track their status, and manage workers and inventory.

## 🚀 Features

- **User Authentication**: Secure login and logout system.
- **Department Management**: Separate request handling for Civil, Electrical, and Plumbing departments.
- **Request Tracking**: Users can track the status of their requests (Pending, In Progress, Completed).
- **Worker Management**: Add, list, and remove workers assigned to tasks.
- **Inventory Management**: Track and update inventory items required for maintenance work.
- **Responsive UI**: Built with Bootstrap for a seamless user experience.

## 📌 Usage

1. **User Login**: Users can log in using their credentials.
2. **Submit Requests**: Users can submit maintenance requests.
3. **Track Requests**: Users can track the progress of their requests.
4. **Manage Workers & Inventory**: Admins can add or remove workers and update inventory.

## 🏗 Technologies Used

- **Node.js** - Backend runtime environment
- **Express.js** - Web framework for Node.js
- **EJS** - Template engine for rendering dynamic HTML
- **MySQL** - Database for storing request details
- **Bootstrap** - CSS framework for responsive design
- **JavaScript** - Frontend interactivity

## 🚀 Installation & Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/prudhvitejad/cms
   cd cms
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Configure environment variables in `.env` file:
   ```plaintext
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=yourpassword
   DB_NAME=facility_db
   ```
4. Set up the database:
   - Import `cms3.sql` into MySQL.
5. Start the server:
   ```bash
   npm start
   ```
6. Open the application in your browser:
   ```bash
   http://localhost:3000
   ```

## 📂 Project Structure

```
+-- .env                    # Environment variables for configuration
+-- .gitignore               # Git ignore rules
+-- app.js                   # Main entry point for the application
+-- cms3.sql                 # Database schema or dump file
+-- database.js              # Database connection and configuration
+-- package-lock.json        # Lock file for dependencies
+-- package.json             # Node.js dependencies and project information

+-- .vscode                  # Visual Studio Code settings
|   +-- settings.json        # VS Code workspace settings

+-- bin                      # Bin directory for startup scripts
|   +-- www                  # Script to start the application

+-- public                   # Public assets served to the frontend
|   +-- images               # Image files used in the app
|   |   +-- download.jfif    # Image file
|   |   +-- download.png     # Image file
|   |   +-- download.webp    # Image file
|   |   +-- duty.png         # Image file
|   |   +-- inventory.jpg    # Image file
|   |   +-- latest.png       # Image file
|   |   +-- logo.PNG         # Logo image
|   
|   +-- javascripts          # Custom JavaScript files for frontend functionality
|   |   +-- elctricscript.js # Electric service script
|   |   +-- script.js        # Main script
|   |   +-- sort.js          # Sorting functionality script
|   |   +-- table-sort.js    # Table sorting script
|   
|   +-- stylesheets          # CSS styles for the app
|       +-- bootstrapicons.css # Bootstrap icon styles
|       +-- electriccs.css     # Electric service styles
|       +-- loginstyle.css     # Login page styles
|       +-- reset.css          # General reset styles
|       +-- stackpathboot.css  # External styles (possibly from a CDN)
|       +-- style.css          # Main stylesheet

+-- routes                   # Backend routing for different sections
|   +-- civil_route.js       # Routes related to civil section
|   +-- electric_route.js    # Routes related to electric section
|   +-- index.js             # Home route
|   +-- login_route.js       # Routes for login functionality
|   +-- logout_route.js      # Routes for logout functionality
|   +-- plumbing_route.js    # Routes related to plumbing section
|   +-- users.js             # Routes for user management
|   +-- user_route.js        # Routes related to user operations

+-- views                    # EJS views to render dynamic pages
|   +-- error.ejs            # Error page template
|   +-- index.ejs            # Home page template
|   +-- login.ejs            # Login page template
|   
|   +-- civil                # Civil service views
|   |   +-- addinventory.ejs     # Add inventory page
|   |   +-- civil_closed.ejs     # Civil closed tasks page
|   |   +-- civil_completed.ejs  # Completed civil tasks
|   |   +-- civil_home.ejs       # Civil home page
|   |   +-- civil_inprogress.ejs # In-progress civil tasks
|   |   +-- civil_latest.ejs     # Latest civil tasks
|   |   +-- civil_pending.ejs    # Pending civil tasks
|   |   +-- duty_assignment.ejs  # Duty assignment page
|   |   +-- location_add.ejs     # Add location page
|   |   +-- location_list.ejs    # List of locations
|   |   +-- location_remove.ejs  # Remove location page
|   |   +-- reset_civil.ejs      # Reset civil data page
|   |   +-- updateinventory.ejs  # Update inventory page
|   |   +-- view_inventory.ejs   # View inventory page
|   |   +-- worker_add.ejs       # Add worker page
|   |   +-- worker_list.ejs      # List of workers
|   |   +-- worker_remove.ejs    # Remove worker page
|   
|   +-- Electric             # Electric service views
|   |   +-- addinventory.ejs        # Add electric inventory page
|   |   +-- duty_assignment.ejs     # Duty assignment page
|   |   +-- electrician_add.ejs     # Add electrician page
|   |   +-- electrician_list.ejs    # List of electricians
|   |   +-- electrician_remove.ejs  # Remove electrician page
|   |   +-- electric_closed.ejs     # Electric closed tasks
|   |   +-- electric_completed.ejs  # Completed electric tasks
|   |   +-- electric_home.ejs       # Electric home page
|   |   +-- electric_inprogress.ejs # In-progress electric tasks
|   |   +-- electric_latest.ejs     # Latest electric tasks
|   |   +-- electric_pending.ejs    # Pending electric tasks
|   |   +-- location_add.ejs        # Add location page
|   |   +-- location_list.ejs       # List of electric locations
|   |   +-- location_remove.ejs     # Remove electric location page
|   |   +-- reset_electric.ejs      # Reset electric data page
|   |   +-- updateinventory.ejs     # Update electric inventory page
|   |   +-- view_inventory.ejs      # View electric inventory page
|   
|   +-- Plumbing             # Plumbing service views
|   |   +-- addinventory.ejs        # Add plumbing inventory page
|   |   +-- duty_assignment.ejs     # Duty assignment page
|   |   +-- location_add.ejs        # Add plumbing location
|   |   +-- location_list.ejs       # List of plumbing locations
|   |   +-- location_remove.ejs     # Remove plumbing location page
|   |   +-- plumber_add.ejs         # Add plumber page
|   |   +-- plumber_list.ejs        # List of plumbers
|   |   +-- plumber_remove.ejs      # Remove plumber page
|   |   +-- plumbing_closed.ejs     # Plumbing closed tasks
|   |   +-- plumbing_completed.ejs  # Completed plumbing tasks
|   |   +-- plumbing_home.ejs       # Plumbing home page
|   |   +-- plumbing_inprogress.ejs # In-progress plumbing tasks
|   |   +-- plumbing_latest.ejs     # Latest plumbing tasks
|   |   +-- plumbing_pending.ejs    # Pending plumbing tasks
|   |   +-- reset_plumbing.ejs      # Reset plumbing data page
|   |   +-- updateinventory.ejs     # Update plumbing inventory page
|   |   +-- view_inventory.ejs      # View plumbing inventory page
|   
|   +-- User                 # User-related views
|       +-- civil_all.ejs       # View for all civil tasks
|       +-- civil_launch.ejs    # Civil task launch page
|       +-- civil_status.ejs    # Civil status page
|       +-- electric_all.ejs    # View for all electric tasks
|       +-- electric_launch.ejs # Electric task launch page
|       +-- electric_status.ejs # Electric status page
|       +-- plumbing_all.ejs    # View for all plumbing tasks
|       +-- plumbing_launch.ejs # Plumbing task launch page
|       +-- plumbing_status.ejs # Plumbing status page
|       +-- user_home.ejs       # User home page
|       +-- user_profile.ejs    # User profile page
|       +-- user_reset.ejs      # User reset page
```
