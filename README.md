# Student Management System

A comprehensive desktop application for managing student records efficiently. Built with Python, this system provides a user-friendly GUI interface to perform CRUD operations on student data with a MySQL database backend.

## 📋 Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Requirements](#requirements)
- [Installation](#installation)
- [Database Setup](#database-setup)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Key Features in Detail](#key-features-in-detail)
- [Contributing](#contributing)
- [License](#license)


## Preview

![Screenshot 1](Screenshots/Screenshot%202026-05-30%20020246.png)
![Screenshot 2](Screenshots/Screenshot%202026-05-30%20020317.png)
![Screenshot 3](Screenshots/Screenshot%202026-05-30%20020354.png)


## ✨ Features

- **Add Students**: Register new students with complete information
- **Update Records**: Modify existing student data seamlessly
- **Delete Records**: Remove student records from the database
- **Search Functionality**: Search students by Roll Number, Name, or Contact
- **View All Students**: Display complete list of all registered students
- **Data Validation**: Ensures all required fields are filled before submission
- **Interactive Table View**: Display student records in a well-organized table with scrollbars
- **Clear Form**: Reset input fields with a single click

## 🛠️ Technologies Used

- **Python 3.x** - Programming language
- **Tkinter** - GUI framework for desktop interface
- **PyMySQL** - MySQL database connector
- **MySQL** - Relational database management system

## 📦 Requirements

Before running the application, ensure you have the following installed:

- Python 3.x
- MySQL Server
- pip (Python package manager)

### Python Dependencies

```bash
pip install pymysql
```

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/naahe25/Student-Management-System-In-Python.git
   cd Student-Management-System-In-Python
   ```

2. **Install required packages**
   ```bash
   pip install pymysql
   ```

3. **Set up the MySQL database** (see Database Setup section)

4. **Run the application**
   ```bash
   python Student.py
   ```

## 🗄️ Database Setup

### Create Database and Table

1. **Open MySQL Command Line or MySQL Workbench**

2. **Create the database**
   ```sql
   CREATE DATABASE stm;
   USE stm;
   ```

3. **Create the students table**
   ```sql
   CREATE TABLE students (
       roll_no VARCHAR(50) PRIMARY KEY,
       name VARCHAR(100) NOT NULL,
       email VARCHAR(100),
       gender VARCHAR(20),
       contact VARCHAR(15),
       dob VARCHAR(20),
       address TEXT
   );
   ```

4. **Configure database connection in code**
   - Update the connection parameters in `Student.py` if needed:
     - `host`: localhost (default)
     - `user`: root (default)
     - `password`: "" (empty by default)
     - `database`: stm

## 📖 Usage

### Main Interface

The application window displays three main sections:

#### 1. **Manage Student Panel** (Left Side)
   - **Roll Number**: Enter student's roll number
   - **Name**: Enter student's full name
   - **Email**: Enter student's email address
   - **Gender**: Select gender from dropdown (Male, Female, Other)
   - **Contact**: Enter student's contact number
   - **D.O.B**: Enter date of birth
   - **Address**: Enter student's address

#### 2. **Action Buttons**
   - **Add**: Insert a new student record
   - **Update**: Modify an existing student record
   - **Delete**: Remove a student record
   - **Clear**: Clear all input fields

#### 3. **Search & Display Panel** (Right Side)
   - **Search Options**: Choose search criteria (Roll_No, Name, Contact)
   - **Search**: Find specific student records
   - **Show All**: Display all student records
   - **Table View**: View all student data in a formatted table

### Workflow

1. **Adding a Student**
   - Fill in all required fields in the Manage Student panel
   - Click the "Add" button
   - A confirmation message will appear upon successful insertion

2. **Updating a Student**
   - Click on a student row in the table to populate the form
   - Modify the desired fields
   - Click the "Update" button

3. **Deleting a Student**
   - Click on a student row in the table
   - Click the "Delete" button
   - The record will be removed from the database

4. **Searching for a Student**
   - Select a search criteria from the dropdown
   - Enter the search term
   - Click the "Search" button
   - Results will be displayed in the table

5. **Viewing All Records**
   - Click the "Show All" button to display all student records

## 🏗️ Project Structure

```
Student-Management-System-In-Python/
│
└── Student.py          # Main application file containing the Student class
```

## 🔑 Key Features in Detail

### GUI Components
- **Tkinter Frames**: Organized layout with separate panels for input and display
- **Entry Widgets**: Text fields for user input
- **Combobox**: Dropdown selections for Gender and Search criteria
- **Treeview Table**: Professional table display with horizontal and vertical scrollbars
- **Text Widget**: Multi-line address input field

### Database Operations
- **CRUD Operations**: Full Create, Read, Update, Delete functionality
- **Search Functionality**: Filter records based on multiple criteria
- **Data Persistence**: All changes are committed to the MySQL database

### User Experience
- **Data Validation**: Prevents submission of incomplete forms
- **Error Handling**: User-friendly error messages via message boxes
- **Clear Feedback**: Success notifications for all operations
- **Responsive UI**: Interactive table with row selection capability

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the MIT License. Feel free to use it for personal and educational purposes.

## 👤 Author

**naahe25**
- GitHub: [@naahe25](https://github.com/naahe25)

## 🙋 Support

If you encounter any issues or have questions:
- Open an issue on the [GitHub repository](https://github.com/naahe25/Student-Management-System-In-Python)
- Check existing issues for solutions

---

**Last Updated**: December 2024

Happy coding! 🎓
