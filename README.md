# 🎓 Course Registration Portal

*Northeastern University, College of Engineering*
📚 *Object-Oriented Design – Spring Boot Project*
👨‍🏫 *Instructor: Professor Daniel Peters*


## 📌 Project Overview

Welcome to the Course Registration Portal – a full-stack web application. This system enables students and faculty to manage course enrollments efficiently. The project demonstrates real-world application of **OOP principles**, using **Spring Boot**, **Hibernate**, and **MySQL**.

---

## 🗂 Table of Contents

* [🔧 Installation](#-installation)
* [🚀 Usage Guide](#-usage-guide)
* [🛠 Database Configuration](#-database-configuration)
* [🧠 Object-Oriented Principles Applied](#-object-oriented-principles-applied)
* [💡 Key Design Highlights](#-key-design-highlights)
* [🧱 Database Schema](#-database-schema)
* [👥 Authors & Contributions](#-authors--contributions)

---

## 🔧 Installation

### ✅ Prerequisites

Before you begin, ensure you have the following installed:

* ✅ Java Development Kit (JDK)
* ✅ Spring Tool Suite (STS) or IntelliJ IDEA
* ✅ Maven (build tool)
* ✅ MySQL

---

### 🌀 Clone the Repository

```bash
git clone https://github.com/CSYE6200-Object-Oriented-DesignFall2023/final-project-final-group-10.git
cd course-registration-portal
```

---

### 📦 Import into STS

1. Open **Spring Tool Suite**
2. Navigate to `File → Import → Existing Maven Projects`
3. Browse to the cloned directory
4. Finish the import process

> 🔄 STS will auto-build the project. You can track it in the **Console tab**.

---

### ⚙ Configure `application.properties`

Edit this file: `src/main/resources/application.properties`

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/course_registration_db
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD
spring.jpa.hibernate.ddl-auto=update
```

---

### ▶️ Run the Application

1. Locate `CourseRegistrationApplication.java`
2. Right-click → `Run As → Spring Boot App`

Now open your browser and visit:
👉 **[http://localhost:8080](http://localhost:8080)**

---

## 🚀 Usage Guide

### 👨‍🎓 Student Features

* View all available courses
* Filter/search by course name or ID
* Register for preferred courses
* View and manage registered courses

### 👩‍🏫 Professor Features

* Log in to access dashboard
* Create new courses
* Edit/update existing course information

> API endpoints are exposed for further integrations and automation.

---

## 🛠 Database Configuration

This app connects to **MySQL** for data storage.
Ensure your MySQL server is running and the required database is created:

```sql
CREATE DATABASE course_registration_db;
```

Update your credentials in the `application.properties` file as shown above.

---

## 🧠 Object-Oriented Principles Applied

This project is a live example of Object-Oriented Design best practices:

| Principle         | Implementation Example                                    |
| ----------------- | --------------------------------------------------------- |
| **Encapsulation** | POJOs (Plain Java Objects) – `Nilraj Mayekar`             |
| **Inheritance**   | `Student` and `Professor` extend `User` – `Rajeev Ramesh` |
| **Polymorphism**  | Method overriding for behavior – `Rajeev Ramesh`          |
| **Abstraction**   | Interfaces in DAO layer with Hibernate – `Nilraj Mayekar` |

---

## 💡 Key Design Highlights

* ✅ **Singleton Pattern** – For `SessionFactory` creation (`Manish Prasanna Kumar`)
* 🏭 **Factory Pattern** – For object creation (Student/Person) (`Srishti C Rai`)
* 📄 **Generic CSV Parser** – Reads Student/Person data (`Srishti C Rai`)
* 🧮 **Lambda Expressions** – For sorting logic (`Abdul Azeem Syed`)
* 🔍 **Streams & Comparators** – For filtering courses/students (`Puja Kalivarapu`)
* ❗ **Exception Handling** – Multiple failsafes across app (`Abdul Azeem Syed`)
* 🔐 **Role-based ENUMs** – Defining access levels (`Manish Prasanna Kumar`)
* 📊 **Data Structures** – Arrays, Lists, Sets used throughout (`Srishti C Rai`)

---

## 🌐 Tech Stack & Architecture

| Technology  | Purpose                        |
| ----------- | ------------------------------ |
| Spring Boot | Web application framework      |
| Hibernate   | ORM for database interaction   |
| MySQL       | Relational database            |
| Thymeleaf   | Template engine for HTML views |
| Maven       | Dependency management          |
| Java        | Core language for backend      |

---

## 🗃️ Sample Database Schema

> *(Add ER Diagram or schema screenshot here)*

```text
User (user_id, name, email, password, role)
Course (course_id, title, description, professor_id)
Registration (reg_id, student_id, course_id, reg_date)
```



