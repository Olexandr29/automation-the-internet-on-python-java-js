
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

<details><summary> <b>Test Suit - Dropdown</b> </summary>

## TC21 – Verify default state
### Precondition:
- The dropdown feature is available.
### Steps to reproduce:
1. Open the Home page https://the-internet.herokuapp.com/
2. Click the “Dropdown” to open the Dropdown page
### Expected result:
- The Dropdown page is opened successfully.
- The dropdown is visible.
- The dropdown is enabled.
- The dropdown is focusable.
- The default selected value is "Please select an option".

## TC22 – Verify all available options are displayed
### Precondition
- User is on the Dropdown page.
### Steps to reproduce
1. Click the dropdown.
2. Observe the list of available options.
### Expected result
- The dropdown list is opened.
- The following options are displayed:
    - Please select an option
    - Option 1
    - Option 2
- No unexpected options are displayed.

## TC23 – Verify dropdown opens when clicking the selected value 
### Precondition
- User is on the Dropdown page.
### Steps to reproduce
1. Click the currently selected value (Please select an option)
2. Click outside the dropdown
### Expected result
- The dropdown list is opened after step 1.
- All available options are displayed.
- The dropdown list is closed after step 2.

## TC24 – Verify dropdown opens when clicking dropdown arrow 
### Precondition
- User is on the Dropdown page.
### Steps to reproduce
1. Click the dropdown arrow
2. Press Escape key
### Expected result
- The dropdown list is opened after step 1.
- All available options are displayed.
- The dropdown list is closed after step 2.

## TC25 – Select Option 1 using mouse
### Precondition:
- User is on the Dropdown page.
### Steps to reproduce:
1. Click the dropdown
2. Select Option 1
### Expected result:
- Option 1 became the selected value.

## TC26 – Select Option 2 and verify the selected option is highlighted when reopen the dropdown
### Precondition:
- User is on the Dropdown page.
### Steps to reproduce:
1. Click the dropdown
2. Select Option 2
3. Open dropdown again
### Expected result:
- The dropdown is opened after step 1.
- Option 2 is selected after step 2.
- The dropdown is opened and the Option 2 is highlighted as selected after step 3.

## TC27 – Change selected option using keyboard arrow keys
### Precondition:
- User is on the Dropdown page.
- The dropdown is focused
- Option 1 is selected
### Steps to reproduce:
1. Press the Arrow Down key
2. Press the Arrow Up key
### Expected result:
- After pressing Arrow Down, Option 2 becomes selected.
- After pressing Arrow Up, Option 1 becomes selected.

## TC28 – Navigate, select and change the dropdown option using keyboard
### Precondition:
- User is on the Dropdown page.
### Steps to reproduce:
1. Press the Tab key until the dropdown will be focused
2. Press Enter to open the dropdown
3. Press Arrow Down to select Option 1
4. Press Arrow Down to change selected option to Option 2
5. Press Arrow Up to select Option 1
### Expected result:
- The Drodown is focused after step 1.
- The Dropdown is opened and all available options are displayed after step 2.
- The Option 1 is selected after step 3.
- The Option 2 is selected after step 4.
- The Option 1 is selected after step 5.

## TC29 – Verify the selected option persists after closing and reopening the dropdown
### Precondition:
- User is on the Dropdown page.
### Steps to reproduce:
1. Select Option 2
2. Open the dropdown again
### Expected result:
- The Option 2 is selected
- The previously selcted value Option 2 is displayed(selected) when the dropdown is reopened

## TC30 – Verify the Arrow Upd and Down on the first and last options
### Precondition:
- User is on the Dropdown page.
- The dropdown is opened.
- The Option 1 is selected.
### Steps to reproduce:
1. Press Arrow Up
2. Select Option 2
3. Press Arrow Down
### Expected result:
- The selected value does not change. The Option 1 remains selected after step 1.
- The Option 2 is selected after step 2.
- The selected value does not change. The Option 2 remains selected after step 3.

## TC31 – Verify only one option can be selected at a time
### Precondition:
- User is on the Dropdown page.
- The dropdown is opened.
- The Option 1 is selected.
### Steps to reproduce:
1. Open the dropdown again
2. Select Option 2
### Expected result:
- Option 2 is selected after step 2.
- Option 1 is no longer selected.
- Only one option is selected at a time.



</details>
