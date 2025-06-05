# Duo OIDC Auth API - Postman Collection

The **Duo OIDC Auth API** provides an OIDC standards-based interface for adding strong two-factor authentication to your web application. This API supports the **Duo Universal Prompt**, which leverages a new OIDC-compliant authentication protocol to perform secure and user-friendly authentication.

For more information about the Duo OIDC Auth API, refer to the [Duo Documentation](https://duo.com/docs/universal-prompt).

---

## 📦 Duo OIDC Postman Collection Template

This Postman collection is designed to help you easily test and explore the Duo OIDC Auth API without needing to immediately integrate it into your application.

### 🔧 Requirements

To use the collection effectively, pair it with a **Postman Environment** that contains the following variables for the OIDC application integration being tested:

- `IKEY` – Integration Key for the application
- `SKEY` – Secret Key for the application
- `APIHOST` – API hostname for the Duo OIDC Auth integration

These variables are used in the authentication headers and API calls throughout the collection.

---

## 📚 Additional Resources

For detailed explanations, usage instructions, and screenshots, please refer to the `README.md` files under the [duo-admin-api](https://duo.com/docs/administration-api) or [duo-auth-api](https://duo.com/docs/authapi) documentation.

---

## 💡 Tip

The Duo OIDC API supports the **Universal Prompt**—an improved user interface for two-factor authentication. Be sure to review your configuration to ensure compatibility and readiness for Universal Prompt.

---

🛠 Happy Testing!
