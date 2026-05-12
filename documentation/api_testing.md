# API Testing - Technical Documentation

This section documents the backend validation for the Conduit system using Postman. Testing the API directly ensures that business rules are enforced at the server level, providing a robust security layer regardless of the Front-end implementation.

## 🛠️ API Test Scope
The Postman collection was structured to validate the full lifecycle of user interactions:

1. **Authentication (Auth):** User login validation and session persistence via Bearer Tokens.
2. **Articles:** Validation of success and error scenarios for creating new articles, and secure deletion (Delete).
3. **Comments:** Testing the posting of comments and the correct removal of user interactions.
4. **Registration:** Validation of the `POST /users` endpoint with unique data.

## 🚀 Technical Highlights & Automation
As a QA Engineer with a background in development, I implemented advanced Postman features to ensure a repeatable and isolated testing process:

* **Dynamic Data:** Used `{{$randomInt}}` to generate unique usernames and emails, preventing data collision and "already taken" errors during bulk execution.
* **Chained Requests:** Implemented scripts to automatically capture the authentication token from responses and apply it to subsequent requests (Articles/Comments).
* **Environment Management:** Utilized environment variables (`{{BASE_URL}}`, `{{token}}`) to allow seamless switching between local and demo environments.
* **Comprehensive Validation:** Verified status codes (200 OK, 201 Created, 422 Unprocessable Entity) and JSON payload structures.

### Evidence
The following image demonstrates the request setup in Postman, including the use of pre-defined variables and dynamic randomizers:

![Postman Registration Evidence](../../assets/images/postman_registration_test.png)

---

## How to Import and Run
1. Download the [conduit_collection.json](./api/Postman%20extended%20[Edemberg%20Rodrigues].postman_collection.json).
2. Import it into your Postman Workspace.
3. (Optional) Import the environment variables file if provided.
4. Click **Send** or use the **Collection Runner** to execute the full suite.