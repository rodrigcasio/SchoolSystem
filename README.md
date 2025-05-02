# School System: C++ OOP Project

A C++ project demonstrating object-oriented programming (OOP) principles, including polymorphism, encapsulation, and abstraction. The system models a school (`University of Alberta`) managing teachers and students, with features for assigning classrooms, evaluating teachers, enrolling students, and displaying information.

## Features
- **Teachers**: Base `Teacher` class with derived `MathTeacher` and `ScienceTeacher` classes, showcasing polymorphism via virtual `chat()` methods.
- **Evaluations**: Teachers receive evaluations (grade, comment, feedback), stored in a vector and displayed individually or school-wide.
- **Students**: Students enroll in teachers’ classes, tracked via `Teacher*` pointers, with formatted enrollment display.
- **School**: Manages teachers and students using `std::vector<Teacher*>` and `std::vector<Student*>`, with methods for adding, enrolling, and displaying data.

## OOP Principles
- **Polymorphism**: Virtual `chat()` method overridden in `MathTeacher` (e.g., "teaching for 15 years") and `ScienceTeacher` (e.g., "favorite topic Energy").
- **Encapsulation**: Private data (e.g., `Teacher::name`, `Student::enrolledTeachers`) accessed via getters/setters.
- **Abstraction**: Methods like `enrollInClass()` and `displayAllEvaluations()` hide implementation details.
- **Pointers**: Use of `Teacher*` and `Student*` avoids object slicing and supports dynamic allocation, as noted in the code.

## How to Run
```bash
g++ src/mainReviewAbstraction.cpp src/fns_*.cpp -I include -o school
./school
```
## Sample Output

### Classroom Assignments
Leonhard Euler's classroom will be #1002 for this year's Mathematics class!

Marie Curie's classroom will be #1003 for this year's Science class!

Emmy Noether's classroom will be #1004 for this year's Mathematics class!

Albert Einstein's classroom will be #1005 for this year's Science class!

### Teacher Introductions
Leonhard Euler: I've been teaching Mathematics for 15 years.

Marie Curie: My favorite Science topic is Radioactivity.

Emmy Noether: My favorite Mathematics topic is Abstract Algebra.

Albert Einstein: My favorite Science topic is Relativity.

### Student Enrollments 
Rodrigo Casio enrolled in Mathematics with Leonhard Euler (Room 1002)

Rocio Garcia enrolled in Science with Marie Curie (Room 1003)

Alex Chen enrolled in Mathematics with Emmy Noether (Room 1004)

Priya Sharma enrolled in Science with Albert Einstein (Room 1005)

### Evaluations 
--All Evaluations at University of Alberta-- :

Teacher: Leonhard Euler
- 95 | Euler explains calculus clearly! | More examples needed.

Teacher: Marie Curie
- 92 | Curie’s experiments are inspiring! | Lab sessions could be longer.
  
Teacher: Emmy Noether
- 98 | Noether makes algebra exciting! | Faster grading, please.
  
Teacher: Albert Einstein
- 100 | Einstein is an amazing professor! | No feedback needed!

## Purpose
Developed as part of my C++ learning journey to demonstrate mastery of OOP concepts. This project showcases my ability to design and implement complex systems using pointers, vectors, and inheritance, building on projects like `RestaurantInheritance` and `BankSystem`.

## Author
Rodrigo Casio ([View my Github profile](https://github.com/rodrigcasio))
