# API Testing - Registration Flow

This section documents the backend validation for the Sign Up process using Postman. Testing the API directly ensures that business rules are enforced at the server level, regardless of the Front-end.

## 🚀 Postman Collection Overview
I developed a suite of tests to validate the `POST /users` endpoint. To ensure tests are repeatable and isolated, I implemented dynamic data generation.

### Key Technical Features:
*   **Dynamic Variables:** Used `{{$randomInt}}` to generate unique usernames and emails, avoiding "already taken" errors during bulk execution.
*   **Environment Management:** Utilized `{{BASE_URL}}` and global variables to switch between local and demo environments seamlessly.
*   **Payload Validation:** Verified the required JSON structure for the Conduit API.

### Evidence
The following image demonstrates the request setup in Postman, including the use of pre-defined variables and dynamic randomizers:

![Postman Registration Evidence](../../assets/images/postman_registration_test.png)

---

## How to Import and Run
1. Download the [conduit_collection.json](./api/Postman extended [Edemberg Rodrigues].postman_collection.json).
2. Import it into your Postman Workspace.
3. (Optional) Import the environment variables file if provided.
4. Click **Send** to execute the registration test.