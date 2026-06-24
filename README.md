# \# 🛴 Urban Scooter — Full QA Plan

# 

# Complete quality assurance plan for the Urban Scooter web and mobile application,

# covering manual testing, API validation, mobile testing, and SQL data validation.

# 

# \## 📋 Project Overview

# 

# | Item | Detail |

# |---|---|

# | Application | Urban Scooter — scooter rental web + mobile app |

# | QA Type | Manual Testing, API Testing, Mobile Testing, SQL Validation |

# | Total Test Cases | 76 (41 web + 35 mobile) |

# | Bugs Reported | 15+ documented with severity and priority |

# | Tools Used | Jira, Postman, SQL, Chrome DevTools, Android Emulator |

# 

# \## 🧪 What was tested

# 

# \### Web Application (41 test cases)

# \- User registration and login flows

# \- Form field validation — equivalence classes and boundary values

# \- Order creation and management

# \- UI behavior across different screen sizes

# 

# \### Mobile Application (35 test cases)

# \- Login and authentication flows

# \- Order placement and tracking

# \- Push notification delivery

# \- Offline mode behavior

# \- Emulator vs real device validation

# 

# \### API Testing (Postman)

# \- Courier creation endpoint

# \- Order cancellation flow

# \- Station search validation

# \- Authentication token handling

# \- Status code validation (200, 400, 401, 404, 422)

# 

# \### SQL Data Validation

# \- Delivery time queries

# \- User activity reports

# \- Employee salary data integrity

# \- Backend data consistency checks

# 

# \## 📁 Repository Structure

# urban-scooter-qa/

# 

# │

# 

# ├── test-cases/

# 

# │   └── urban-scooter-test-cases.xlsx   # Full test suite (web + mobile)

# 

# │

# 

# ├── api-testing/                         # Postman collections (coming soon)

# 

# ├── sql-queries/                         # SQL validation queries (coming soon)

# 

# ├── bug-reports/                         # Bug documentation (coming soon)

# 

# │

# 

# └── README.md

# 

# \## 🔍 Test Design Techniques Used

# 

# \- \*\*Equivalence Class Partitioning\*\* — grouped valid/invalid inputs for form fields

# \- \*\*Boundary Value Analysis\*\* — tested min/max limits for name, phone, date fields

# \- \*\*Decision Tables\*\* — mapped combinations of conditions for order flows

# \- \*\*Exploratory Testing\*\* — uncovered edge cases not covered by formal test cases

# 

# \## 📊 Test Results Summary

# 

# | Area | Test Cases | Status |

# |---|---|---|

# | Web — Valid flows | 12 | ✅ All passed |

# | Web — Invalid inputs | 29 | ✅ All passed |

# | Mobile — Core flows | 20 | ✅ All passed |

# | Mobile — Edge cases | 15 | ✅ All passed |

# | API endpoints | 8 | ✅ All validated |

# 

# \## 👤 Author

# 

# \*\*Santiago Valencia Cortés\*\* — QA Engineer  

# \[GitHub](https://github.com/SantiagoSvc) · \[LinkedIn](https://linkedin.com/in/santivacomecatronica)

