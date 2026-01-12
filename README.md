# Hospital Patient Management System  
**Purwadhika Data Science Bootcamp - Capstone 1**  

> ⚠️ **Important Note**: This project is created **solely for learning Python fundamentals**. The main purpose is to understand and practice basic Python concepts in the context of a simple application.

## 🏥 Project Overview
A command-line interface (CLI) application for hospital patient data management with full CRUD (Create, Read, Update, Delete) operations. This project demonstrates core Python fundamentals in real-world scenarios.

## 📚 Python Fundamentals Applied

This project implements various Python fundamental concepts as follows:

### 1. **Variables and Data Types**
   - Using variables to store data (dictionary `patientData`)
   - Data types: Dictionary, String, Integer
   - Examples: `patient_ID`, `name`, `age`, `gender`, etc.

### 2. **Dictionary (Data Structure)**
   - Storing patient data in dictionary format
   - Dictionary operations: access, add, update, delete
   - Nested dictionary to store patient information
   - Example: `patientData[patient_ID]['Name']`

### 3. **Functions**
   - Creating functions for code modularity
   - Functions with parameters and return values
   - Functions used: `read()`, `find()`, `add()`, `update()`, `delete()`, `menu()`, etc.

### 4. **Conditional Statements (If, Elif, Else)**
   - `if` statement for condition checking
   - `elif` statement for alternative conditions
   - `else` statement for default condition
   - Examples: Input validation, data checking, confirmation

### 5. **Nested If Statements**
   - Using if inside if for complex logic
   - Example: Multi-level validation in `add()` and `update()` functions

### 6. **Loops**
   - **While Loop**: For input validation and repeated menus
     - Example: `while True:` for input validation
   - **For Loop**: For iterating patient data
     - Example: `for patient_ID, data in sortedPatients:`

### 7. **String Methods**
   - `.upper()`: Convert string to uppercase
   - `.capitalize()`: Capitalize first letter
   - `.lower()`: Convert string to lowercase
   - `.isdigit()`: Check if string is a digit
   - Examples: `input().upper()`, `name.capitalize()`

### 8. **Input and Output**
   - `input()`: Receive input from user
   - `print()`: Display output to console
   - F-string for formatting: `f"Name: {name}"`

### 9. **Control Flow**
   - `break`: Exit from loop
   - `return`: Exit from function
   - Usage in validation and menu navigation

### 10. **Boolean and Logical Operations**
   - Operators: `and`, `or`, `not`
   - Comparison operators: `==`, `!=`, `<=`, `>=`
   - Example: `if age.isdigit() and 0 <= int(age) <= 120`

### 11. **Lambda Function**
   - Using lambda for sorting
   - Example: `sorted(patientData.items(), key=lambda data: data[1]['Name'])`

### 12. **List Operations**
   - `.items()` method for dictionary
   - `sorted()` function for sorting data
   - Iteration with unpacking: `for patient_ID, data in ...`

### 13. **Error Handling and Validation**
   - Input validation with while loop
   - Condition checking before operations
   - Error prevention with data validation

### 14. **Modular Program Structure**
   - Separating functions by task
   - Submenus for feature organization
   - Main menu as entry point

### 15. **Dictionary Operations**
   - Adding data: `patientData[key] = value`
   - Accessing data: `patientData[key]`
   - Updating data: `patientData[key]['field'] = new_value`
   - Deleting data: `del patientData[key]`
   - Checking existence: `if key in patientData`
## ✨ Key Features

## Key Features
1. **Patient Data Management**:
   - Add new patients with automatic validation
   - View data with name sorting option
   - Partial updates (modify specific fields only)
   - Delete data with double confirmation

2. **Smart Validation System**:
   - Automatic input standardization (uppercase names, blood types)
   - Allowlist for gender (Male/Female) and blood types (A/B/AB/O)
   - Numeric validation for age (0-120 years)
   - Duplicate Patient ID prevention

##  Validation Rules
| Field         | Rules                                   | Example Handling              |
|---------------|-----------------------------------------|--------------------------------|
| Patient ID    | Uppercase conversion, Unique check      | `p123` → `P123` (auto-fixed)  |
| Name          | Mandatory, Uppercase enforced           | `john` → `JOHN`               |
| Gender        | Strict Male/Female selection            | `male` → `Male`               |
| Age           | 0-120 numeric range                     | `150` → Rejected              |
| Blood Type    | Medical-standard values (A/B/AB/O)      | `a+` → Rejected               |
| Address       | Non-empty text input                    | Empty → Retry prompt          |

