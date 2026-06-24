# Urban Scooter - Full QA Plan

![Manual Testing](https://img.shields.io/badge/Manual_Testing-76_Cases-blue?style=for-the-badge)
![API Testing](https://img.shields.io/badge/API_Testing-Postman-orange?style=for-the-badge&logo=postman)
![Mobile](https://img.shields.io/badge/Mobile_Testing-Android-green?style=for-the-badge&logo=android)
![SQL](https://img.shields.io/badge/Data_Validation-SQL-lightgrey?style=for-the-badge&logo=postgresql)

**Complete quality assurance plan for a scooter rental web + mobile application.**
Manual testing · API validation · Mobile QA · SQL data integrity

---

## Project at a Glance

| Item | Detail |
|---|---|
| Application | Urban Scooter — scooter rental web + Android mobile app |
| Test Cases | 76 total — 41 web, 35 mobile |
| Bugs Found | 15+ documented with severity, priority and steps to reproduce |
| Techniques | Equivalence classes, Boundary values, Decision tables, Exploratory |
| Tools | Jira, Postman, SQL, Chrome DevTools, Android Emulator |

---

## What Was Tested

### Web Application — 41 Test Cases

| Area | Cases | Result |
|---|---|---|
| Registration and login flows | 8 | Passed |
| Form field validation with boundary values | 18 | Passed |
| Order creation and management | 10 | Passed |
| UI behavior and responsiveness | 5 | Passed |

### Mobile Application — 35 Test Cases

| Area | Cases | Result |
|---|---|---|
| Login and authentication | 8 | Passed |
| Order placement and tracking | 12 | Passed |
| Push notification delivery | 7 | Passed |
| Offline mode behavior | 8 | Passed |

### API Testing with Postman

| Endpoint | Method | Status |
|---|---|---|
| Create courier | POST | Validated |
| Cancel order | PUT | Validated |
| Search stations | GET | Validated |
| Authentication flow | POST | Validated |
| Status codes 200, 400, 401, 404, 422 | ALL | Validated |

### SQL Data Validation

- Delivery time consistency across tables
- User activity audit queries
- Employee salary data integrity
- Backend data consistency checks

---

## Test Design Techniques

| Technique | Applied To |
|---|---|
| Equivalence Class Partitioning | Form fields — valid vs invalid input groups |
| Boundary Value Analysis | Name length, phone format, date ranges |
| Decision Tables | Order flow condition combinations |
| Exploratory Testing | Edge cases beyond formal test cases |

---

## Repository Structure

    urban-scooter-qa/
    |
    +-- test-cases/
    |   +-- urban-scooter-test-cases.xlsx
    |
    +-- api-testing/
    +-- sql-queries/
    +-- bug-reports/
    |
    +-- README.md

---

## Author

**Santiago Valencia Cortes** — QA Engineer
Mechatronics Engineer transitioning into QA Automation and AI Testing

GitHub: https://github.com/SantiagoSvc
LinkedIn: https://linkedin.com/in/santivacomecatronica