# Student Course Elective Management System

## Overview

The Student Elective Management System is a console-based C program designed to help manage the elective course selection process for students in a Computer Science and Engineering (CSE) department. This program allows an administrator to create a list of elective courses, register students, allocate electives based on student preferences and SPI (Semester Performance Index), and manage changes to student elective choices.

## Features

- **Admin Login**: Secure login for administrators with a password.
- **Elective Management**: Create and display a list of electives with available seats.
- **Student Registration**: Register students with their details and elective preferences.
- **Elective Allocation**: Allocate electives to students based on their preferences and available seats.
- **Data Display**: View the list of electives and student details.
- **Search Student Details**: Search for and display specific student information.
- **Change Student Electives**: Modify the elective choice for a student if necessary.
- **Exit and Credits**: Properly close the program with a credits display.

## Usage

### Compilation

To compile the program, use a C compiler like `gcc`:

```sh
gcc -o student_elective_management_system main.c
```

### Execution

Run the compiled program:

```sh
./student_elective_management_system
```

### Admin Login

Upon running the program, you will be prompted to enter the admin password. The default password is `Matrix49`.

### Main Menu

After successful login, the main menu provides the following options:

1. **View list of Electives**: Displays the list of available electives and their seat count.
2. **View Student Data**: Displays the details of all registered students, including their allocated electives.
3. **Search Student Details**: Allows you to search for a student by roll number and view their details.
4. **Change Student Elective**: Allows changing the elective choice for a specific student.
5. **Exit**: Closes the program and displays credits.

### Creating Electives and Students

- **Elective Creation**: Enter the number of electives and their details, including the number of seats available for each elective.
- **Student Registration**: Enter the number of students and their details, including elective preferences. Preferences are prioritized from highest (1) to lowest.

### Elective Allocation

Electives are allocated to students based on their preferences and the availability of seats. Students with higher SPI are given priority during the allocation process.

### Changing Electives

Admins can modify a student's elective choice if needed. The system checks for seat availability before making changes.

### Closing the Program

To close the program, select the 'Exit' option from the main menu. The program will display credits before terminating.

## Data Structures and Algorithms

This project utilizes several data structures and algorithms concepts:

- **Linked List**: Used to store and manage the list of students. Each student is represented as a node in the linked list, allowing dynamic addition and traversal of student records.
- **Dynamic Memory Allocation**: `malloc` is used for allocating memory for the student nodes and elective arrays, allowing the program to handle a flexible number of students and electives.
- **Sorting**: Bubble sort is implemented to sort students based on their SPI. This ensures that students with higher SPI get preference during elective allocation.
- **Searching**: Linear search is used to find specific student records based on their roll number.
- **String Manipulation**: Functions such as `strcpy`, `strcmp`, and custom string swap functions are used to manage student names and elective information.

## Code Structure

The program is divided into several functions:

- **Elective Data Management**:
  - `struct electives *Elective_data()`: Create and store the list of electives.
  - `void Display_Elective_data()`: Display the list of electives with seat count.
  - `void Display_Elective_list()`: Display the list of elective names.
- **Student Data Management**:
  - `struct student *Student_data()`: Register students and collect their elective preferences.
  - `void Display_Student_Data()`: Display details of all registered students.
  - `void search_student_details()`: Search and display specific student details by roll number.
- **Elective Allocation and Modification**:
  - `int *Choice_filling()`: Collect elective preferences from students.
  - `void Allotment_Electives()`: Allocate electives to students based on preferences and available seats.
  - `void Change_Student_Elective()`: Change the elective choice for a specific student.
- **Utility Functions**:
  - `void delay()`: Introduce a delay in execution.
  - `void swap_string()`: Swap two strings.
  - `void swap_elective()`: Swap elective choices between students.
  - `void swap_SPI()`: Swap SPI values between students.
  - `void bubblesort_()`: Sort students based on their SPI using bubble sort.
- **Menu and Exit**:
  - `void menu()`: Display the main menu and handle user input.
  - `void close_project()`: Display credits and close the program.

## Dependencies

- Standard C libraries: `stdio.h`, `stdlib.h`, `string.h`, `conio.h`

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
