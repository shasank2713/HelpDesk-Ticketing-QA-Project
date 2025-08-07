# HelpDesk Support System – API Testing 

This is a real-time QA project that simulates API testing for a HelpDesk support system using the [ReqRes.in](https://reqres.in/) public API. The goal of the project is to test core ticketing system features such as login, user listing, create, update, and delete operations.

---

## 📌 Project Details

- **Tools Used:**  
  - Postman  
  - Excel (Test Case Documentation)  
  - Jira (Bug Tracking - Optional)  
  - GitHub (Version Control)  
  - Jenkins (CI/CD Automation with Newman)

---

## ✅ Modules Covered

| Module Name         | API Endpoint                         | Method |
|---------------------|--------------------------------------|--------|
| Login               | `/api/login`                         | POST   |
| Get All Users       | `/api/users?page=2`                  | GET    |
| Create Ticket/User  | `/api/users`                         | POST   |
| Update Ticket/User  | `/api/users/2`                       | PUT    |
| Delete Ticket/User  | `/api/users/2`                       | DELETE |

---

## 📋 How to Use

1. Open **Postman**
2. Import the file `Postman_Collection.json`
3. Run each API request manually or using Collection Runner
4. Refer to `TestCases.xlsx` for expected outcomes

---

## 🔁 CI/CD Integration – Jenkins + Newman

This project includes Jenkins integration to automate API testing using Newman (Postman CLI).

### ⚙️ Jenkins Setup Overview

- Jenkins installed on EC2 (Ubuntu)
- Freestyle job created for this project
- GitHub repo connected to Jenkins
- Newman CLI used to run the Postman collection

### ▶️ Jenkins Build Steps

1. Git pull latest repo
2. Run below command:
   ```bash
   newman run Postman_Collection.json --reporters cli,html --reporter-html-export results.html
   ```
3. Archive and publish `results.html`
4. Optionally send email/slack notifications

---

## 📊 Sample Test Case (Excel)

| Test Case ID | Title                             | Method | Expected Result             | Status |
|--------------|-----------------------------------|--------|-----------------------------|--------|
| TC_POST_01   | Login with valid credentials      | POST   | 200 OK with token           | Pass   |
| TC_GET_01    | Get users – page 2                | GET    | 200 OK with users list      | Pass   |
| TC_POST_02   | Create a new user/ticket          | POST   | 201 Created with ID         | Pass   |
| TC_PUT_01    | Update user info                  | PUT    | 200 OK with updated info    | Pass   |
| TC_DELETE_01 | Delete user by ID                 | DELETE | 204 No Content              | Pass   |

---

## 📢 Outcome

All APIs were tested using valid, invalid, and edge-case data. Test cases passed successfully with correct status codes and response payloads. With Jenkins integration, API testing is now automated and repeatable – suitable for CI/CD environments and real-world projects.

---

## 🙋‍♂️ Author

**Shasank Sinha**  
Manual QA Tester | API Testing | CI/CD  
📧 [coolshasank.sinha@gmail.com](mailto:coolshasank.sinha@gmail.com)
