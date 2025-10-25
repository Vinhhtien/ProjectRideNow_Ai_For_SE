# 🏍️ RideNow – AI-Generated Booking Test Suite (SWP391)

> **Course:** SWP391 – Software Engineering Project  
> **Student:** Lê Vĩnh Tiến | Lê Văn Ngọc Ẩn | Phan Trọng Quý   
> **University:** FPT University, Da Nang Campus  
> **Date:25 October 2025  

---

## 🌟 Project Overview

**RideNow** is a web-based **Rent Bike Management System** developed using  
Java Servlet/JSP and SQL Server.  
This repository contains the **automated test suite (AI_Test_Output)** — a fully runnable **JUnit 5 + Mockito + JaCoCo** environment  
generated using **ChatGPT GPT-5** to verify the booking process and core logic of RideNow.

The system has four primary roles:
- **Admin:** manages bikes, stores, partners, and orders  
- **Partner:** manages owned motorbikes and withdrawal requests  
- **Customer:** books, pays, and requests refunds  
- **Guest:** can browse motorbikes and view details  

This AI-driven testing project ensures that the **booking, payment, and detail viewing** logic work correctly under simulated conditions  
— without connecting to a real database.

---

## 🧠 Purpose of This Repository

This repo focuses on **automated testing and coverage validation**, not app deployment.

It demonstrates:
- Use of **AI to generate runnable test code**
- Application of **ISTQB test planning principles**
- Integration of **JaCoCo** for measurable coverage
- Validation of **servlet behaviors** (Booking, MyOrders, MotorbikeDetail)
- Separation between application code and test code

---

## ⚙️ Technology Stack

| Component | Version | Description |
|------------|----------|-------------|
| Java | 17 → 23 | Runtime and compilation |
| Maven | 3.9.x | Build tool |
| JUnit | 5.10.x | Testing framework |
| Mockito | 5.5.x | Mocking framework |
| AssertJ | 3.24.x | Fluent assertions |
| JaCoCo | 0.8.12 | Coverage reporting |

---

## 🧩 Project Structure

```
RideNow-Booking-Tests/
│
├── booking-tests/
│   ├── java-stubs/                 # AI-generated test sources
│   │   └── src/test/java/booking/tests/
│   │       ├── servlet/            # Tests for Servlets
│   │       ├── service/            # Tests for Business Logic
│   │       └── ...  
│   ├── runner/
│   │   ├── pom.xml                 # Maven build file (JUnit, JaCoCo)
│   │   └── target/site/jacoco/     # HTML report after running tests
│   └── docs/                       # Optional QA documentation
│
└── README.md
```

---

## 🚀 How to Run the Tests

From the repository root, run:

```bash
mvn -f booking-tests/runner/pom.xml clean test
```

✅ Expected result:
```
BUILD SUCCESS
Tests run: 24, Failures: 0, Errors: 0, Skipped: 0
```

---

## 📊 View Coverage Report

After running the tests, open the following file in your browser:

```
booking-tests/runner/target/site/jacoco/index.html
```

This **JaCoCo HTML report** visualizes coverage metrics, showing:
- Line and branch coverage
- Missed vs executed instructions
- Per-class and per-package summaries

---

## 🤖 How the AI-Generated Tests Were Built

The following prompt workflow was used to create this repository via **ChatGPT GPT-5 Codex mode**:

| Step | Prompt Description | Output |
|------|--------------------|---------|
| **1.** | Generate ISTQB-style Test Plan | Created formal QA structure |
| **2.** | Adapt Plan to RideNow context | Identified test items and actors |
| **3.** | Generate runnable JUnit + Mockito tests | Created test classes for core servlets |
| **4.** | Configure Maven Runner | Added JaCoCo + Surefire plugins |
| **5.** | Verify execution and coverage | Confirmed full green test run & HTML report |

All logic tests are **mock-based**, ensuring independence from SQL Server and real deployment.

---

## 📘 Learning Outcomes

This project demonstrates:
- Practical application of **AI in software testing**  
- Ability to integrate **automated QA pipelines** into Maven  
- Use of **JaCoCo coverage reports** for validation metrics  
- Advanced understanding of **test isolation using Mockito**  
- Compliance with **ISTQB and academic standards**

---

## 📜 License

MIT License © 2025 

> Free for educational and academic use.  
> Attribution required for reuse or modification.

---

## ❤️ Acknowledgment

Developed using **ChatGPT GPT-5 (OpenAI)**  
as part of the **Software Engineering Project (SWP391)** course.  
> “AI doesn’t replace testers — it empowers them to test smarter.” 🤖
