# OAuth2-cheat-sheet

Resources and References I've found: 
* https://stormpath.com/blog/secure-your-rest-api-right-way
* https://stormpath.com/blog/token-auth-spa
* https://stormpath.com/blog/the-problem-with-api-authentication-in-express
* https://blog.risingstack.com/web-authentication-methods-explained/
* https://www.digitalocean.com/community/tutorials/an-introduction-to-oauth-2
* https://oauth.net/2/
* https://aaronparecki.com/oauth-2-simplified/

###Oauth2 Steps: For Grant type auth code

1. The application requests authorization to access service resources from the user
  
  Aka user logs on, clicks "login with provider" (eg. facebook, twitter, etc...)

2. If the user authorized the request, the application receives an authorization grant
 
 User gets little window and "authorizes request", API server sends back auth code

3. The application requests an access token from the authorization server (API) by presenting authentication of its own identity, and the authorization grant
 
 The app uses the auth code to request an access token + its app identity

4. If the application identity is authenticated and the authorization grant is valid, the authorization server (API) issues an access token to the application. Authorization is complete.

  The app proves itself and receives an access token

5. The application requests the resource from the resource server (API) and presents the access token for authentication

6. If the access token is valid, the resource server (API) serves the resource to the application
