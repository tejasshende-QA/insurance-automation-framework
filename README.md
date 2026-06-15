# 🛡️ Insurance Policy & Claims Automation Framework

> **Hybrid Test Automation Framework** for Insurance Domain (Property & Casualty / Life Insurance)  
> Built with Selenium WebDriver + Java + TestNG + Maven | Page Object Model + Data-Driven

---

## 👨‍💻 Author
**Tejas Shende** | QA Automation Engineer  
📧 tejasshende3666@gmail.com | 📍 Pune, India

---

## 🏗️ Framework Architecture

```
insurance-automation/
├── src/
│   ├── main/java/com/insurance/
│   │   ├── pages/          # Page Object Model Classes
│   │   │   ├── LoginPage.java
│   │   │   ├── PolicyPage.java
│   │   │   └── ClaimsPage.java
│   │   ├── utils/          # Utility Classes
│   │   │   ├── ConfigReader.java
│   │   │   ├── ExcelReader.java
│   │   │   └── ScreenshotUtil.java
│   │   └── config/
│   └── test/
│       ├── java/com/insurance/
│       │   ├── base/
│       │   │   └── BaseTest.java       # WebDriver Setup & Teardown
│       │   └── tests/
│       │       ├── LoginTest.java      # 5 Test Cases
│       │       ├── PolicyTest.java     # 6 Test Cases
│       │       └── ClaimsTest.java     # 5 Test Cases
│       └── resources/
│           ├── config.properties
│           └── testng.xml
├── testdata/
│   └── InsuranceTestData.xlsx          # Excel Test Data
├── screenshots/                        # Auto-captured on failure
├── reports/                            # Extent HTML Reports
└── pom.xml
```

---

## 🧪 Test Coverage

### Login Module (5 Test Cases)
| Test ID | Test Case | Type |
|---------|-----------|------|
| TC_LOGIN_001 | Valid admin login | Smoke |
| TC_LOGIN_002 | Invalid credentials (Data-Driven) | Regression |
| TC_LOGIN_003 | Empty username validation | Regression |
| TC_LOGIN_004 | Empty password validation | Regression |
| TC_LOGIN_005 | SQL Injection blocked | Security |

### Policy Management Module (6 Test Cases)
| Test ID | Test Case | Type |
|---------|-----------|------|
| TC_POL_001 | Create new policy (Data-Driven) | Regression |
| TC_POL_002 | Policy status ACTIVE after creation | Regression |
| TC_POL_003 | Policy renewal | Regression |
| TC_POL_004 | Policy endorsement | Regression |
| TC_POL_005 | Policy cancellation | Regression |
| TC_POL_006 | Premium calculation | Regression |

### Claims Management Module (5 Test Cases)
| Test ID | Test Case | Type |
|---------|-----------|------|
| TC_CLM_001 | File new claim - FNOL (Data-Driven) | Regression |
| TC_CLM_002 | Claim status PENDING after filing | Regression |
| TC_CLM_003 | Claim approval → APPROVED status | Regression |
| TC_CLM_004 | Claim rejection → REJECTED status | Regression |
| TC_CLM_005 | Settlement processing → SETTLED status | Regression |

---

## 🛠️ Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| Java | 11 | Programming Language |
| Selenium WebDriver | 4.18.1 | Browser Automation |
| TestNG | 7.9.0 | Test Framework |
| Maven | 3.9+ | Build & Dependency Management |
| Apache POI | 5.2.5 | Excel Data-Driven Testing |
| ExtentReports | 5.1.1 | HTML Test Reports |
| WebDriverManager | 5.7.0 | Auto Driver Management |

---

## ⚡ How to Run

### Prerequisites
- Java 11+
- Maven 3.9+
- Chrome Browser

### Run All Tests
```bash
mvn clean test
```

### Run Specific Suite
```bash
mvn clean test -Dsurefire.suiteXmlFiles=src/test/resources/testng.xml
```

### Run on Firefox
```bash
mvn clean test -Dbrowser=firefox
```

---

## 📊 Framework Features

- ✅ **Page Object Model (POM)** — Reusable page classes, easy maintenance
- ✅ **Data-Driven Testing** — Excel-based test data using Apache POI
- ✅ **Hybrid Framework** — Combines POM + Data-Driven + TestNG
- ✅ **Parallel Execution** — TestNG parallel class execution
- ✅ **Auto Screenshot** — Captured on test failure
- ✅ **Extent HTML Reports** — Detailed test execution reports
- ✅ **Cross-Browser** — Chrome & Firefox supported
- ✅ **Thread-Safe** — ThreadLocal WebDriver for parallel runs
- ✅ **Config Management** — External config.properties

---

## 🏢 Domain Knowledge

**Insurance (Property & Casualty / Life Insurance)**
- Policy Lifecycle: New Business → Renewal → Endorsement → Cancellation
- Claims Lifecycle: FNOL → Investigation → Adjudication → Settlement
- Premium Calculation & Rating Logic
- Policy Administration System (PAS) Integration

---

## 📈 Results

- **16 Test Cases** automated across 3 modules
- **Regression time reduced by 40%** compared to manual execution
- **Test coverage improved** from 60% to 90% on Policy Management module
