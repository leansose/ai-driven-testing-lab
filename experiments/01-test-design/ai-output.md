---

Here is the test scenario suite derived strictly from the provided specification.

---

### Positive Cases

**Scenario ID:** TS_LOGIN_001

* **Title:** Successful login with valid credentials
* **Objective:** Verify that a user providing valid credentials is authenticated and granted access.
* **Preconditions:** A registered user account exists with valid credentials. The login form is displayed.
* **Test Data:** Username: `valid_user`, Password: `valid_password`
* **Expected Result:** User is successfully authenticated and granted access to the application.

---

### Negative Cases

**Scenario ID:** TS_LOGIN_002

* **Title:** Login attempt with invalid password
* **Objective:** Verify that authentication fails when a valid username is paired with an incorrect password.
* **Preconditions:** A registered user account exists. The login form is displayed.
* **Test Data:** Username: `valid_user`, Password: `invalid_password`
* **Expected Result:** User is not authenticated and receives appropriate feedback.

**Scenario ID:** TS_LOGIN_003

* **Title:** Login attempt with non-existent username
* **Objective:** Verify that authentication fails when using a username that does not exist in the system.
* **Preconditions:** The login form is displayed.
* **Test Data:** Username: `non_existent_user`, Password: `any_password`
* **Expected Result:** User is not authenticated and receives appropriate feedback.

---

### Input Validation

**Scenario ID:** TS_LOGIN_004

* **Title:** Login submission with empty username
* **Objective:** Verify feedback and access restriction when submitting a login attempt without entering a username.
* **Preconditions:** The login form is displayed.
* **Test Data:** Username: `[empty]`, Password: `valid_password`
* **Expected Result:** User is not authenticated and receives appropriate feedback regarding missing credentials.

**Scenario ID:** TS_LOGIN_005

* **Title:** Login submission with empty password
* **Objective:** Verify feedback and access restriction when submitting a login attempt without entering a password.
* **Preconditions:** The login form is displayed.
* **Test Data:** Username: `valid_user`, Password: `[empty]`
* **Expected Result:** User is not authenticated and receives appropriate feedback regarding missing credentials.

**Scenario ID:** TS_LOGIN_006

* **Title:** Login submission with all fields empty
* **Objective:** Verify behavior when submitting the login form without providing any input.
* **Preconditions:** The login form is displayed.
* **Test Data:** Username: `[empty]`, Password: `[empty]`
* **Expected Result:** User is not authenticated and receives appropriate feedback.

---

### Justified Edge Cases

**Scenario ID:** TS_LOGIN_007

* **Title:** Password case sensitivity
* **Objective:** Verify that password validation respects letter casing.
* **Preconditions:** A registered user account exists with a password containing mixed-case letters (e.g., `ValidPass1`). The login form is displayed.
* **Test Data:** Username: `valid_user`, Password: `validpass1`
* **Expected Result:** User is not authenticated and receives appropriate feedback.

**Scenario ID:** TS_LOGIN_008

* **Title:** Username leading/trailing whitespace handling
* **Objective:** Verify authentication behavior when whitespace is included around a valid username.
* **Preconditions:** A registered user account exists. The login form is displayed.
* **Test Data:** Username: `valid_user`, Password: `valid_password`
* **Expected Result:** System handles input according to credential matching (either fails authentication or successfully authenticates if whitespace trimming is enforced). Access is granted only upon exact or normalized credential match.