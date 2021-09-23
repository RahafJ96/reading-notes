#  Authentication



## [What is OAuth](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)


1. **What is OAuth?**
- OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial

2. **Give an example of what using OAuth would look like.**

- The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website


3. **How does OAuth work? What are the steps that it takes to authenticate the user?**


- The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
- The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
- The first site gives this token and secret to the initiating user’s client software.
- The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
- If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
- The user approves (or their software silently approves) a particular transaction type at the first website.
- The user is given an approved access token (notice it’s no longer a request token).
- The user gives the approved access token to the first website.
- The first website gives the access token to the second website as proof of authentication on behalf of the user.
- The second website lets the first website access their site on behalf of the user.



4. **What is OpenID?**

- OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans.



## [Authorization and Authentication flows](https://auth0.com/docs/flows)



1. **What is the difference between authorization and authentication?**

- Authentication confirms that users are who they say they are. Authorization gives those users permission to access a resource.

2. **What is Authorization Code Flow?**

- exchanges an Authorization Code for a token.

3. **What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?**

- provides a version of the Authorization Code Flow

4. **What is Implicit Flow with Form Post?**

- is intended for Public Clients, or applications which are unable to securely store Client Secrets.

5. **What is Client Credentials Flow?**

- is a server to server flow. There is no user authentication involved in the process. In fact there is no user at all, the resulting access tokens will not contain a user, but will instead contain the Client ID as subject (if not configured otherwise).

6. **What is Device Authorization Flow?**

- is an OAuth 2.0 extension that enables devices with no browser or limited input capability to obtain an access token. This is commonly seen on Apple TV apps, or devices like hardware encoders that can stream video to a YouTube channel.

7. **What is Resource Owner Password Flow?**

- The Resource Owner Password Credentials flow allows exchanging the username and password of a user for an access token and, optionally, 
- The primary difference is that the user’s password is accessible to the application. This requires strong trust of the application by the user.

