# HelpDesk Support System – API Testing 

This is a real-time freelance QA project that simulates API testing for a HelpDesk support system using the [ReqRes.in](https://reqres.in/) public API. The goal of the project is to test core ticketing system features such as login, user listing, create, update, and delete operations.

---

## 📌 Project Details

- **Client:** Freelance Simulation (Based on Real-Time Scenarios)
- **Tools Used:**  
  - Postman  
  - Excel (Test Case Documentation)  
  - Jira (Bug Tracking - Optional)  
  - GitHub (Version Control)

---

## ✅ Modules Covered

| Module Name         | API Endpoint                         | Method |
|---------------------|--------------------------------------|--------|
| Login               | `/api/login`                         | POST   |
| Get All Users       | `/api/users?page=2`                  | GET    |
| Create Ticket/User  | `/api/users`                         | POST   |
| Update Ticket/User  | `/api/users/2`                       | PUT    |
| Delete Ticket/User  | `/api/users/2`                       | DELETE |


## 📋 How to Use

1. Open **Postman**
2. Import the file `Postman_Collection.json`
3. Run each API request manually or using Collection Runner
4. Refer to `TestCases.xlsx` for expected outcomes

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

All APIs were tested using valid, invalid, and edge-case data. Test cases were passed successfully with correct status codes and response payloads. This project is helpful for validating API behavior in a support system scenario.

---

## 🙋‍♂️ Author

**Shasank Sinha**  
Manual QA Tester | API Testing | 
📧 [coolshasank.sinha@gmail.com](mailto:coolshasank.sinha@gmail.com)

