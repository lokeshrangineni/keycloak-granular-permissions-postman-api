### Assumptions
* This script is tested using keycloak version - 21.0.2.
* As part of keycloak version 21.0.2, granular permissions is a preview feature. We need to enable preview features while running the keycloak instance. Please find [documentation here](https://www.keycloak.org/docs/latest/server_admin/#_fine_grain_permissions). This feature is required for this script to work without any errors.
* This script creates groups, roles, policies, permissions. etc., so it is expected to have elevated privileges on keycloak to run this script.
* for IDP customers, we are not adding any users. 

### Setup and Running the script using Postman
This project is having postman scripting to set up the group data with granular permissions on a keycloak instance. 

Import the postman collection from the [github location](https://github.com/lokeshrangineni/keycloak-granular-permissions-setup-using-rest-apis/blob/main/Keycloak-Granular-Permissions.postman_collection.json)

* Open postman --> Check for the scratch pad 
* Import option --> click on import --> select the file mentioned in the above URL --> import
* Once you import into postman --> Double-click on collection(folder) you imported
  * Go to the variables tab and Update variables
  * Make sure that you are referring to the correct Keycloak environment where you want to create the group data
  * Click on Run to run the collection
  * Check the progress on postman console
  * Once the script is completed validate the data on Keycloak.


### Documentation of variables.

| Variable Name | Description | Example |
| --- | --- | --- |
| keycloak_url_prefix | Prefix of the keycloak URL where you want to setup the data.|http://localhost:8080|
| tokenRealm | Realm to get the token for creating the data | master |
| username | username to get the token for creating the data | admin |
| password | password to get the token for creating the data | password |
| realm | realm where the groups will be created | Redhat-external |
| parentGroupName | Parent group name used to create the data | customer1 |
| orgAttributeName | org_name attribute with the value of this variable will be added to group | IDP Customer |
| orgAttributeID | org_id attribute with the value of this variable will be added to group | 1234 |
| addingGroupAdmin.UserName | A user with this user name will be added as admin of the group  | customer1Admin1 |
| addingGroupAdmin.Password | A user with this password will be added as admin of the group  | password |
| addingGroupAdmin.Email | A user with this email will be added as admin of the group | customer1Admin1@redhat.com |