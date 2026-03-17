# 🏦 Guru99 Bank — Manual Testing Project

![Testing](https://img.shields.io/badge/Type-Manual%20Testing-blue)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Test Cases](https://img.shields.io/badge/Test%20Cases-149-green)
![Bugs](https://img.shields.io/badge/Bugs%20Reported-45-red)
![Environment](https://img.shields.io/badge/Environment-UAT-orange)

---

## 📌 Project Overview

This project represents a **Manual Testing** effort applied to the **Guru99 Demo Banking Application**. The goal is to validate core banking functionalities across multiple application versions through structured test case design, execution, and defect reporting.

The project follows a standard **Bug Life Cycle** — from test case design and execution, to bug reporting, retesting, and regression validation.

---

## 🌐 Application Under Test (AUT)

| Version | URL |
|---------|-----|
| V1 | https://demo.guru99.com/V1/ |
| V2 | https://demo.guru99.com/V2/ |
| V3 | https://demo.guru99.com/V3/ |

---

## 👥 QA Team

| Tester | Contribution |
|--------|-------------|
| Hajar Muhammad | Fund Transfer, Balance Enquiry, Mini Statement, Change Password |
| Nada Ahmed | New Customer, Edit Customer, Delete Customer, Security |
| Hussien Hamdy | Mini Statement, Change Password, Login |
| Abdelrhman Lotfy | Customized Statement, Balance Enquiry, Fund Transfer, Login |

---

## 🧪 Test Scope & Modules

The following modules were covered during this testing cycle:

| Module | Test Cases | Bugs Found |
|--------|-----------|------------|
| Fund Transfer | 26 | 16 |
| Balance Enquiry | 10 | 6 |
| Mini Statement | 10 | 8 |
| Change Password | 12 | 6 |
| New Customer (Add) | 18 | 1 |
| Edit Customer | 22 | 2 |
| Delete Customer | 3 | 1 |
| Customized Statement | 12 | 3 |
| Login | 3 | 1 |
| **Total** | **149** | **45** |

---

## 📂 Project Artifacts

| File | Description |
|------|-------------|
| `G99_Manual_Testing_Project.xlsx` | Full test case suite with steps, expected vs actual results, and execution status |
| `G99_BugReport_Manual_Testing_Project.xlsx` | Detailed bug report including severity, priority, status, and regression tracking |

---

## 📊 Test Execution Summary

### ✅ Test Cases

| Status | Count |
|--------|-------|
| Pass | ~110 |
| Fail | ~25 |
| Blocked | 5 |
| Not Tested | 9 |

### 🐛 Bug Report Summary

| Severity | Count |
|----------|-------|
| High | 15 |
| Medium | 18 |
| Low | 12 |

| Priority | Count |
|----------|-------|
| High | 20 |
| Medium | 14 |
| Low | 11 |

| Bug Status | Count |
|------------|-------|
| ReOpen | 24 |
| New | 10 |
| Closed | 4 |
| Fixed | 1 |
| Open | 4 |
| Not Fixed | 2 |

---

## 🔍 Key Defects Highlighted

| Bug ID | Module | Summary | Severity |
|--------|--------|---------|----------|
| BUG-01 | Withdrawal | System accepts negative withdrawal amounts | High |
| BUG-03 | Edit Customer | PIN displayed in plain text — Security Vulnerability | High |
| BUG-04 | Balance Enquiry | Valid account number returns broken page (HTTP Error) | High |
| BUG-27 | Fund Transfer | System accepts negative transfer amounts | High |
| BUG-37 | Fund Transfer | Fund Transfer success page loads blank/empty | High |
| BUG-42 | Edit Customer | HTTP 500 Internal Server Error on Edit Customer submit | High |
| BUG-44 | Customized Statement | From Date > To Date accepted without validation | High |
| BUG-45 | Change Password | Changed password does not allow login with new credentials | High |

---

## 🧩 Testing Types Applied

- **Functional Testing** — Verifying all module features work as specified
- **Negative Testing** — Validating system behavior with invalid, boundary, and edge-case inputs
- **Boundary Value Analysis (BVA)** — Account numbers (8–16 digits), password length, amount fields
- **Equivalence Partitioning** — Valid vs. invalid input classes per field
- **Security Testing** — PIN masking, unauthorized account access
- **Regression Testing** — Retesting fixed bugs for potential side effects
- **Smoke Testing** — Basic navigation and page load verification

---

## 🛠️ Test Environment

| Parameter | Details |
|-----------|---------|
| Testing Type | Manual (UAT) |
| Browsers | Google Chrome, Microsoft Edge |
| OS | Windows 10, Windows 11 |
| Test Management | Microsoft Excel |

---

## 📋 Bug Report Fields

Each reported bug includes the following information:

- **Bug ID** — Unique identifier (BUG-01 through BUG-45)
- **Summary** — Short description of the defect
- **Description** — Detailed explanation of the issue
- **Steps to Reproduce** — Clear reproduction steps
- **Expected Result** — What the system should do
- **Actual Result** — What the system actually did
- **Severity & Priority** — Impact classification
- **Status** — Current state in the Bug Life Cycle
- **Environment** — Browser, OS, and build info
- **Regression Status** — Pass / Fail / Not Tested after fix
- **Fixed In Version** — Version where fix was deployed

---

## 📐 Test Case Fields

Each test case includes:

- **TC ID** — Unique identifier (e.g., TC-FT-014, TC-BE-037)
- **Title & Description** — What is being validated
- **Preconditions** — Required state before execution
- **Test Steps** — Sequential execution steps
- **Priority** — High / Medium / Low
- **Expected Result** — Defined acceptance criteria
- **Actual Result** — Observed system behavior
- **Status** — Pass / Fail / Blocked / Not Tested
- **Reporter** — Assigned tester
- **Requirement ID** — Traceability to business requirements

---

## 📎 Notes

- Some **Edit Customer** test cases were marked as **Blocked** due to an HTTP 500 server error preventing further testing of that module.
- The **Balance Enquiry** and **Mini Statement** modules showed critical failures on valid account lookups — the system redirected to a broken page instead of displaying data.
- **Security concern (BUG-03):** PIN was exposed in plain text in the Edit Customer page. This was marked as **Fixed** and successfully retested.

---

> *This project was completed as part of a practical Software QA training exercise using the Guru99 Demo Banking platform.*
