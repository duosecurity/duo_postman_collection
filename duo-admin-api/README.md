# duo-admin-api
## Duo Admin API

The Duo Admin API provides programmatic access to the administrative functionality of Duo Security's two-factor authentication platform.

The Admin API lets developers integrate with Duo Security's platform at a low level. The API has methods for creating, retrieving, updating, 
and deleting the core objects in Duo's system: users, phones, hardware tokens, admins, and integrations.
Developers can write applications that programmatically read their Duo account's authentication logs, administrator logs, and telephony logs; 
read or update account settings; and retrieve reports and other information.
Review the API Details to see how to construct your first API request.

## Postman Configuration using Pre-built Templates

Setting Up Multiple Environments
Postman environments can be used to allow a user to change the properties/headers of a request on the fly. Since the Duo requests must have 
the authentication headers regenerated upon each new request, this works REALLY well with environments. Below is an example of how to set this up.

## Adding an environment:

1. In Postman, the Environment dropdown lives in the upper right. By default, no environments are configured. To add an environment, click the Eye icon, then click Add:

[<img src="/assets/images/duo-admin-api/image.png">](/assets/images/duo-admin-api/image.png)

2. Add your specific ikey, skey, apihost as Variables and add your Admin/Auth API integration keys in as the current values.

![alt text](../assets/images/duo-admin-api/image-1.png)

## Import Postman Environment Template

First, the Duo Admin API Postman Environment template needs to be imported into the Postman application.
1. Open the Postman application if it is not open already.
2. In the left panel, select the Environments tile. If there is no Environments tile displayed, select the ![alt text](../assets/images/duo-admin-api/image-2.png) tile at the bottom of the left panel and then make sure the toggle slider is enabled for the Environments sidebar item.

![alt text](../assets/images/duo-admin-api/image-3.png)

3. Download this [Postman Duo Admin API Environment template](/duo-admin-api/Duo%20Admin%20API.postman_environment.json) file.
4. Select the Import button in the upper right of the Environments section.
5. Browse to the JSON file downloaded in step #3 above.
6. Select the new Duo Admin API entry and verify that there are variables defined for:
ikey
skey
apihost


## Import Postman Collections Template

Second, the Duo Admin API Postman Collections template needs to be imported into the Postman application.
1. Open the Postman application if it is not open already.
2. In the left panel, select the Collections tile. If there is no Collections tile displayed, select the ![ ](../assets/images/duo-admin-api/image-4.png) tile at the bottom of the left panel and then make sure the toggle slider is enabled for the Collections sidebar item.

![alt text](../assets/images/duo-admin-api/image-5.png)

3. Download this [Postman Duo API Collections template](/duo-admin-api/Duo%20Admin%20API%20v4.1.0.postman_collection.json) file.
4. Select the Import button in the upper right of the Environments section.
5. Browse to the JSON file downloaded in step #3 above.
6. Select the new Duo Admin API Collection entry and verify the Pre-request Script is populated.

![alt text](../assets/images/duo-admin-api/image-6.png)

7. Expand the Duo Admin API Collection item to reveal all the sample requests organized into folders corresponding to the individual API endpoints.

## Using the Templates
Once the templates have been imported, they require the standard three pieces of information from a Duo Admin API application integration.

## Adding the Duo API credentials
Navigate to the Duo Admin API environment within Postman and update the Current value rows for each of the ikey, skey, and apihost with information from the Duo Admin API integration from the account will be tested. Click the save button in the upper right if the values should be stored for future use after the Postman application has been closed.
