# 🎓 University Course Registration System (Python)

## 📌 Description

This project is a **simple university course registration system**, developed in **Python** using **Object-Oriented Programming (OOP)** principles.

It allows:
- creating students and courses,
- registering students for courses,
- limiting the number of courses per student,
- calculating a student’s GPA,
- displaying the courses a student is enrolled in.

This project is intended for **educational purposes**.

---

## 🧱 Project Structure

The system is based on **three main classes**:

### 1️⃣ `Student`
Represents a student.

**Attributes:**
- `name`: student name
- `id`: unique student ID
- `email`: email address
- `major`: field of study
- `enrolled_courses`: list of currently enrolled courses
- `completed_courses`: list of completed courses with grades

**Methods:**
- `calculate_gpa()`: calculates the GPA
- `register_course(course)`: registers the student for a course (maximum of 5)

---

### 2️⃣ `Course`
Represents a university course.

**Attributes:**
- `code`: course code
- `name`: course name
- `credits`: number of credits
- `capacity`: maximum number of students (default: 30)
- `enrolled_students`: list of enrolled students
- `prerequisites`: list of prerequisite course codes

**Methods:**
- `add_prerequisite(course_code)`
- `is_full()`: checks whether the course is full

---

### 3️⃣ `RegistrationSystem`
Manages students and courses.

**Attributes:**
- `students`: list of students
- `courses`: list of courses

**Methods:**
- `add_student(student)`
- `add_course(course)`
- `register_student(student_id, course_code)`
- `show_student_courses(student_id)`

---

## ▶️ Example Usage

```python
s1 = Student("Alice", "S001", "alice@email.com", "Computer Science")
s2 = Student("Bob", "S002", "bob@email.com", "Mathematics")

c1 = Course("CS101", "Python", 3)
c2 = Course("CS102", "Java", 3)

system = RegistrationSystem()
system.add_student(s1)
system.add_student(s2)
system.add_course(c1)
system.add_course(c2)

system.register_student("S001", "CS101")
system.register_student("S001", "CS102")

system.show_student_courses("S001")
