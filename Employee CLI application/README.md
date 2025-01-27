# Employee Management CLI Application

## Description

This project is a **Command-Line Interface (CLI)** application for managing employee information. The application allows users to perform various operations such as adding, updating, deleting, viewing, and searching for employees. Employee data is saved persistently in a `employees.txt` file.

The application is implemented using Python's **Object-Oriented Programming (OOP)** principles for a clean and modular design.

---

## Features

1. **Add Employee**  
   Automatically generate a unique employee ID and add the employee's details to the system.
   
2. **Update Employee Information**  
   Modify specific details of an employee using their ID.
   
3. **Delete an Employee**  
   Remove an employee from the system by specifying their ID.
   
4. **View All Employees**  
   Display all employees stored in the system.
   
5. **Search Employee**  
   Search for employees using their name or designation.

---

## Classes and Methods

### 1. `Employee` Class
The `Employee` class acts as a blueprint for creating employee objects:
- **Attributes**:
  - `employeeId` (private): A unique identifier for each employee.
  - `name`, `designation`, `department`: Public attributes storing employee details.
- **Methods**:
  - `getEmployeeId()`: Retrieve the private employee ID.
  - `setEmployeeId(id)`: Update the private employee ID.

### 2. `EmployeeManager` Class
The `EmployeeManager` class manages all employee-related operations and handles data persistence.
- **Attributes**:
  - `employee_list`: A list storing all `Employee` objects.
  - `employee_data`: The file (`employees.txt`) used for data storage.

#### Key Methods:
- **`add_employee_list()`**  
  Loads employee data from the `employees.txt` file. Splits each line to create an `Employee` object and adds it to `employee_list`.

- **`save_employee()`**  
  Writes all `Employee` objects from `employee_list` to `employees.txt` to ensure persistent data storage.

- **`add_employee(name, designation, department)`**  
  Adds a new employee with auto-generated ID to the system and saves the changes.

- **`update_employee(employeeId, name, designation, department)`**  
  Updates the details of an existing employee by searching for their ID.

- **`delete_employee(employeeId)`**  
  Removes an employee by creating a new list without the specified ID and saving it to the file.

- **`view_all_employee()`**  
  Displays all employees in the system if `employee_list` is not empty.

- **`search_employee(name, designation)`**  
  Searches for employees based on a partial match of name or designation.

---

## Usage Instructions

1. Clone the repository:
   ```bash
   git clone <repository-link>
   cd <repository-folder>
