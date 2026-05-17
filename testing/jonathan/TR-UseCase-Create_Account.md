# TEST REPORT — Create Account Use Case

**Tester:** Jonathan Bitingingwa
**Date:**  25th April,2026
**Issue Reference:**  #2
**Use Case:**  Create Account

---

## What I am testing
This test focuses on verifying that a user can successfully create an account as a Student, correctly select their level and programming languages, and proceed through the expected flow up to account creation and pending approval.

## What I did (steps)

### Scenario 1 —
- I opened the live application in the browser [](https://student.michaelkentburns.com/)

- The web page asked me to accept or reject all cookies

- I went on and accepted all cookies and saved preferences

- I Clicked on "User" 

- Chose "Register as Student"

- The web page asked me to type a username and email adress

- I Entered a valid username "jonathantest" and a valid email addresse "jonathanngoy234@gmail.com" then clicked on "Register"

- Got a promp message that says: "Registration complete. Please check your email, then visit the login page

- Got an email directly showing the username inputed and tells me to click on the provided link to create a password

- I was redirected to a page showing a suggested passeword

- I saved the password and the page populated a message saying: " Your password has been reset" and a login button

- I Clicked the login button and got redirected to the login page that requires me to put the registered username and password

- I had to put the valid username and password created then clicked on login

- I successfully logged in as a student in the  student dashboard

### Scenario 2 —
- I opened the application: https://student.michaelkentburns.com
- I clicked on “User”
- I selected “Register as Student”
- I left the username field empty
- I entered a valid email: jonathanngoy234@gmail.com
- I clicked “Register”

### Scenario 3 —
- I entered a valid username
- I left the email field empty
- I clicked “Register”

### Scenario 4 —
- I left both username and email fields empty
- I clicked “Register”
---

## What I noticed
**Scenario 1 Result:**
- The system does not ask for level or programming languages, which is expected in the use case
- The flow includes a password reset mechanism instead of direct password creation, which is not mentioned in the use case
- The message says “visit the login page”, but I was required to create a password first, which is slightly confusing
- There is no mention of “Pending Approval by Administrator”
- I was able to log in immediately after registration, meaning no approval step exists
- The system worked smoothly, but the flow is different from what is defined in the use case

**Scenario 2 Result:**

Error: “Please enter a username.”
Error: “This email address is already registered…”
Issue: The system shows duplicate email error even though the main problem is missing username

**Scenario 3 Result:**

Error: “This username is already registered…”
Error: “Please type your email address.”
Issue: The system shows username already registered error even when email is empty

Scenario 4 Result:

Error: “Please enter a username.”
Error: “Please type your email address.”
This one behaves correctly 

---

## What should have happened
Based on the use case:

- After selecting Student role, I should:
- Choose level
- Choose programming languages
- My account should be:
- Stored
- Sent for administrator approval
- I should see a message like: “Your account is pending approval”

Validation should be field-specific and logical
**Expected behavior:**
If username is empty,  show ONLY:
 “Username is required”
If email is empty,  show ONLY:
 “Email is required”

System should not check duplicates when required fields are missing

---

## Is this a problem?

| # | Short Description | Type | Severity |
|---|-------------------|------|----------|
| 1 |  YES because the actual system flow does not match the documented use case| - Functional mismatch / Missing features / UX inconsistency| High (core functionality differs from system design)|
| 2 |YES, Incorrect validation logic shows irrelevant error messages |Bug / Validation Logic Issue / UX Issue
 |Medium - High (because it affects user understanding and form usability) |
| 3 | | | |

---

## Special Note
- “Choose Level and Programming Languages” is completely missing
- “Pending Approval by Administrator” is not implemented
- Password creation is done via email reset flow, not described in the use case
-User can log in immediately, which contradicts the approval step
-  System performs duplicate checks even when required fields are missing
-  Error messages are not prioritized correctly
-  Use case mentions “Error message” but does not define validation order
-  Scenario 3 works correctly → shows inconsistency in logic
---

## Evidence
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/4b7679e7-14a1-4105-a826-61d1448fbc26" /> **Screenshot of registration confirmation message**

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/bc3e64fc-9554-480f-b950-ca515f49193f" /> **Screenshot of email received**

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/b2d99dfd-0bfa-4526-a94a-0cf482e32c26" /> **Screenshot of password reset page**

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/7b5670f1-6e50-477a-9a5d-fcc1807e4108" /> **Screenshot of student dashboard after login**
<img width="600" height="609" alt="Image" src="https://github.com/user-attachments/assets/bcf4e7ba-7e4f-4c10-ae72-ad99891d597c" /> **The system shows duplicate email error even though the main problem is missing username**
<img width="1280" height="722" alt="Image" src="https://github.com/user-attachments/assets/59572428-bc7c-4f25-92e6-c750157f048b" /> **The system shows username already registered error even when email is empty**

---

## My thoughts / questions
- Is the use case outdated or is the system incomplete?
- Why is student-specific data (level, languages) not collected?
- Is admin approval intentionally removed or not yet implemented?
- Why use password reset instead of standard registration form?
- Why is duplicate validation triggered before required field validation?
- Is validation happening on backend only?
- Is there no validation hierarchy?
- Ideas for improvement:
- Implement validation order:
- Required fields
- Format validation
- Duplicate checks
- Show one clear error per field
- Improve error clarity and prioritization

---

## Action taken
- [x] I created a sub-issue for each valid bug
- [x] I added the `bug` label on each sub-issue
- [x] I continued testing

Sub-issue links:

-https://github.com/FreeDev-Group/Samuel-Special-Challenge-for-Cohort-3/issues/7
-https://github.com/FreeDev-Group/Samuel-Special-Challenge-for-Cohort-3/issues/8


---

## Files
`/testing/[Your-Name]/[TR-UseCase-Name].md`
