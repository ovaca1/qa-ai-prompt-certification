# User Story: Password Reset

## Title
Password Reset Functionality

## Description
As a registered user,
I want to reset my password when I forget it,
So that I can regain access to my account securely.

## Acceptance Criteria

1. The user can request a password reset by providing their registered email address.
2. The system sends a password reset link to the user's email address.
3. The password reset link expires after 1 hour for security purposes.
4. The user can set a new password using the reset link.
5. The new password must meet complexity requirements (minimum 8 characters, at least one uppercase, one lowercase, one number, one special character).
6. The new password cannot be the same as the previous 3 passwords.
7. The user is redirected to the login page after a successful password reset.
8. An error message is displayed if the email address is not found in the system.
9. An error message is displayed if the reset link has expired or has already been used.
10. The user receives a confirmation email after successfully resetting their password.
