# School System (C++)

This is a small C++ project I made to practice object-oriented programming (OOP) ideas like classes, inheritance, and pointers. The program simulates a simple school system where you can add teachers and students, assign classrooms, enroll students, and see teacher evaluations.

## Features
- **Teachers**: Base `Teacher` class with derived `MathTeacher` and `ScienceTeacher` classes, showcasing polymorphism via virtual `chat()` methods.
- **Evaluations**: Teachers receive evaluations (grade, comment, feedback), stored in a vector and displayed individually or school-wide.
- **Students**: Students enroll in teachers’ classes, tracked via `Teacher*` pointers, with formatted enrollment display.
- **School**: Manages teachers and students using `std::vector<Teacher*>` and `std::vector<Student*>`, with methods for adding, enrolling, and displaying data.

## Pointers and OOP Concepts (in simple terms)

- **Pointers**: I used pointers (like `Teacher*` and `Student*`) so I could keep track of teachers and students without copying them. This also helps when you want to use inheritance and avoid problems like object slicing.
- **Polymorphism**: Some methods (like `chat()`) are virtual, so each teacher type can have their own version. This lets the program call the right method for each teacher, even if you only know the base type.
- **Encapsulation**: Most data is private, and you use getters and setters to access it. This keeps things organized and safe.
- **Abstraction**: Some methods hide the details of how things work, so you can use them without worrying about the code inside.

These ideas helped me learn how to organize code and use OOP in a small project.

## Purpose

I made this project to get better at using pointers, classes, and OOP in C++. It helped me understand how to organize code for a small system and how to use inheritance and virtual methods.

## How to Run

This project uses **CMake** build system generator for easy, cross-platform compilation. Follow these steps from the root directory of the project `SchoolSystem/`

1. **Ensure CMake is installed:**
- Make sure you have CMake (version 3.1- or higher please) and a C++ compiler (g++ or clang++) installed on your system.

2. **Generate the build system (configure):**
- Create a separated directory for the build files  and run CMake inside it. Keeping source files clean

```bash
mkdir build
cd build
cmake ..
```

3. **Build:**
- Use generated build system (`make` on Unix-like systems) to compile the executable.

```bash 
make
```

4. **Run the program:**
- The executable (SchoolSystem) will be placed inside the `build` directory.

```bash 
./SchoolSystem
```

**IMPORTANT: Note for windows users:**

- Windows developers have two ways to build the project using CMake.
  - **Command line (MSYS2/Cygwin):** If you use an environment like **MSYS2** or **WLS** (Windows Subsystem for Linux), you can follow the **Standard Build** steps above exactly.
  - **Visual Studio:** CMake can generate a Visual Studio solution. Run CMake from your `developer command prompt`, specify the generator:

```bash 
cmake .. -G "Visual Studio 17 2022"
```

Then, open the generated `.sln` file and build within Visual Studio IDE.

## Sample Output

### Classroom Assignments
```
Leonhard Euler's classroom will be #1002 for this year's Mathematics class!

Marie Curie's classroom will be #1003 for this year's Science class!

Emmy Noether's classroom will be #1004 for this year's Mathematics class!

Albert Einstein's classroom will be #1005 for this year's Science class!
```
### Teacher Introductions
```
Leonhard Euler: I've been teaching Mathematics for 15 years.

Marie Curie: My favorite Science topic is Radioactivity.

Emmy Noether: My favorite Mathematics topic is Abstract Algebra.

Albert Einstein: My favorite Science topic is Relativity.
```
### Student Enrollments 
```
Rodrigo Casio enrolled in Mathematics with Leonhard Euler (Room 1002)

Rocio Garcia enrolled in Science with Marie Curie (Room 1003)

Alex Chen enrolled in Mathematics with Emmy Noether (Room 1004)

Priya Sharma enrolled in Science with Albert Einstein (Room 1005)
```
### Evaluations 
```
--All Evaluations at University of Alberta-- :

Teacher: Leonhard Euler
- 95 | Euler explains calculus clearly! | More examples needed.

Teacher: Marie Curie
- 92 | Curie’s experiments are inspiring! | Lab sessions could be longer.
  
Teacher: Emmy Noether
- 98 | Noether makes algebra exciting! | Faster grading, please.
  
Teacher: Albert Einstein
- 100 | Einstein is an amazing professor! | No feedback needed!
```
## Author

Rodrigo Casio  
[My GitHub Profile](https://github.com/rodrigcasio)
