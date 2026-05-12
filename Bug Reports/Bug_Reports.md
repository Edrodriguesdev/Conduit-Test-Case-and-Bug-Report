# Bug Reports - Sign Up Functionality

This document logs the defects identified during the testing process of the Conduit Sign Up flow.

---

## 🐞 [BUG-001] Incorrect Redirection After Sign Up (Bypassing Verification)

**Severity:** Critical | **Priority:** High  
**Status:** Open  
**Component:** Authentication / Registration Flow

### Description
After a successful Sign Up attempt, the system is redirecting the user directly to the **Global Feed** page instead of the **Complete Registration** page. This prevents the user from entering the 6-digit verification code sent via email, violating the security requirement.

### Environment
*   **OS:** Windows 10 Pro x64
*   **Browser:** Chrome 87.0.4280.88
*   **App Version:** Demo Environment

### Steps to Reproduce
1.  Open the [Conduit Demo Site].
2.  Click the **Sign up** link in the navigation bar.
3.  Fill in all required fields (Username, Email, Password, Confirm Password) with valid data.
4.  Click the **Sign up** button.
5.  Observe the page redirection.

### Expected Result
The user should be redirected to the **"Complete Registration"** page to enter the 6-digit verification code.

### Actual Result
The user is immediately redirected to the **Global Feed** page, logged in without email verification.


### Technical Observation (Dev Insights)
*   **Network Tab:** The `POST /api/users` request returns a `201 Created` status, but the front-end router is pointing to `/` instead of `/verify-email`.
*   **Security Risk:** This bug allows unverified emails to access the platform's features.

---

## Attachment 

Link to image
https://freeimage.host/i/BbZxB71

### Evidence
> `![Bug Evidence](../assets/images/Bug_After_Signup_Redirect_to_Homepage)`