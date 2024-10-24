**Tags**: #WebSecurity #CSRF #CyberSecurity #WebDevelopment

---

### Definition

**Cross-Site Request Forgery (CSRF)** is a type of web security vulnerability where an attacker tricks a user into performing actions on a web application in which they are authenticated, without the user's intention. This can lead to unauthorized actions such as data modification, transactions, or account changes.

### How CSRF Works

1. **Authentication**: The user logs into a trusted website, obtaining an authenticated session (e.g., via cookies).
2. **Malicious Request**: The attacker crafts a request that performs an unwanted action on the trusted site.
3. **Execution**: The attacker induces the user to submit the malicious request (e.g., through a hidden form, image tag, or script).
4. **Action Performed**: The trusted site processes the request using the user's authenticated session, executing the unintended action.

### Common Targets

- **Financial Transactions**: Initiating transfers or payments.
- **Account Management**: Changing email addresses, passwords, or other sensitive settings.
- **Content Management**: Posting or deleting content without authorization.
- **Privilege Escalation**: Altering user roles or permissions.

### Prevention Techniques

- **CSRF Tokens**:
    - **Synchronizer Tokens**: Unique, unpredictable tokens embedded in forms and validated on the server.
    - **Double Submit Cookies**: Tokens sent both as cookies and form parameters, verified for consistency.
- **SameSite Cookies**:
    - **SameSite Attribute**: Restricts how cookies are sent with cross-site requests, mitigating CSRF risks.
- **Referer and Origin Header Validation**:
    - **Referer Check**: Validates the origin of the request based on the `Referer` header.
    - **Origin Check**: Ensures the `Origin` header matches the trusted domain.
- **Custom Request Headers**:
    - **X-Requested-With**: Uses custom headers that are not automatically included in cross-site requests.
- **User Interaction Requirements**:
    - **CAPTCHAs**: Ensures that the request is made by a human.
    - **Re-authentication**: Requires users to re-enter credentials for sensitive actions.
- **Content Security Policy (CSP)**:
    - **Restrict Resource Loading**: Limits the sources from which resources can be loaded, reducing attack vectors.

### Security Considerations

- **State-Changing Requests**: Focus protection on requests that alter server state, such as POST, PUT, DELETE.
- **Idempotent Methods**: Use HTTP methods appropriately; GET requests should not change state.
- **Least Privilege**: Limit the actions that authenticated sessions can perform based on user roles.

### Personal Insight

**CSRF attacks exploit the trust a web application has in a user's browser**, making it imperative for developers to implement robust protection mechanisms. Combining multiple prevention techniques enhances security, ensuring that user actions are intentional and authorized.

### Related Notes

- [[Input Validation Techniques]]
- [[Secure Coding Practices]]
- [[Web Security Best Practices]]
- [[Authentication and Authorization]]
- [[Session Management]]