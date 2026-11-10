
# Test Suite - Login(Form Authentication)
<details><summary> <b>TC1-20
</b> </summary>

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

# Test Suite - Dropdown

<details><summary> <b>TC21-30</b> </summary>

## TC21 – Verify default state
### Precondition:
- The dropdown feature is available.
### Steps to reproduce:
1. Open the Home page https://the-internet.herokuapp.com/
2. Click the “Dropdown” to open the Dropdown page
### Expected result:
- The Dropdown page is opened successfully.
- The dropdown is visible.
- The default selected value is "Please select an option".


## TC22 – Verify all available options are displayed
### Precondition
- User is on the Dropdown page.
### Steps to reproduce
1. Open the dropdown.
### Expected result
- The dropdown list is opened.
- The following options are displayed:
    - Please select an option
    - Option 1
    - Option 2
- No unexpected options are displayed.

## TC23 – Select Option 1 using mouse
### Precondition:
- User is on the Dropdown page.
### Steps to reproduce:
1. Click the dropdown
2. Select Option 1
### Expected result:
- Option 1 is selected.

## TC24 – Verify option remains selected after reopening and closing
### Precondition:
- User is on the Dropdown page.
### Steps to reproduce:
1. Click the dropdown
2. Select Option 2
3. Open dropdown again
4. Close dropdown
### Expected result:
- The dropdown is opened after step 1.
- Option 2 is selected after step 2.
- The dropdown is opened and the Option 2 is highlighted as selected after step 3.
- The Option 2 remain selected after closing.

## TC25 – Change selected option using keyboard arrow keys
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

## TC26 – Navigate, select and change the dropdown option using keyboard
### Precondition:
- User is on the Dropdown page.
### Steps to reproduce:
1. Press Tab key until the dropdown receives focus
2. Press Enter to open the dropdown
3. Press Arrow Down and ENTER to select Option 1
4. Press Arrow Down to change selected option to Option 2
5. Press Arrow Up to select Option 1
### Expected result:
- The Dropdown is focused after step 1.
- The Dropdown is opened and all available options are displayed after step 2.
- The Option 1 is selected after step 3.
- The Option 2 is selected after step 4.
- The Option 1 is selected after step 5.

## TC27 – Verify the Arrow Up and Down on the first and last options
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

## TC28 – Verify only one option can be selected at a time
### Precondition:
- User is on the Dropdown page.
- The dropdown is opened.
- The Option 1 is selected.
### Steps to reproduce:
1. Select Option 2
### Expected result:
- Option 2 is selected.
- Option 1 is no longer selected.
- Only one option is selected at a time.

## TC29 – Verify selected option after refresh
### Precondition:
- User is on the Dropdown page.
- The Option 1 is selected.
### Steps to reproduce:
1. Click the browser Refresh button
### Expected result:
- The default value "Please select an option" is selected.

## TC30 – Verify browser Back and Forward navigation behaviour
### Precondition:
- User is on the Dropdown page.
- The Option 2 is selected.
### Steps to reproduce:
1. Click the browser Back button
2. Click the browser Forward button
### Expected result:
- The Home page is opened after step 1.
- The "Dropdown" link is visible.
- The Dropdown page is opened after step 2.
- The Option 2 is selected.


</details>

# Test Suite - Checkbox
<details><summary> <b>TC31-35
</b> </summary>

## TC31 – Verify Checkboxes are visible
### Precondition:
- The checkbox feature is available.
### Steps to reproduce:
1. Open the Home page https://the-internet.herokuapp.com/
2. Click the "Checkboxes" link to open the Checkboxes page
### Expected result:
- The Checkboxes page is opened successfully.
- The "checkbox 1" and "checkbox 2" are visible.

## TC32 – Verify Checkboxes initial state
### Precondition:
- User is on the Home page.
### Steps to reproduce:
1. Click the "Checkboxes" link to open the Checkboxes page
### Expected result:
- The "checkbox 1" is unchecked.
- The "checkbox 2" is checked.

## TC33 – Verify checkboxes state changes correctly
### Precondition:
- User is on the Checkboxes page.
### Steps to reproduce:
1. Click the checkbox "checkbox 1"
2. Click the "checkbox 1" again
3. Click the "checkbox 2"
4. Click the "checkbox 2" again
### Expected result:
- The "checkbox 1" is checked after first click.
- The "checkbox 1" is unchecked after second click.
- The "checkbox 2" is unchecked after first click.
- The "checkbox 2" is checked after second click.

## TC34 – Verify checkboxes state after refresh
### Precondition:
- User is on the Checkboxes page.
- The "checkbox 1" and "checkbox 2" are checked.
### Steps to reproduce:
1. Click the browser Refresh button
### Expected result:
- The "checkbox 1" is unchecked.
- The "checkbox 2" is checked.

## TC35 – Verify checkbox state chnges using keyboard
### Precondition:
- User is on the Checkboxes page.
### Steps to reproduce:
1. Navigate to the checkbox using the Tab key
2. Press the Space key to change state for "checkbox 1"
3. Repeat steps 1-2 for "checkbox 2"
### Expected result:
- Checkbox state toggles successfully
- Focus indicator is visible
- The "checkbox 1" is checked.
- The "checkbox 2" is unchecked.



</details>


</details>

# Test Suite - Broken images
<details><summary> <b>TC36-37
</b> </summary>


## TC36 – Verify page content
### Precondition:
- The Broken images feature is available.
### Steps to reproduce:
1. Open the Broken Images page https://the-internet.herokuapp.com/broken_images
2. Verify that the page header "Broken Images" is displayed
3. Verify that 3 `<img>` elements are displayed on the page
4. Verify that the text "Powered by Elemental Selenium" is displayed
5. Verify that the "Elemental Selenium" link is displayed
### Expected result:
- The Broken Images page loaded successfully: 
    - URL is https://the-internet.herokuapp.com/broken_images
    - The document `readyState` is `complete`
- The "Broken Images" header is displayed
- Three `<img>` elements are displayed
- The text "Powered by Elemental Selenium" is displayed
- The "Elemental Selenium" link is displayed

## TC37 – Verify image loading
### Precondition:
- The Broken Images page is open.
### Steps to reproduce:
1. Locate the first image on the page.
2. Verify that the first image is displayed correctly.
3. Repeat Steps 1-2 for the second image.
4. Repeat Steps 1-2 for the third image.
### Expected result:
- No broken image indicator or missing image placeholder is displayed:
    - The first image is displayed correctly.
    - The second image is displayed correctly.
    - The third image is displayed correctly.



</details>


# Test Suite - Dynamic Controls
<details><summary> <b>TC38-46
</b> </summary>


## TC38 – Verify page content
### Precondition:
- The Dynamic Controls feature is available.
### Steps to reproduce:
1. Open the Dynamic Controls page https://the-internet.herokuapp.com/dynamic_controls
2. Verify that the page header "Dynamic Controls" is displayed
3. Verify that the text description "This example demonstrates when elements (e.g., checkbox, input field, etc.) are changed asynchronously."is displayed on the page
4. Verify that the first subheader "Remove/add" is displayed
5. Verify that one checkbox with the text " A checkbox" is displayed
6. Verify that button "Remove" is displayed
7. Verify that the second subheader "Enable/disable" is displayed
8. Verify that the input field is displayed
9. Verify that button "Enable" is displayed
10. Verify that the text "Powered by Elemental Selenium" is displayed
11. Verify that the "Elemental Selenium" link is displayed
### Expected result:
1. The Dynamic Controls page loaded successfully: 
    - URL is https://the-internet.herokuapp.com/dynamic_controls
    - The document `readyState` is `complete`
2. The "Dynamic Controls" header is displayed
3. The text description "This example demonstrates when elements (e.g., checkbox, input field, etc.) are changed asynchronously."is displayed
4. The subheader "Remove/add" is displayed
5. The checkbox with the text " A checkbox" is displayed
6. The button "Remove" is displayed
7. The subheader "Enable/disable" is displayed
8. The input field is displayed
9. The button "Enable" is displayed
10. The text "Powered by Elemental Selenium" is displayed
11. The "Elemental Selenium" link is displayed- The text "Powered by Elemental 

## TC39 – Verify checkbox initial state and changes
### Precondition:
- The Dynamic Controls page https://the-internet.herokuapp.com/dynamic_controls is opened.
### Steps to reproduce:
1. Observe checkbox initial state
2. Click the checkbox "A checkbox"
3. Click the "A checkbox" again
### Expected result:
1. The initial state of the checkbox "A checkbox" is unchecked.
2. The "A checkbox" is checked afer first click.
3. The "A checkbox" is unchecked after second click.

## TC40 – Remove and add checkbox
### Precondition:
- The Dynamic Controls page https://the-internet.herokuapp.com/dynamic_controls is opened.
### Steps to reproduce:
1. Observe checkbox initial state
2. Click the "Remove" button
3. Click the "Add" button
### Expected result:
1. The initial state of the checkbox "A checkbox" is unchecked.
2. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is removed and not displayed at the page.
The button title "Remove" changed to "Add".
The text "It's gone!" is appeared.
3. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is appeared and has unchecked state.
The button title "Add" changed to "Remove".
The text "It's gone!" changed to "It's back!".

## TC41 – Remove and add checked checkbox
### Precondition:
- The Dynamic Controls page https://the-internet.herokuapp.com/dynamic_controls is opened.
### Steps to reproduce:
1. Observe checkbox initial state
2. Click the checkbox "A checkbox"
3. Click the "Remove" button
4. Click the "Add" button
5. Repeat Steps 2 and 3
6. Repeat Step 4
7. Repeat Steps 2 and 3 again
8. Repeat Step 4 again
### Expected result:
1. The initial state of the checkbox "A checkbox" is unchecked.
2. The "A checkbox" is became checked.
3. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is removed and not displayed at the page.
The button title "Remove" changed to "Add".
The text "It's gone!" is appeared.
4. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is appeared and has unchecked state.
The button title "Add" changed to "Remove".
The text "It's gone!" changed to "It's back!".
5. The "A checkbox" is became checked.
The text "Wait for it" and indeterminate progress bar are appeared.
The checkbox "A checkbox" is removed and just text "A checkbox" is displayed at the page.
The button title "Remove" changed to "Add".
The text "It's gone!" is displayed.
6. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is appeared with unchecked state and the text "A checkbox" is displayed under the checkbox.
The button title "Add" changed to "Remove".
The text "It's gone!" changed to "It's back!".
7. The "A checkbox" is became checked.
The text "Wait for it" and indeterminate progress bar are appeared.
The checkbox "A checkbox" is removed and the text "A checkbox" is displayed 2 times at the page.
The button title "Remove" changed to "Add".
The text "It's gone!" is displayed.
8. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is appeared with unchecked state and the text "A checkbox" is displayed 2 times under the checkbox.
The button title "Add" changed to "Remove".
The text "It's gone!" changed to "It's back!".

## TC42 – Enable and disable the Input field
### Precondition:
- The Dynamic Controls page https://the-internet.herokuapp.com/dynamic_controls is opened.
### Steps to reproduce:
1. Verify the initial state of the input field
2. Click the "Enable" button
3. Enter a text into the input field (e.g. "Hello")
4. Click the "Disable" button
### Expected result:
1. The initial state of the input field is disabled.
2. The text "Wait for it" and indeterminate progress bar are appeared.
The state of the input field became enabled.
The button title "Enable" changed to "Disable".
The text "It's enabled!" is appeared.
3. The entered text displayed into the input field
4. The text "Wait for it" and indeterminate progress bar are appeared.
The state of the input field became disabled and the text entered by Step 3 is displayed.
The button title "Disable" changed to "Enable".
The text "It's enabled!" changed to "It's disabled!".

## TC43 – Verify checkbox section state after refresh
### Precondition:
- The Dynamic Controls page https://the-internet.herokuapp.com/dynamic_controls is opened.
### Steps to reproduce:
1. Click the "Remove" button
2. Click the browser Refresh button
3. Click the "A checkbox"
4. Click "Remove" button
5. Click the "Add" button
6. Click the browser Refresh button
### Expected result:
1. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is removed and not displayed at the page.
The button title "Remove" changed to "Add".
The text "It's gone!" is appeared.
2.The Checkbox section got initial state after refresh:
The initial state of the checkbox "A checkbox" is unchecked.
The button title "Remove" is displayed.
3. The "A checkbox" state is became cheked.
4. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is removed and not displayed at the page.
The button title "Remove" changed to "Add".
The text "It's gone!" is appeared.
5. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is appeared and has unchecked state.
The button title "Add" changed to "Remove".
The text "It's gone!" changed to "It's back!".
6.The Checkbox and Input Field sections got initial state after refresh:
The initial state of the checkbox "A checkbox" is unchecked.
The button title "Remove" is displayed.
The initial state of the input field is disabled.
The button title "Enable" is displayed.

## TC44 – Verify Iput field section state after refresh
### Precondition:
- The Dynamic Controls page https://the-internet.herokuapp.com/dynamic_controls is opened.
### Steps to reproduce:
1. Click the "Enable" button
2. Click the browser Refresh button
3. Navigate to the Input field and enter an input value (e.g. "Input123$")
4. Click "Disable" button
5. Click the browser Refresh button
### Expected result:
1. The text "Wait for it" and indeterminate progress bar are appeared.
The state of the input field became enabled.
The button title "Enable" changed to "Disable".
The text "It's enabled!" is appeared.
2.The Input Field section got initial state after refresh:
The initial state of the input field is disabled.
The button title "Enable" is displayed.
3. The entered text displayed into the input field
4. The text "Wait for it" and indeterminate progress bar are appeared.
The state of the input field became disabled and the text entered by Step 3 is displayed.
The button title "Disable" changed to "Enable".
The text "It's enabled!" changed to "It's disabled!".
5.The Input Field section got initial state after refresh:
The initial state of the input field is disabled.
The button title "Enable" is displayed.

## TC45 – Navigate, select and change checkbox section state using keyboard
### Precondition:
- The Dynamic Controls page https://the-internet.herokuapp.com/dynamic_controls is opened.
### Steps to reproduce:
1. Press Tab key until the checkbox " A checkbox" receives focus.
2. Press Space key to check the checkbox.
3. Press Tab key until the button "Remove" receives focus.
4. Press Enter key to click the "Remove" button.
5. Press Tab key until the button "Add" receives focus.
6. Press Enter key to click the "Add" button.
7. Repeat Steps 1 and 2.
8. Repeat Steps 3 and 4.
9. Repeat Steps 5 and 6.
### Expected result:
1. The checkbox " A checkbox" is focused.
2. The "A checkbox" is checked.
3. The "Remove" button is focused.
4. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is removed and not displayed at the page.
The button title "Remove" changed to "Add".
The text "It's gone!" is appeared.
5. The "Add" button is focused.
6. The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is appeared and has unchecked state.
The button title "Add" changed to "Remove".
The text "It's gone!" changed to "It's back!".
7. The checkbox " A checkbox" is focused.
The "A checkbox" is checked.
8. The "Remove" button is focused.
The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" is removed and not displayed at the page.
The button title "Remove" changed to "Add".
The text "It's gone!" is appeared.
9. The "Add" button is focused.
The text "Wait for it" and indeterminate progress bar are appeared.
The "A checkbox" with unchecked state and text "A checkbox" is displayed under the checkbox.
The button title "Add" changed to "Remove".
The text "It's gone!" changed to "It's back!".

## TC46 – Navigate, select and change input field section state using keyboard
### Precondition:
- The Dynamic Controls page https://the-internet.herokuapp.com/dynamic_controls is opened.
### Steps to reproduce:
1. Press Tab key until the button "Enable" receives focus.
2. Press Enter key to click the "Enable" button.
3. Press Tab key until the input field receives focus.
4. Enter a value to the input field (e.g. "$And40")
5. Press Tab key until the button "Disable" receives focus.
6. Press Enter key to click the "Disable" button.
### Expected result:
1. The "Enable" button is focused.
2. The text "Wait for it" and indeterminate progress bar are appeared.
The state of the input field became enabled.
The button title "Enable" changed to "Disable".
The text "It's enabled!" is appeared.
3. The input field is focused.
4. The entered value is displayed into the input field
5. The "Disable" button is focused.
6. The text "Wait for it" and indeterminate progress bar are appeared.
The state of the input field became disabled and the text entered by Step 4 is displayed.
The button title "Disable" changed to "Enable".
The text "It's enabled!" changed to "It's disabled!".


</details>
