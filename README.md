# keycloak-granular-permissions-postman-api
This project is having postman scripting to setup the group data with granular permissions on a keycloak instance. 

Import the postman collection from the [github location](https://github.com/lokeshrangineni/keycloak-granular-permissions-setup-using-rest-apis/blob/main/Keycloak-Granular-Permissions.postman_collection.json)

* Open postman --> Check for the scratch pad 
* Import option --> click on import --> select the file mentioned in the above URL --> import
* Once you import into postman --> Double-click on collection(folder) you imported
  * Go to the variables tab and Update variables
  * Make sure that you are referring to the correct Keycloak environment where you want to create the group data
  * Click on Run to run the collection
  * Check the progress on postman console
  * Once the script is completed validate the data on Keycloak.
