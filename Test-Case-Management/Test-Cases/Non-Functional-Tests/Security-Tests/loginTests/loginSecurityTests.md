### Login Security Test - Password Strength (Web App)
**ID:**

**Title:** Verify password Strength Requirements are enforced for an active user that is changing their password through the login page
*Description:* Verifies that the application enforces password strength requirements during password changes, using the `Forgot Password?` workflow

*Preconditions:*
* The web app is deployed and running
* A test user with valid credentials has been created and activated
* Tester has access to the testing environment

**Steps:**
1. Attempt to change an active user's password using the `Forgot Password?` element on the web applications login page. 
2. After receiving the email sent, select the call to action button.
3. Attempt to change the password with one that does not meet the requirements. *(e.g., same password, minimum character length, invalid characters, spaces, etc)
4. Observe the response

**Expected Results:**
* Application prevents password change
* An error message is displayed, indicating the password does not meet the requirements (and which if relevant)
* The password field is cleared

**Actual Results:**
*(to be filled out during testing)*
**Status:** *(e.g., Pass, Fail, Retest, In Progress)*
**Notes:** *(Additional information/ notes)*

### Login Security Test - Password Strength (Web App)
**ID:**

**Title:** Verify password Strength Requirements are enforced for during user registration.
*Description:* Verifies that the application enforces password strength requirements during user registration

*Preconditions:*
* The web app is deployed and running
* A test user with valid credentials has been created, but not yet activated
* The Test users' email address is accessible to the Tester
* Tester has access to the testing environment

**Steps:**
1. Attempt to complete activation/registration for the invited user by selecting a valid invitation key.
2. Attempt to change the password with one that does not meet the requirements. *(e.g., minimum character length, case requirements, invalid characters, spaces, etc)
4. Observe the response

**Expected Results:**
* Application prevents activation/registration
* An error message is displayed, indicating the password does not meet the requirements (and which if relevant)
* The password field is cleared

  ### Login Security Test - Password Strength (Web App)
**ID:**

**Title:** Verify password Strength Requirements are enforced for an active user that is changing their password through the Profile page
*Description:* Verifies that the application enforces password strength requirements during password changes using the Change password flow within `Application/ProfilePage`

*Preconditions:*
* The web app is deployed and running
* A test user with valid credentials has been created and activated
* Tester has access to the testing environment

**Steps:**
1. Login as test user and navigate to the profile page.
2. Attempt to change an active user's password using the `Change Password` element on the web applications profile page.
3. Attempt to change the password with one that does not meet the requirements. *(e.g., same password, minimum character length, invalid characters, spaces, etc)
5. Observe the response

**Expected Results:**
* Application prevents password change
* An error message is displayed, indicating the password does not meet the requirements (and which if relevant)
* The password field is cleared

**Actual Results:**
*(to be filled out during testing)*
**Status:** *(e.g., Pass, Fail, Retest, In Progress)*
**Notes:** *(Additional information/ notes)*
