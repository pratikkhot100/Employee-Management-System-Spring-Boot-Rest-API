# 🌐📡 Spring Boot Rest-API

## 🌱 What is Spring Boot REST API?
A Spring Boot REST API is a web service built using Spring Boot, a Java-based framework that simplifies the development of stand-alone, production-grade Spring applications. REST (Representational State Transfer) is a popular architectural style for building web services that communicate over HTTP using standard methods like GET, POST, PUT, and DELETE.

# 🚀 Spring Boot REST API Example

This project demonstrates a complete **Spring Boot REST API** using:

- **Spring MVC**
- **Spring Data JPA**
- **Hibernate**
- **MySQL**
- **Postman** for API testing
- **MVC architecture**

---

## 🧰 Technologies Used

| Technology | Purpose |
|------------|---------|
| **Spring Boot** | Framework to quickly build RESTful APIs |
| **Spring MVC** | Handles HTTP requests via controllers |
| **JPA (Java Persistence API)** | ORM specification to interact with databases |
| **Hibernate** | Implementation of JPA |
| **MySQL** | Relational database used for data storage |
| **Postman** | API client for testing endpoints |
| **REST API** | Architectural style for building web services |

---

## 🌐 What is a REST API?

A **REST API** (Representational State Transfer) allows applications to communicate via HTTP using standard methods:

- `GET` → Retrieve data  
- `POST` → Create new data  
- `PUT` → Update existing data  
- `DELETE` → Remove data

All data is exchanged in **JSON** format.

---

## 🏗️ Project Architecture (MVC Pattern)

The application follows the **Model-View-Controller (MVC)** architecture:

- **Model** – Represents application data (e.g., User, Product)
- **View** – Not used directly; API returns JSON responses
- **Controller** – Handles incoming HTTP requests and routes them to the correct service
- **Service** – Contains the business logic
- **Repository** – Communicates with the database using JPA

---

### 📂 Project Structure

        spring-boot-rest-api/
        ├── src/
        │   └── main/
        │       ├── java/
        │       │   └── com/
        │       │       └── example/
        │       │           └── demo/
        │       │               ├── controller/
        │       │               │   └── UserController.java        # Handles HTTP requests
        │       │               ├── service/
        │       │               │   └── UserService.java           # Business logic
        │       │               ├── repository/
        │       │               │   └── UserRepository.java        # JPA repository for DB access
        │       │               ├── model/
        │       │               │   └── User.java                  # JPA entity mapped to DB table
        │       │               └── DemoApplication.java           # Main class to bootstrap app
        │       └── resources/
        │           ├── application.properties                     # Configuration (DB, JPA, etc.)
        │           └── static/                                    # Static files (if any)
        │
        ├── pom.xml or build.gradle                                # Project dependencies and plugins
        └── README.md                                               # Project documentation


---

## ⚙️ MySQL Configuration (application.properties)

Update the following in your `application.properties`:

- Database URL
- Username & Password
- Hibernate dialect
- DDL auto mode (e.g., `update`, `create`, `validate`)

---

## 🧪 API Testing with Postman

| Method | Endpoint | Description | Body (JSON) |
|--------|----------|-------------|-------------|
| `GET` | `/api/users` | Fetch all users | – |
| `POST` | `/api/users` | Create a new user | `{ "name": "John", "email": "john@example.com" }` |
| `DELETE` | `/api/users/{id}` | Delete a user by ID | – |

Use **Postman** or **cURL** to interact with these endpoints after running the app.

---

## 📖 Key Concepts

| Term | Description |
|------|-------------|
| **JPA** | Java API for managing relational data via ORM |
| **Hibernate** | Popular implementation of JPA |
| **Spring Boot** | Framework for rapid application development |
| **MySQL** | Open-source relational database |
| **REST** | API style using HTTP methods for CRUD operations |
| **MVC** | Design pattern separating data, UI, and logic layers |

---

## ✅ How to Run

1. Clone the repository
2. Set up your MySQL database
3. Update the `application.properties` with DB credentials
4. Run the Spring Boot application
5. Test APIs via Postman

---

## 📦 Future Enhancements

- Add Swagger for API documentation
- Integrate Spring Security for authentication
- Dockerize the application
