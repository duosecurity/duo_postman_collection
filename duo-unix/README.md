
# Duo Unix – Postman Collection

This repository provides a **Postman Collection** to simulate and test the **Duo Unix integration** without needing to install the Duo Unix client on a Unix server or workstation.

Duo Unix leverages a **REST API** interface similar to the [Duo Auth API](https://duo.com/docs/authapi), and this collection allows you to quickly understand, test, and demonstrate the integration flow.

---

## 🔧 Requirements

To use this collection effectively, you'll need to set up a corresponding **Postman Environment** that defines the following variables:

- `IKEY` – Your integration key  
- `SKEY` – Your secret key  
- `APIHOST` – Your API hostname (e.g., `api-xxxxx.duosecurity.com`)

These values should correspond to the Duo Unix integration being tested.

---

## 🧪 What You Can Do

- Simulate Duo Unix login requests
- Verify integration with your Duo tenant without installing software
- Test authentication flows with pre-configured accounts and responses

---

## 📚 Need More Details?

For a deeper dive, screenshots, and usage tips, refer to the following repositories:

- [Duo Admin API – README](../duo-admin-api/README.md)
- [Duo Auth API – README](../duo-auth-api/README.md)

---

## 📌 Note

This Postman collection is intended for **testing and demonstration** purposes only. It does not replace actual deployment or client-side behavior.
