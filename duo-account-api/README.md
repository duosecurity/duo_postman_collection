# duo-account-api
## Duo Account API

The Duo Account API provides programmatic access to the administrative functionality of Duo Security's two-factor authentication platform.

The Account API lets developers integrate with Duo Security's platform at a low level. The API has methods for creating, retrieving, updating, and deleting the core objects in Duo's system: users, phones, hardware tokens, admins, and integrations.
Developers can write applications that programmatically read their Duo account's authentication logs, administrator logs, and telephony logs; read or update account settings; and retrieve reports and other information.
Review the API Details to see how to construct your first API request.

## Postman Configuration using Pre-built Templates

Setting Up Multiple Environments
Postman environments can be used to allow a user to change the properties/headers of a request on the fly. Since the Duo requests must have the authentication headers regenerated upon each new request, this works REALLY well with environments. Below is an example of how to set this up.

## Adding an environment:

1. In Postman, the Environment dropdown lives in the upper right. By default, no environments are configured. To add an environment, click the Eye icon, then click Add:

[<img src="image.png">](image.png)




















2. Add your specific ikey, skey, apihost as Variables and add your Accounts API integration keys in as the current values. 


![alt text](Account-api-env.png)


## Import Postman Environment Template

First, the Duo Account API Postman Environment template needs to be imported into the Postman application.
1. Open the Postman application, if it is not open already.
2. In the left panel, select the Environments tile. If there is no Environments tile displayed, select the ![alt text](image-2.png) tile at the bottom of the left panel and then make sure the toggle slider is enabled for the Environments sidebar item.





![alt text](Accounts-api-1.png)








3. Download this Postman Duo Account API Environment template file.
4. Select the Import button in the upper right of the Environments section.
5. Browse to the JSON file downloaded in step #3 above.
6. Select the new Duo Account API entry and verify that there are variables defined for:
ikey
skey
apihost


## Import Postman Collections Template

Second, the Duo Account API Postman Collections template needs to be imported into the Postman application.
1. Open the Postman application, if it is not open already.
2. In the left panel, select the Collections tile. If there is no Collections tile displayed, select the ![ ](image-4.png)tile at the bottom of the left panel and then make sure the toggle slider is enabled for the Collections sidebar item.






![alt text](Accounts-API.png)










3. Download this Postman Duo API Collections template file.
4. Select the Import button in the upper right of the Environments section.
5. Browse to the JSON file downloaded in step #3 above.
6. Select the new Duo Account API Collection entry and verify the Pre-request Script is populated.




![alt text](accounts-api-scripts.png)










7. Expand the Duo Account API Collection item to reveal two example requests.


## Using the Templates
Once the templates have been imported, they require the standard three pieces of information from a Duo Account API application integration.

## Adding the Duo API credentials
Navigate to the Duo Account API environment within Postman and update the Current value rows for each of the ikey, skey, and apihost with information from the Duo Account API integration from the account will be tested. Click the save button in the upper right if the values should be stored for future use after the Postman application has been closed.
