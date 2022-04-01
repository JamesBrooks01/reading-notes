# Reading Assignment 15

## Authentication

---

### What is OAuth

---

- What is OAuth?
  - An Open-Standard Authorization Protocol.
- Give an example of what using OAuth would look like.
  - A user sending cloud-stored files via email when the two sevices are unrelated other than both supporting OAuth.
- How does OAuth work? What are the steps that it takes to authenticate the user?
  - Assuming a user is already signed in on one website, they then initiate a feature or transaction on another followed by;
    1. The first connects to the second on behalf of the user.
    2. The second provides a one-time use token unique to the transaction.
    3. The first gives this token to the client's software.
    4. The software presents this token to the authorization provider.
    5. If not authenticated, the user may be asked to authenticate, afterwards the user is asked to approve the transaction.
    6. The user approves on the first website.
    7. The user is given an approved token.
    8. The user provides the approved token to the first website.
    9. The first gives the approved token to the second as proof of authenticaion.
    10. The second allows the first to access the site on behalf of the user.
    11. The user sees a sucessful completed transaction.
- What is OpenID?
  - As a Stack Overflow commenter put it; OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans.

### Authorization and Authentication flows

---

- What is the difference between authorization and authentication?
  - Authentication is for verifying a user's identity, Authorization is for verifying what they have access to.
- What is Authorization Code Flow?
  - The method a server uses to exchange an Authorization Code for a Token.
- What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
  - An additional security measure for Authorization Code Flow, specifically for native apps and single-page apps.
- What is Implicit Flow with Form Post?
  - An alternative to Authorization Code Flow that provides Implicit Flow.
- What is Client Credentials Flow?
  - An Authentication and Authoriztion Flow for machines rather than people.
- What is Device Authorization Flow?
  - Machine authorization for input-constrained devices like with mobile devices and native apps.
- What is Resource Owner Password Flow?
  - An authorization that is only used for high trust applications where it requests the user to provide username and password.
  