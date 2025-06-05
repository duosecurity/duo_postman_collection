# Duo Generic OIDC Integration - Postman Collection

The **Duo Generic OIDC Integration** provides an OIDC standards-based interface for adding strong two-factor authentication to your web application. This integration enables Duo to act as an OpenID Provider (OP) for a Relaying Party (RP) application.

For more information about the Duo Generic OIDC integration, refer to the [Duo Documentation](https://duo.com/docs/sso-oidc-generic).

---

## 📦 Duo Generic OIDC Integration Postman Collection Template

This Postman collection is designed to help you easily test and validate the Duo Generic OIDC integration without needing to immediately integrate it into your application.

### 🔧 Requirements

To use the collection effectively, populate the following variables within the Postman Collection for the Duo Generic OIDC application integration being tested:

- `oidc_client_id` – The CLIENT ID for the Generic OIDC application integration
- `oidc_client_secret` – The CLIENT SECRET for the Generic OIDC application integration
- `oidc_apihost` – The API hostname for the Generic OIDC application integration
- `oidc_redirect_url` - The Relaying Party URL that is configured in the Generic OIDC application integration

A test tool, such as [OIDC Debugger](https://oidcdebugger.com/debug) can be used to mimic the OIDC Relaying Party application. The appropriate OIDC Redirect URL for the application/test tool needs to be configured in the Generic OIDC application integration within the Duo Admin Panel as well as in the `oidc_redirect_url` variable in the Postman Collection.

### Usage

The Duo Generic OIDC collection template is intended to provide a basic framework for testing/troubleshooting a Duo Generic OIDC integration. The collection template relies on the use of a third party testing tool called OpenID Connect Debugger.

The essential steps for using the OpenID Connect Debugger tools are:

1. Create a new Generic OIDC integration in Duo (or use an existing one, if available).
2. In the Generic OIDC integration configuration page:
     - Select the checkbox for Refresh Tokens
     - Make any adjustments to the **Absolute** and **Inactivity** Lifetime values 
     - Populate the **Sign-In Redirect URLs** with https://oidcdebugger.com/debug

    ![Screenshot of Generic OIDC integration token and redirect URL settings](/assets/images/duo-generic-oidc-integrations/integration_tokens_and_redirect.png)

    - Save the changes

3. Import the [Duo Generic OIDC integration collection template](/duo-generic-oidc-integrations/Duo%20Generic%20OIDC%20Integration%20v1.1.0.postman_collection.json) into Postman.
4. Update the Postman Collection variables with the information (api host, client id, client secret) specific to the Duo Generic OIDC integration.

> [!NOTE] 
> The api host is the hostname portion of any of the URL values from the Duo Generic OIDC integration configuration page)

    ![Screenshot of Postman Collection variables](/assets/images/duo-generic-oidc-integrations/variables.png)

5. Copy the **Authorization URL** from the Duo Admin Panel and paste it into the **Authorize URL** in the OpenID Connect Debugger site.
6. Copy the **Client ID** from the Duo Admin Panel and paste it into the **Client ID** field in the OpenID Connect Debugger site.
7. Add an `offline_access` scope to the OpenID Connect Debugger tool configuration (this is needed in order for Duo to know that a Refresh Token should be issued along with the normal Access Token).

   ![Screenshot of OIDC Debugger scope configuration](/assets/images/duo-generic-oidc-integrations/offline_access_scope.png)


8. Scroll down and select the SEND REQUEST button in the OpenID Connect Debugger tool.
9. Complete a Duo authentication with a user already enrolled in Duo with access to the Generic OIDC integration.
10. Copy the Authorization code from the OpenID Connect Debugger tool

    ![Screenshot of OIDC Debugger authorization code](/assets/images/duo-generic-oidc-integrations/auth_code.png)

11. Paste the **Authorization code** into the **Request Access Token** request within the Postman Duo Generic OIDC Integration Collection.

> [!TIP]
> How to enter auth code in Postman
> The {{oidc_auth_code}} Postman variable is local to the request. If you hover the mouse cursor over the variable identifier in Value column, a popup input box will appear.

    ![Screenshot of OIDC auth code variable definition](/assets/images/duo-generic-oidc-integrations/oidc_auth_code_variable.png)

12. Send the request.
13. Open the **Request New Token Using Refresh Token** request in Postman and **Send** it.

> [!NOTE]
> Variable values are automatically updated 
> There is no need to change any of the variable values in the request. A successful response from the Request Access Token request will automatically extract the necessary values from the response and update the appropriate variables.

14. Open the **Refresh Token Inspection** request in Postman and **Send** it.

> [!TIP]
> Additional Troubleshooting Option 
> A normal Access Token value can also be placed in the token value of the Refresh Token Inspection request as well.
    
---

🛠 Happy Testing!
