# Duo Device API – Postman Collection

This project provides a Postman Collection and Environment to help you explore the [Duo Device API](https://duo.com/docs/deviceapi).  

The Device API allows you to create and manage **device caches** from a Management System, which can be used with Duo Trusted Endpoints.

---

## Contents

- `duo-device-api.postman_collection.json` – Postman collection with all Device API endpoints.  
- `duo-device-api.postman_environment.json` – Postman environment for configuring your credentials and host values.  
- Pre-request script (included in the collection) – generates the **Date** and **Authorization** headers automatically.  

---

## Prerequisites

1. A Duo account with access to the **Device API**.  
2. Your Device API credentials from the [Duo Admin Panel](https://admin.duosecurity.com/):  
   - Integration key (`ikey`)  
   - Secret key (`skey`)  
   - Management system key (`mkey`)  
   - API hostname (e.g. `api-XXXXXXXX.duosecurity.com`)  
3. [Postman](https://www.postman.com/downloads/).  

---

## Setup

1. Import both JSON files into Postman:  
   - `duo-device-api.postman_collection.json`  
   - `duo-device-api.postman_environment.json`  

2. In Postman, select the **Duo Device API Env** environment and update the following variables:  
   - `ikey` – your integration key  
   - `skey` – your secret key  
   - `mkey` – your management system key  
   - `api_hostname` – your Duo API hostname (without `https://`)  

3. The collection already includes a **Pre-request Script** that will:  
   - Add the required `Date` header (RFC 2822 format).  
   - Compute the HMAC-SHA1 signature using your `skey`.  
   - Generate the `Authorization` header (`Basic ikey:signature`).  

No manual signing is needed — Postman handles it automatically. ✅  

---

## Available Requests

The collection contains the following requests:

- **Create Device Cache**  
- **Add Devices to Cache**  
- **Retrieve Devices from Cache**  
- **Delete Devices from Cache**  
- **Activate Device Cache**  
- **Delete Device Cache**  
- **List All Device Caches**  
- **Retrieve Device Cache**  

Each request references variables from the environment for easy reuse.  

---

## Example Usage

1. Create a new device cache with **Create Device Cache**.  
2. Add devices to the cache with **Add Devices to Cache**.  
3. Verify the devices with **Retrieve Devices from Cache**.  
4. Activate the cache with **Activate Device Cache**.  

---

## Notes

- The `authorization_header` and `date_header` are generated dynamically and do not need to be set manually.  
- Ensure your system clock is correct — Duo requires accurate timestamps for signing.  
- Duo’s official documentation: [https://duo.com/docs/deviceapi](https://duo.com/docs/deviceapi)  

---

## License

This project is provided as-is under the MIT license.  
