# jwt-token
This project is a Spring Boot REST API that implements JWT (JSON Web Token) based authentication. It allows users to log in and receive a token, which can be used to access secured endpoints.
# 🔐 Spring Boot JWT Authentication API

## 📌 Project Description

This project is a **Spring Boot REST API** that implements **JWT (JSON Web Token) based authentication**. It allows users to log in and receive a token, which can be used to access secured endpoints.

---

## 🚀 Features

* User login authentication
* JWT token generation
* Secure API endpoints
* RESTful API design

---

## 🛠 Technologies Used

* Java
* Spring Boot
* Spring Security
* Spring Data JPA
* MySQL
* Maven
* JWT (JJWT)

---

## 📂 Project Structure

```
com.JWTExample.JWT_Demo
│
├── config
│   └── SecurityConfig.java
│
├── controller
│   └── AuthController.java
│
├── entity
│   └── User.java
│
├── repository
│   └── UserRepository.java
│
├── filter
│   └── Jwtfilter.java
│
└── service
    └── jwtservice.java
```

---

## ⚙️ How It Works

1. User sends login request (`/api/login`)
2. Backend checks username & password from database
3. If valid → JWT token is generated
4. Token is used to access secured APIs

---

## 🔑 API Endpoints

### 🔹 Login

**POST** `/api/login`

**Params:**

```
username=your_username
password=your_password
```

**Response:**

```
JWT Token (if valid)
OR
Invalid Credentials
```

---

### 🔹 Test Endpoint

**GET** `/api/hello`

**Response:**

```
Hello! JWT Authentication Successful
```

---

## 🧩 Dependencies

Add in `pom.xml`:

```xml
<dependency>
    <groupId>io.jsonwebtoken</groupId>
    <artifactId>jjwt-impl</artifactId>
    <version>0.11.5</version>
    <scope>runtime</scope>
</dependency>

<dependency>
    <groupId>io.jsonwebtoken</groupId>
    <artifactId>jjwt-jackson</artifactId>
    <version>0.11.5</version>
    <scope>runtime</scope>
</dependency>
```

---

## 🔒 Security Config

* CSRF disabled
* CORS disabled
* Form login disabled
* JWT-based authentication

---

## 🗄️ Database

**Table:** `users`

| Column   | Type   |
| -------- | ------ |
| id       | Long   |
| username | String |
| password | String |

---

## 📸 Screenshots

### 🔹 Login API (Postman)

 <img width="1787" height="926" alt="Screenshot 2026-04-02 060810" src="https://github.com/user-attachments/assets/ea961b38-0362-444f-97f3-c4845061071e" />

<img width="1815" height="821" alt="Screenshot 2026-04-02 064211" src="https://github.com/user-attachments/assets/4d5f1216-ddb0-4998-b910-2223f9720a04" />

### 🔹 Invalid Login

<img width="1805" height="949" alt="Screenshot 2026-04-02 064900" src="https://github.com/user-attachments/assets/c7dca3b4-9f4b-499a-aefa-0f86d0fcf539" />

### 🔹 Secured API (JWT Token)
 <img width="1805" height="964" alt="Screenshot 2026-04-02 064847" src="https://github.com/user-attachments/assets/667336b0-dedc-41ac-a969-eec048243e1d" />

### 🔹 Database (MySQL)
<img width="511" height="81" alt="Screenshot 2026-04-02 065730" src="https://github.com/user-attachments/assets/cd5d0c20-468a-48d4-91af-82ca3f8c965c" />

---

## ▶️ Run Project

```bash
mvn spring-boot:run
```

---

 
