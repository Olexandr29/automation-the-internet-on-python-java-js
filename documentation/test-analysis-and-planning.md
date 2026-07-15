# Test Analysis & Planning

## Feature

Form Authentication (Login)

## Goal

Verify that users can log in and log out successfully and that invalid authentication attempts are handled correctly.

## Scope

### In Scope

- Login
- Logout
- Credential validation
- Error messages
- Password masking
- Basic security checks (SQL Injection, XSS)

### Out of Scope

- Registration
- Forgot Password
- Session timeout
- Performance
- Accessibility

---

# Test Scenarions

- Successful login
- Login with empty credentials
- Login with empty password
- Login with empty username
- Login with invalid password
- Login with invalid username
- Login with invalid username and password
- Logout
- Access protected page after logout
- Username with leading spaces
- Password with leading spaces
- Username with trailing spaces
- Password with trailing spaces
- Username with different letter case
- Password with different letter case
- SQL Injection in username
- SQL Injection in password
- XSS in username
- XSS in password
- Password masking

---

# Test Data

Valid credentials

- Username: tomsmith
- Password: SuperSecretPassword!

Invalid data

- Invalid username
- Invalid password
- Empty username
- Empty password
- Leading spaces
- Trailing spaces
- Different letter case
- SQL Injection payload
- XSS payload
