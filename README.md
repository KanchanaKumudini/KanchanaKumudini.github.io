# KanchanaKumudini.github.io
MS18912258
Step 1 - Registering the Client App in Facebook Developer Website
Create an application using https://developers.facebook.com/ and add the new application.
![image](https://user-images.githubusercontent.com/50174329/57983406-1394fb00-7a6f-11e9-8b90-79cade7a4ef1.png)
Insert display name and the contact email to create the application.
![image](https://user-images.githubusercontent.com/50174329/57983676-750a9900-7a72-11e9-866e-940bd765a2f6.png) 
Associate “Facebook Login” with the application.
![image](https://user-images.githubusercontent.com/50174329/57983857-e8f97100-7a73-11e9-986a-9abe31898448.png)
Type the Redirection Endpoint URL. 
![image](https://user-images.githubusercontent.com/50174329/57984884-c10f0b00-7a7d-11e9-8886-fd7162c84212.png)
Find the App ID and the App Secret of the application.
![image](https://user-images.githubusercontent.com/50174329/57984994-316a5c00-7a7f-11e9-9c48-fd77e09e9a2a.png)
Complete registering the application in facebook and get the App ID and App Secret of the application and also the Redirection Endpoint URL. (App ID:410788766438800, App Secret: 68d00ce4b68af62439703eca89829748, Redirection Endpoint URL http://localhost:8080/facebookapp/callback)
Step 2 - Obtaining the Authorization Code
Send a HTTP GET request to the Authorize Endpoint using https://www.facebook.com/dialog/oauth with the following parameters.
https://www.facebook.com/dialog/oauth?response_type=code&client_id=410788766438800&redirect_uri=http%3A%2F%2Flocalhost%3A8080%2Ffacebookapp%2Fcallback&scope=public_profile%20user_posts%20user_friends%20user_photos
Log into facebook.
