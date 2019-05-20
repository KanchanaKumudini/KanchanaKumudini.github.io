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
![image](https://user-images.githubusercontent.com/50174329/57985495-71810d00-7a86-11e9-84b3-2ddd63128cba.png)

User Consent Page will show the resources of the user account that can be accessed by the application. 
![image](https://user-images.githubusercontent.com/50174329/57985580-92962d80-7a87-11e9-8f9d-b1287a885988.png)

Click Continue then facebook will redirect the browser to the Redirection Endpoint URL which has been defined in the app settings and along with the URL, it will send the query parameter code, which is the authorization code. 
Get the URL from the browser
http://localhost:8080/facebookapp/callback?code=AQC_SqeuC6SaYsJZKTk1FdDCBtTZXxRrzrwsOWUkG3OoL6axiNWF1Xo8Ri3Y6IwRcYC-YSKyySs3BUc1eA4GCyoM2Z7WnsDyGwk5G-5aHS0R03_gcsD6mkx3K8Q8hL248pX817QVRbWBsYy3Wip1Y0tM7Oeg7a5ggC3iOvGx1WdPtxXIPH20a9xy5gm2_7vw3xDge_Nng2ZJt791Bn85EGT69w5sWqD0RrRkMTYSgvGLSlldZUHFUYyWE8eW2z5NByJByCyi1Mm6EDYjIcgYGyI26np4JJlYCxIb-Q7Onph8pmWynoatA1XBrDNsqw5RvKQ#_=_

Step 3 - Obtaining the Access Token
Request an OAuth access token from facebook, which can be used to access user resources. Send a HTTP POST request to the Token Endpoint of facebook using the authorization code received in the previous step to https://graph.facebook.com/oauth/access_token. 

Prepare the parameter values. (App ID=410788766438800, App Secret=68d00ce4b68af62439703eca89829748, App ID:App Secret=410788766438800:68d00ce4b68af62439703eca89829748, Base64 App ID: App Secret=NDEwNzg4NzY2NDM4ODAwOjY4ZDAwY2U0YjY4YWY2MjQzOTcwM2VjYTg5ODI5NzQ4)

Authentication: Basic NDEwNzg4NzY2NDM4ODAwOjY4ZDAwY2U0YjY4YWY2MjQzOTcwM2VjYTg5ODI5NzQ4
Use a HTTP Client browser plugin like RESTClient. 
![image](https://user-images.githubusercontent.com/50174329/57986084-dbe97b80-7a8d-11e9-8ed7-4b116a1a92e7.png)

