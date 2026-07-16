# Evaluation 02: Password Reset User Story Test Suite

**Prompt Evaluated:** QA Test Suite Generator  
**User Story:** Password Reset Functionality  

---

## Input User Story

As a user who forgot my password,  
I want to reset my password,  
so that I can regain access to my account.

### Acceptance Criteria

- Users can request a password reset using their registered email address.
- Users receive a password reset link.
- Reset links expire after a defined period.
- Users can create a new password following security requirements.
- Users cannot reuse previous passwords.
- Invalid reset requests are handled securely.

---

## Prompt Evaluation

The QA Test Suite Generator prompt was applied to the password reset workflow to evaluate its ability to generate test scenarios for a multi-step authentication process.

The generated output demonstrated the prompt's capability to identify functional workflows, security risks, validation scenarios, and integration points involving email delivery and password management.

---

## Generated Test Coverage Summary

The generated test suite covered:

- Functional password reset scenarios
- Negative scenarios and invalid inputs
- Boundary validation
- Security considerations
- Email delivery integration
- Token expiration handling
- API validation
- Automation recommendations

---

## Sample Generated Test Cases

### TC-PWRESET-001: Request Password Reset with Valid Email

**Priority:** High  
**Test Type:** Functional  
**Traceability:** AC-1

**Steps:**

1. Navigate to the login page.
2. Select the "Forgot Password" option.
3. Enter a registered email address.
4. Submit the password reset request.

**Expected Result:**

A password reset email is generated and sent to the registered user.

---

### TC-PWRESET-002: Password Reset Request with Invalid Email

**Priority:** High  
**Test Type:** Negative  
**Traceability:** AC-1

**Steps:**

1. Navigate to the password reset page.
2. Enter an invalid email format.
3. Submit the request.

**Expected Result:**

The system displays an appropriate validation message and does not create a reset request.

---

### TC-PWRESET-003: Expired Password Reset Link

**Priority:** High  
**Test Type:** Security / Functional  
**Traceability:** AC-3

**Steps:**

1. Request a password reset link.
2. Wait until the expiration period has passed.
3. Attempt to use the expired link.

**Expected Result:**

The system rejects the expired link and requires the user to request a new password reset.

---

### TC-PWRESET-004: Password History Validation

**Priority:** Medium  
**Test Type:** Security  
**Traceability:** AC-5

**Steps:**

1. Open a valid password reset link.
2. Enter a previously used password.
3. Submit the new password.

**Expected Result:**

The system prevents password reuse and displays an appropriate validation message.

---

## Automation Recommendations Generated

The prompt identified the following automation opportunities:

- UI automation using Playwright or Cypress.
- API testing for password reset endpoints.
- Email validation using test email services.
- Security validation for token expiration and reset flows.

---

## Evaluation Results

### Strengths

- Generated complete password reset workflow coverage.
- Identified security-related scenarios such as expired tokens and password reuse.
- Considered external dependencies like email delivery.
- Provided practical automation recommendations.

### Areas for Improvement

- Additional application-specific requirements would improve test precision.
- Email provider failure scenarios could be expanded.
- Token expiration rules should be defined by business requirements.

---

## Conclusion

The QA Test Suite Generator prompt successfully generated a structured QA test suite for a password reset workflow.

This evaluation demonstrates that the prompt can analyze authentication-related features and produce actionable test scenarios covering functionality, security, integration points, and automation opportunities.