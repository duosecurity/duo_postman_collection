# Cisco Duo Postman API Collections

## Overview
This repository contains [Postman](https://www.postman.com/home) collections and environment configurations to interact with the various Duo APIs for managing users, groups, authentication logs, applications, and more.

The collections are designed to help security administrators and developers test and automate administrative tasks within Duo Security. In addition, the collections assembled here are an effort to provide examples of how to interact with each of the Duo API endpoints.

---

## Prerequisites

Before using this collection, ensure you have:

1. **Duo Admin Panel Access**:
   - You need API credentials (Integration Key, Secret Key, and API Hostname).
   - Enable **[Admin API](https://duo.com/docs/adminapi)**/**[Auth API](https://duo.com/docs/authapi)**/**[OIDC API](https://duo.com/docs/oauthapi)**/**[UNIX](https://duo.com/docs/loginduo)** in the [Duo Admin Panel](https://admin.duosecurity.com).
   - The API requires **Duo MFA** with an Admin role enabled.

2. **Postman Installed**:
   - Download [Postman](https://www.postman.com/downloads/).

---

## Setup & Installation

### 1. Clone Repository
```bash
git clone https://github.com/shhv/duo_postman_api_collections.git
cd duo_postman_api_collections
```

### 2. Import Postman Collection & Environment
- Open **Postman** → Click **Import** → Select the collection JSON file (E.g : `Duo-Admin-API-Collection.json`).
- Import the environment JSON (E.g : `Duo-Environment.json`).

### 3. Configure Environment Variables
Set the following environment variables in Postman:

| Variable Name        | Description                  | Example |
|----------------------|------------------------------|---------|
| `DUO_API_HOSTNAME`   | Your Duo API hostname       | `api-xxxx.duosecurity.com` |
| `DUO_INTEGRATION_KEY`| Your Integration Key        | `DIXXXXXXXXXXXXXXXXXX` |
| `DUO_SECRET_KEY`     | Your Secret Key (store securely) | `xxxxxxxxxxxxxxxxxxxx` |

---

## Authentication & Security

### API Authentication
Duo API uses **HMAC-SHA1** request signing. Each request must include a properly formatted **Authorization Header**.

Postman pre-request scripts handle this automatically by generating:
- The **Date** header.
- The **Signature** using your Secret Key.


### Important Security Notes
- **Never share or expose your Secret Key** in a public repository.
- Use **Postman’s variable encryption** or store secrets securely.
- If credentials are compromised, **revoke & regenerate** in Duo Admin Panel.

---

## How to Use

### Using Postman UI
1. Select the **Duo-xxx-API-Postman_Collection** in Postman.
2. Choose an **API request** (e.g., `Get Users`, `Get Logs`).
3. Ensure your **environment is set** with API credentials.
4. Click **Send** and view the response.

---

## Collection Structure

```
/duo-xxx-api
├── Duo-xxx-API-postman_collection.json
├── Duo-xxx-postman_environment.json
│── README.md
```

- **collections/** → Contains the Postman collection for Duo Admin API.
- **environments/** → Stores the environment JSON file with API credentials.
- **scripts/** → Custom scripts for authentication and request signing.

---

## Troubleshooting

**Common Issues & Fixes**

| Issue                 | Cause                          | Solution |
|----------------------|------------------------------|---------|
| `401 Unauthorized`  | Incorrect API key            | Verify `DUO_INTEGRATION_KEY` & `DUO_SECRET_KEY` |
| `403 Forbidden`     | Insufficient permissions     | Ensure Admin API is enabled in Duo Dashboard |
| `500 Internal Server Error` | Incorrect request format | Double-check API request body & parameters |

For more troubleshooting, check 
* [Duo Admin API Documentation](https://duo.com/docs/adminapi).
* [Duo Auth API Documentation](https://duo.com/docs/authapi)
* [Duo OIDC API Documentation](https://duo.com/docs/oauthapi)
* [Duo Unix Documentation](https://duo.com/docs/loginduo)

---

## Contributing
- If you find issues or have suggestions, feel free to open a pull request.
- Follow [Duo's API guidelines](https://duo.com/docs/adminapi#api-guidelines).

---

## License
This project is open-source and follows the **MIT License**.
