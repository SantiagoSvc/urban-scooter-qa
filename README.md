# \# 🛴 Urban Scooter — Full QA Plan

# 

# <div align="center">

# 

# !\[Manual Testing](https://img.shields.io/badge/Manual%20Testing-76%20Cases-blue?style=for-the-badge\&logo=checkmarx)

# !\[API Testing](https://img.shields.io/badge/API%20Testing-Postman-orange?style=for-the-badge\&logo=postman)

# !\[Mobile](https://img.shields.io/badge/Mobile%20Testing-Android-green?style=for-the-badge\&logo=android)

# !\[SQL](https://img.shields.io/badge/Data%20Validation-SQL-lightgrey?style=for-the-badge\&logo=postgresql)

# 

# \*\*Complete quality assurance plan for a scooter rental web + mobile application.\*\*  

# \*Manual testing · API validation · Mobile QA · SQL data integrity\*

# 

# </div>

# 

# \---

# 

# \## 🎯 Project at a Glance

# Application   →  Urban Scooter (web + Android mobile app)

# 

# Test Cases    →  76 total  (41 web  |  35 mobile)

# 

# Bugs Found    →  15+ documented with severity, priority and reproduction steps

# 

# Techniques    →  Equivalence classes · Boundary values · Decision tables · Exploratory

# 

# Tools         →  Jira · Postman · SQL · Chrome DevTools · Android Emulator

# 

# \---

# 

# \## 🗂️ What Was Tested

# 

# \### 🌐 Web Application — 41 Test Cases

# 

# | Area | Cases | Result |

# |---|---|---|

# | Registration \& login flows | 8 | ✅ Passed |

# | Form field validation (boundary values) | 18 | ✅ Passed |

# | Order creation \& management | 10 | ✅ Passed |

# | UI behavior \& responsiveness | 5 | ✅ Passed |

# 

# \### 📱 Mobile Application — 35 Test Cases

# 

# | Area | Cases | Result |

# |---|---|---|

# | Login \& authentication | 8 | ✅ Passed |

# | Order placement \& tracking | 12 | ✅ Passed |

# | Push notification delivery | 7 | ✅ Passed |

# | Offline mode behavior | 8 | ✅ Passed |

# 

# \### 🔌 API Testing — Postman

# 

# | Endpoint | Method | Validated |

# |---|---|---|

# | Create courier | POST | ✅ |

# | Cancel order | PUT | ✅ |

# | Search stations | GET | ✅ |

# | Authentication flow | POST | ✅ |

# | Status codes | 200 / 400 / 401 / 404 / 422 | ✅ |

# 

# \### 🗄️ SQL Data Validation

# 

# \- Delivery time consistency across tables

# \- User activity audit queries

# \- Employee salary data integrity

# \- Backend data consistency checks

# 

# \---

# 

# \## 🔍 Test Design Techniques

# 

# | Technique | Applied To |

# |---|---|

# | \*\*Equivalence Class Partitioning\*\* | Form fields — valid vs invalid input groups |

# | \*\*Boundary Value Analysis\*\* | Name length, phone format, date ranges |

# | \*\*Decision Tables\*\* | Order flow combinations |

# | \*\*Exploratory Testing\*\* | Edge cases beyond formal test cases |

# 

# \---

# 

# \## 📁 Repository Structure

# urban-scooter-qa/

# 

# │

# 

# ├── 📊 test-cases/

# 

# │   └── urban-scooter-test-cases.xlsx

# 

# │

# 

# ├── 🔌 api-testing/

# 

# ├── 🗄️ sql-queries/

# 

# ├── 🐛 bug-reports/

# 

# │

# 

# └── README.md

# 

# \---

# 

# \## 👤 Author

# 

# \*\*Santiago Valencia Cortés\*\*  

# Mechatronics Engineer → QA Engineer

# 

# \[!\[GitHub](https://img.shields.io/badge/GitHub-SantiagoSvc-black?style=flat\&logo=github)](https://github.com/SantiagoSvc)

# \[!\[LinkedIn](https://img.shields.io/badge/LinkedIn-Santiago%20Valencia-blue?style=flat\&logo=linkedin)](https://linkedin.com/in/santivacomecatronica)

