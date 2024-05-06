# PKCE for API first
Using OpenId or Oauth2 for API only can be enabled by using PKCE. It marks a secure and tangible solution.

## The follow is illustrated as follows:

1. Client. Creates a verifier and calculates a SHA256 challenge.
2. Client. Initiates a session om the server using the challenge.
3. Server. Stores the challenge, and returns a session identifer. It also provides a link to an IDP.
4. Client. Use the URL to browse the IDP and authenticate.
5. Idp. Redirects back to server to associate the access token and refresh token with the sessionId.
6. Server. Provices response without any session information to the user that authentication is completed.
7. Client. Use sessionId and the verifier to request exchange of the token.
8. Server. Validates the verifier and recalculates the challenge. If match returns the token.

