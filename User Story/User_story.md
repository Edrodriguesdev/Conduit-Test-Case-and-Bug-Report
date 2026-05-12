Sign Up

General requirements -> https://docs.google.com/document/d/163l8WmwPZJCYqd1PWzwDLpjvfdcAyw3kSrrXFeqS0xE/edit?tab=t.0#heading=h.x0fryrp3g3lm

Requirements for the fields -> https://docs.google.com/document/d/163l8WmwPZJCYqd1PWzwDLpjvfdcAyw3kSrrXFeqS0xE/edit?tab=t.0#heading=h.ne2x55vb0itz

Validation Messages -> https://docs.google.com/document/d/163l8WmwPZJCYqd1PWzwDLpjvfdcAyw3kSrrXFeqS0xE/edit?tab=t.0#heading=h.g0kepsf718at

General requirements

1 - The “Sign Up” page allows users to register on the site or help them to log in if they already have an account. The link to the “Sign Up” page should be accessible for all not logged-in users in the navigation bar.

2 - Users should be able to create an account by filling in all fields and clicking on the [Sign Up] button or pressing the Enter button.

3 - If there is no conflict with the credentials, then the user is registere,d and an email to verify the email address is sent.

 a. After successful registration, a user should be redirected to the “Finish Registration” page to enter the 6-digit code sent by email.

4 - Users should be able to go to the “Sign In” page by clicking on the “Have an account?” link below the “Sign Up” form.

Requirements for the fields
 
5 - The “Sign up” form should contain the following fields:

Field	Requirements
5.1 Username	required field;
    should be unique;
    min 3 symbols;
    max 40 symbols;
    should accept Latin letters and digits;
    should start with a letter;
    special characters  are not allowed;
    non-printing symbols are not allowed;
    no case sensitive.
    the format of the email is [name]@[domain].[top-domain];
    [name] part accepts Latin letters, digits, and some special characters: plus (+), hyphen (-), underline (_), dot (.);
    should be unique;
    required field.
    required field;
    min 8 symbols,
    max 30 symbols;
    non-printing symbols are not allowed;
    
5.2 Email	should contain at least one special character;
    should contain at least one digit;
    should contain at least one capital letter.
    required field;
    the value should match the Password field.
5.3 Password	required field;
    min 8 symbols,
    max 30 symbols;
    non-printing symbols are not allowed;
    should contain at least one special character;
    should contain at least one digit;
    should contain at least one capital letter.
5.4 Confirm password	required field;
    the value should match the Password field.
    

Validation Messages
6 - The next validation messages should be shown to the user:

a. For the taken username: “This username is taken.“

b. For the non-valid username: “Username must start with a letter, have no spaces, and be 3 - 40 characters.”

c. For the taken email: “This email is taken. Want to log in?”

d. For the non-valid email: “This email does not seem valid.”

e. For the password: “Password can’t be blank. Password should contain at least one capital letter, one number, and one special character.”