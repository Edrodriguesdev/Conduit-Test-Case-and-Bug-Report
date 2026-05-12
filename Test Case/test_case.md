# Test Cases - Sign Up Functionality

This document contains the test scenarios mapped to validate the user registration process in the Conduit system, following the business rules defined in the [User Story](./User_story.md).

## 1. Test Scenarios Matrix - Sign Up

| ID | Test Scenario | Priority | Expected Result |
|:---|:---|:---|:---|
| **C66** | Visibility of the "Sign up" link for logged-out users | High | Link visible in the navigation bar |
| **C67** | Registration via [Sign up] button click | High | Registration processed successfully |
| **C68** | Registration via [Enter] key | Medium | Registration processed successfully |
| **C69** | Registration with no data conflicts | High | Registration completed and verification email sent |
| **C70** | Post-registration redirection flow | Critical | Redirection to the 6-digit code verification page |
| ****C71** | "Have an account?" link (Redirection) | Low | Correct redirection to the Login page |
| **C72** | Validation of already registered Username | Medium | Error: "This username is taken." |
| **C73** | Validation of invalid Username format | High | Format error according to requirements |
| **C74** | Validation of already registered Email | High | Error: "This email is taken. Want to log in?" |
| **C75** | Validation of invalid Email format | High | Error: "This email does not seem valid." |
| **C76** | Validation of empty Password field | Critical | Error: "Password can’t be blank." |

---

## 2. Technical Detailing (Samples)

### TC-C70: Full Success Flow
**Pre-condition:** User must have unique credentials (email and username).
1. Fill in all fields with valid data.
2. Click on the [Sign up] button.
**Expected Result:** The system should register the user and automatically navigate to the 6-digit code entry screen.

### TC-C76: Required Field Validation
1. Leave the password field blank.
2. Fill in all other required fields.
3. Attempt to submit the form.
**Expected Result:** The form submission should be blocked, and the specific "Password can’t be blank" error message must be displayed.

### TC-C74: Duplicate Email Validation
**Pre-condition:** A user is already registered with the email `test@example.com`.
1. Fill out the Sign Up form.
2. In the Email field, enter `test@example.com`.
3. Click on the [Sign up] button.
**Expected Result:** The system must prevent registration and display the message: "This email is taken. Want to log in?"