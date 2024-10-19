# Cursor Instruction File for Claude-3.5-sonnet

## Filesystem
- app/
  - database.py
  - schemas.py
  - main.py
  - crud.py
- templates/
  - index.html
- requirements.txt
- README.md
- .gitignore
- LICENSE

## File Summaries

### README.md
Summary: Project overview, installation instructions, usage information, project structure, contribution guidelines, and license information.

Key components:
- Project description and features
- Installation and setup guide
- Usage examples
- Project structure overview

Future key components:
- Documentation for new features (no-code interface, real-time API, etc.)
- AI agent usage instructions
- Team/User/Project management guide

### .gitignore
Summary: Standard Python .gitignore file, ignoring common files and directories such as __pycache__, virtual environments, IDE-specific files, logs, and databases.

Key components:
- Python-specific ignores
- Virtual environment ignores
- IDE and editor ignores

### LICENSE
Summary: MIT License template, granting permission to use, modify, and distribute the software under certain conditions.

Key components:
- License terms and conditions
- Copyright notice

### app/main.py
Summary: FastAPI application entry point. Contains route definitions, middleware setup, and API endpoint implementations.

Key components:
- FastAPI app initialization
- Database connection handling
- CORS middleware configuration
- API route definitions for CRUD operations

Future key components:
- No-code interface route
- Real-time API consumption endpoints
- CSV upload route
- AI agent interaction endpoints

### app/database.py
Summary: Database connection and session management. Includes SQLAlchemy engine creation and session factory.

Key components:
- SQLAlchemy engine configuration
- Session local class definition
- Base class for declarative models

Future key components:
- Dynamic table creation functions for CSV imports
- Data transformation functions for API consumption
- Team/User/Project schema updates

### app/schemas.py
Summary: Pydantic models for request/response schemas and data validation.

Key components:
- Base schemas for common fields
- Request and response models for each entity
- Validation rules and field constraints

Future key components:
- Schemas for no-code interface
- Real-time API data models
- CSV upload request/response models
- Team/User/Project models

### app/crud.py
Summary: CRUD (Create, Read, Update, Delete) operations for database interactions.

Key components:
- Functions for creating, reading, updating, and deleting entities
- Query optimization techniques
- Error handling for database operations

Future key components:
- Helper functions for no-code interface
- Real-time data update operations
- CSV data import functions
- Team/User/Project CRUD operations

### templates/index.html
Summary: Main HTML template for the dashboard interface.

Key components:
- Base structure for the dashboard
- Placeholders for dynamic content
- JavaScript includes for interactivity

Future key components:
- No-code interface elements
- Real-time data display components
- CSV upload form and progress indicator
- AI agent interaction interface
- Team/User/Project management views

### requirements.txt
Summary: List of Python package dependencies for the project.

Key components:
- FastAPI and related packages
- SQLAlchemy for database operations
- Other necessary libraries

Future key components:
- Additional libraries for CSV parsing
- AI-related packages for the agent system
- WebSocket libraries for real-time updates

## System Expansion Instructions

### 1. No-Code Interface for CRUD Operations

Objective: Create a user-friendly interface for performing CRUD operations on the dashboard without writing code.

Steps:
1. Develop a new route in `main.py` for the no-code interface.
2. Create a new HTML template for the interface in the `templates` directory.
3. Implement JavaScript functions to handle form submissions and API calls.
4. Update `crud.py` to include any necessary helper functions for the no-code interface.
5. Add appropriate error handling and validation for user inputs.
6. Implement a drag-and-drop interface for creating and modifying database schemas.
7. Create a visual query builder for complex database operations.

### 2. Real-time API Consumption

Objective: Implement real-time API consumption to pull data into the SQLite backend for display on the dashboard.

Steps:
1. Add a new file `api_consumer.py` in the `app` directory.
2. Implement asynchronous functions to fetch data from external APIs.
3. Create a background task system using FastAPI's BackgroundTasks.
4. Develop a scheduling mechanism for periodic API calls.
5. Implement data transformation and storage functions in `database.py`.
6. Create new routes in `main.py` to trigger API consumption manually.
7. Update the dashboard to display real-time data from the SQLite backend.
8. Implement WebSocket connections for live updates on the frontend.

### 3. Design Language Improvements

Objective: Enhance the design language using componentized design principles.

Steps:
1. Create a new directory `static/components` for reusable UI components.
2. Develop a base CSS framework for consistent styling across components.
3. Implement a JavaScript module system for component functionality.
4. Create individual component files (e.g., `card.html`, `table.html`, `chart.html`).
5. Update existing templates to use the new componentized design.
6. Implement a theming system for easy customization of the dashboard's appearance.
7. Create documentation for using and extending the component system.

### 4. CSV Data Uploading

Objective: Implement a feature to upload CSV files and ingest the data into a new SQLite backend table.

Steps:
1. Create a new route in `main.py` for CSV file uploads.
2. Implement a file upload form in the dashboard interface.
3. Develop a CSV parsing function in a new file `csv_parser.py`.
4. Create dynamic table creation functions in `database.py`.
5. Implement data validation and error handling for CSV imports.
6. Add a progress indicator for large file uploads and processing.
7. Create a summary view of imported data and allow for corrections.

### 5. AI Agent System

Objective: Develop an AI agent system that can update the dashboard and make code commits on behalf of users.

Steps:
1. Create a new directory `ai_agent` for the agent system.
2. Implement a natural language processing module for understanding user requests.
3. Develop a code generation system based on user instructions.
4. Create a version control interface to make Git commits programmatically.
5. Implement a review and approval system for AI-generated changes.
6. Develop a logging and monitoring system for AI agent actions.
7. Create an interface for users to interact with and guide the AI agent.

### 6. Team/User/Project Structure

Objective: Implement a system for building and managing multiple dashboards with team and user management.

Steps:
1. Update the database schema to include tables for users, teams, and projects.
2. Implement user authentication and authorization systems.
3. Create a project management interface for creating and managing dashboards.
4. Develop team management features, including invitations and role assignments.
5. Implement access control for different dashboard elements based on user roles.
6. Create a system for sharing and collaborating on dashboards within teams.
7. Develop a notification system for team activities and project updates.

## Notes for Claude-3.5-sonnet

- When implementing these features, maintain the existing project structure and coding style.
- Ensure that each expansion is treated as an independent module that can be implemented without relying on the others.
- When generating code, focus on creating modular and reusable components.
- Provide clear documentation and comments for any new features or changes.
- Consider performance implications, especially for data-intensive operations like CSV uploads and real-time API consumption.
- Ensure that all new features adhere to security best practices, particularly for user authentication and data handling.

## Common User Requests

1. "How do I implement feature X from the expansion instructions?"
   - Provide a brief overview of the feature
   - Suggest which files to modify
   - Offer a code snippet example

2. "Can you help me debug this error in [file name]?"
   - Ask for the specific error message
   - Request the relevant code snippet
   - Suggest common troubleshooting steps

3. "How can I optimize the performance of [specific operation]?"
   - Discuss potential bottlenecks
   - Suggest optimization techniques
   - Provide a before/after code example

4. "What's the best way to test [feature/function]?"
   - Recommend appropriate testing frameworks
   - Provide an example test case
   - Discuss test coverage considerations

5. "How do I integrate [third-party library/API] into the project?"
   - Suggest necessary modifications to requirements.txt
   - Provide an example of library usage
   - Discuss potential conflicts or considerations

## Code Style Guide

1. Python:
   - Follow PEP 8 guidelines
   - Use type hints for function arguments and return values
   - Prefer list comprehensions over map() and filter() where appropriate
   - Use f-strings for string formatting

2. JavaScript:
   - Use ES6+ features (arrow functions, destructuring, etc.)
   - Prefer const over let, avoid var
   - Use async/await for asynchronous operations
   - Follow camelCase naming convention for variables and functions

3. HTML/CSS:
   - Use semantic HTML5 elements
   - Follow BEM (Block Element Modifier) naming convention for CSS classes
   - Prefer flexbox and grid for layouts
   - Use CSS variables for theming and consistent styling

4. General:
   - Keep functions small and focused on a single responsibility
   - Use meaningful variable and function names
   - Write descriptive comments for complex logic
   - Include docstrings for all functions and classes
