
<details><summary> <b>Test Suit - Login(Form Authentication)</b> </summary>

## TC1 – Successful login

### Precondition:
- The application is available.
### Steps to reproduce:
1. Open the Home page https://the-internet.herokuapp.com/
2. Click the “Form Authentication” to open the Login page
3. Fill in the Username field with a valid value (e.g. “tomsmith”)
4. Fill in the Password field with a valid value (e.g. “SuperSecretPassword!”)
5. Click the Login
### Expected result:
- User is redirected to the Secure Area page
- The alert “You logged into a secure area!” is displayed
- The message “Welcome to the Secure Area. When you are done click logout below.” is displayed
- The Logout button is displayed.


## TC2 – Unsuccessful login with empty credentials
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Leave the Username field empty
2. Leave the Password field empty
3. Click the Login button
### Expected result:
- The alert “Your username is invalid!” is displayed on the Login page.

## TC3 – Unsuccessful login with empty Password
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username field with a valid value (e.g. «tomsmith»)
2. Leave the Password field empty
3. Click the Login button
### Expected result:
- The alert “Your password is invalid!” is displayed on the Login page

## TC4 – Unsuccessful login with empty Username
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Leave the Username field empty
2. Fill in the Password field with a valid value (e.g. «SuperSecretPassword!»)
3. Click the Login button
### Expected result:
- The alert “Your username is invalid!” is displayed on the Login page

## TC5 – Unsuccessful login with invalid Password
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username field with a valid value(e.g. “tomsmith”)
2. Fill in the Password field with an invalid value (e.g. “111”)
3. Click the Login button
### Expected result:
- The alert “Your password is invalid!” is displayed on the Login page

## TC6 – Unsuccessful login with invalid Username
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username field with an invalid value(e.g. “1”)
2. Fill in the Password field with a valid value (e.g. “SuperSecretPassword!”)
3. Click the Login button
### Expected result:
- The alert “Your username is invalid!” is displayed on the Login page


## TC7 – Unsuccessful login with both Invalid Username and Password
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username field with an invalid value(e.g. “invalidName”)
2. Fill in the Password field with an invalid value(e.g. “invalidPassword”)
3. Click the Login button
### Expected result:
- The alert “Your username is invalid!” is displayed on the Login page

## TC8 – Logout
### Preconditions:
- Username: tomsmith
- Password: SuperSecretPassword! 
- User is logged in successfully and is on the Secure Area page
### Steps to reproduce:
1. Verify that the Logout button is displayed
2. Click the Logout button
### Expected result:
- User is redirected to the Login page
- The alert "You logged out of the secure area!" is displayed
- The Login button is displayed


## TC9 – User cannot access the Secure Area after logout
### Preconditions:
- Username: tomsmith
- Password: SuperSecretPassword! 
- User is logged in successfully and is on the Secure Area page
### Steps to reproduce:
1. Click the Logout button
2. Verify that the Login button is displayed
3. Click the browser Back button
4. Click the browser Refresh button
### Expected result:
  - User is not able to access the Secure Area page
  - User remains on the Login page
  - The Login button is displayed 


## TC10 –  Login with a Username that has leading spaces
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username with a value that has leading spaces(e.g. “ tomsmith” )
2. Fill in the Password field with a valid value (e.g. SuperSecretPassword!)
3. Click the Login button
### Expected result:
- The alert “Your username is invalid!” is displayed on the Login page


## TC11 –  Login with a password that has leading spaces
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username with a valid value(e.g. “tomsmith” )
2. Fill in the Password field with a value that has leading spaces (e.g. “ SuperSecretPassword!”)
3. Click the Login button
### Expected result:
- The alert “Your password is invalid!” is displayed on the Login page


## TC12 –  Login with a Username that has trailing spaces
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username with a value that has trailing spaces(e.g. “tomsmith  ” )
2. Fill in the Password field with a valid value (e.g. SuperSecretPassword!)
3. Click the Login button
### Expected result:
- The alert “Your username is invalid!” is displayed on the Login Page


## TC13 –  Login with a Password that has trailing spaces
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username with a valid value(e.g. “tomsmith” )
2. Fill in the Password field with a value that has trailing spaces (e.g. “SuperSecretPassword! ”)
3. Click the Login button
### Expected result:
- The alert “Your password is invalid!” is displayed on the Login page


## TC14 –  Login with a Username that has a different case
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username with a value that has a different case(e.g. “TOMSMITH” )
2. Fill in the Password field with a valid value (e.g. SuperSecretPassword!)
3. Click the Login button
### Expected result:
- The alert “Your username is invalid!” is displayed on the Login page


## TC15 –  Login with a Password that has a different case
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username with a valid value(e.g., “tomsmith” )
2. Fill in the Password field with a value that has a different case (e.g., “SUPERSECRETPASSWORD!”)
3. Click the Login button
### Expected result:
- The alert “Your password is invalid!” is displayed on the Login page


## TC16 –  Login with SQL Injection in Username
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username with SQL injection (e.g., `' OR '1'='1'` )
2. Fill in the Password field with an invalid value (e.g., “anything”)
3. Click the Login button
### Expected result:
- The alert “Your username is invalid! ” is displayed on the Login page


## TC17 –  Login with SQL Injection in Password
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username with a valid value(e.g., “tomsmith” ) 
2. Fill in the Password field with SQL injection (e.g., `' OR '1'='1` )
3. Click the Login button
### Expected result:
- The alert “Your password is invalid!” is displayed on the Login page


## TC18 –  Login with XSS in Username
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username with XSS (e.g., `<script>alert('xss')</script>` )
2. Fill in the Password field with a valid value (e.g., SuperSecretPassword!)
3. Click the Login button
### Expected result:
- The alert “Your username is invalid! ” is displayed on the Login page


## TC19 –  Login with XSS in Password
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Steps to reproduce:
1. Fill in the Username with a valid value(e.g., “tomsmith” ) 
2. Fill in the Password field with XSS (e.g., `<script>alert('xss')</script>` )
3. Click the Login button
### Expected result:
- The alert “Your password is invalid!” is displayed on the Login page

## TC20 – Password is masked
### Precondition:
- User is on the Login page: https://the-internet.herokuapp.com/login
### Step to reproduce:
1. Fill in the Password field with any value (e.g., “anything”)
### Expected result:
- Password characters are hidden(displayed as dots or asterisks, depending on the browser). 

</details>

