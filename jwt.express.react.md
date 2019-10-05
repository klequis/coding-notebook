- userLogout
- userLogoutRequest
- userValidate
* userValidateRequest
- userLogin
- loginFailed
- userLoginRequest
- userRegister
- userRegisterRequest
- passwordUpdate
- passwordUpdateRequest



SERVER
node passport on server

they use a session, we have session: false
they use redis with connect-redis to persist sessions through app/server restart


JWT Validation
--------------
- Check that the JWT is well formed
- Check the signature
- Validate the stardard claims
- Check application permissions (scopes)

Verify Access Tokens for Custom APIs
------------------------------------
- parse the JWT (using node-jsonwebtoken)
- Check the Signature Alogrithm - the alg prop must match the expected one
  - jsonwebtokens has an 'algorithms' argument
- Verify the signature
  - read jsonwebtokens doc
  
Validate the Claims
-------------------
- exp: current date/time before exp
- iss: value must match. what should the value be in our case? Seems https://dronemadness.live/?
- Check permissions: involes using Auth0 scopes. We would need to create our own since we don't use Auth0


why aren't we using the Bearer schema

jsonwebtokens
-------------
- only object literals are checked for JSON validity, strings & buffers are not
