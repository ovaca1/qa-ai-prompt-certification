# Evaluation 02: Password Reset User Story Test Suite

**Prompt Evaluated:** QA Test Suite Generator  
**Evaluation ID:** EVAL-002  
**Date:** 2026-07-22

---

## Objective

Evaluate the prompt's ability to generate a comprehensive test suite for a password reset workflow, focusing on multi-step authentication processes, token expiration, password validation, and integration with email delivery systems.

---

## Input

### User Story

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

## Expected Output

The prompt should generate:

1. **Functional test cases** covering the complete password reset workflow
2. **Negative test cases** covering invalid inputs, expired tokens, and password reuse
3. **Boundary test cases** covering password complexity limits and token expiration thresholds
4. **Security test cases** covering token manipulation, email interception, and password history validation
5. **Integration test cases** covering email delivery and third-party service dependencies
6. **Test data specifications** including valid emails, invalid formats, and boundary passwords
7. **Preconditions** documenting email service setup and user account states
8. **Traceability matrix** mapping test cases to acceptance criteria
9. **Automation recommendations** for API and UI testing

---

## Evaluation Criteria

### Criterion 1: Functional Test Coverage (30 points)

**Definition:** Extent to which the generated test suite covers all functional requirements for the password reset workflow including request, delivery, and completion.

**Evaluation Rules:**
- 25-30 points: All acceptance criteria have corresponding test cases covering the complete workflow
- 20-24 points: Most acceptance criteria covered, some workflow gaps
- 15-19 points: Basic coverage with significant workflow gaps
- 0-14 points: Incomplete or missing functional coverage

**Pass Threshold:** 20 points

---

### Criterion 2: Negative Test Coverage (25 points)

**Definition:** Extent to which the generated test suite includes comprehensive negative testing scenarios including invalid emails, expired tokens, password reuse, and security vulnerabilities.

**Evaluation Rules:**
- 20-25 points: Comprehensive negative scenarios including expired tokens, password reuse, invalid emails, token manipulation, and email interception
- 15-19 points: Good negative coverage with some security scenarios missing
- 10-14 points: Basic negative testing with limited security coverage
- 0-9 points: Minimal or no negative testing

**Pass Threshold:** 15 points

---

### Criterion 3: Boundary Testing (20 points)

**Definition:** Extent to which the generated test suite includes boundary testing for password complexity requirements, token expiration time limits, and input field validations.

**Evaluation Rules:**
- 17-20 points: Comprehensive boundary testing including password complexity limits, token expiration thresholds, and input field boundaries
- 13-16 points: Good boundary coverage with some edge cases missing
- 9-12 points: Basic boundary testing with significant gaps
- 0-8 points: Minimal or no boundary testing

**Pass Threshold:** 13 points

---

### Criterion 4: Integration Testing (15 points)

**Definition:** Extent to which the generated test suite includes integration testing for email delivery, third-party services, and service-to-service communication.

**Evaluation Rules:**
- 13-15 points: Comprehensive integration testing including email delivery, service failures, and third-party dependencies
- 10-12 points: Good integration coverage with some scenarios missing
- 7-9 points: Basic integration testing
- 0-6 points: Minimal or no integration testing

**Pass Threshold:** 10 points

---

### Criterion 5: Output Formatting (10 points)

**Definition:** Extent to which the generated test suite follows the specified test case format with all required fields (Test ID, Title, Description, Priority, Severity, Traceability, Precondition, Steps, Expected Result, Estimated Execution Time, Test Data).

**Evaluation Rules:**
- 9-10 points: All test cases follow the specified format with all required fields
- 7-8 points: Most test cases follow the format with minor deviations
- 5-6 points: Basic format adherence with significant deviations
- 0-4 points: Minimal or no format adherence

**Pass Threshold:** 7 points

---

## Pass/Fail Rules

### Overall Pass Criteria

- **Pass:** Score ≥ 85 points AND all individual criteria meet their pass thresholds
- **Fail:** Score < 85 points OR any individual criterion fails its pass threshold

### Individual Criterion Pass/Fail

Each criterion must meet its minimum pass threshold. If any criterion fails, the entire evaluation fails regardless of total score.

---

## Evaluation Results

### Criterion Scores

- **Functional Test Coverage:** 27/30 (Pass)
- **Negative Test Coverage:** 22/25 (Pass)
- **Boundary Testing:** 16/20 (Pass)
- **Integration Testing:** 13/15 (Pass)
- **Output Formatting:** 9/10 (Pass)

### Total Score

**87/100 (87%)**

### Pass/Fail Status

**PASS** - All criteria met pass thresholds and total score exceeds 85 points.

---

## Detailed Analysis

### Functional Test Coverage (27/30)

**Strengths:**
- Complete password reset workflow covered from request to completion
- All acceptance criteria have corresponding test cases
- Email delivery scenarios included

**Areas for Improvement:**
- Could include more scenarios for password confirmation step
- User notification after successful reset could be more detailed

---

### Negative Test Coverage (22/25)

**Strengths:**
- Comprehensive expired token scenarios
- Password reuse validation included
- Invalid email format testing covered
- Token manipulation scenarios addressed

**Areas for Improvement:**
- Email interception scenarios could be expanded
- Concurrent reset request handling could be included

---

### Boundary Testing (16/20)

**Strengths:**
- Password complexity limits tested
- Token expiration thresholds covered
- Input field boundaries included

**Areas for Improvement:**
- Minimum password length boundary could be more detailed
- Maximum password length scenarios could be expanded
- Token expiration just-before and just-after scenarios could be more comprehensive

---

### Integration Testing (13/15)

**Strengths:**
- Email delivery integration covered
- Third-party service dependencies addressed
- Service failure scenarios included

**Areas for Improvement:**
- Email provider failure scenarios could be more detailed
- Rate limiting on reset requests could be tested

---

### Output Formatting (9/10)

**Strengths:**
- All test cases follow the specified format
- Required fields consistently included
- Clear and structured presentation

**Areas for Improvement:**
- Some test cases could have more detailed descriptions
- Estimated execution times could be more precise

---

## Sample Generated Output

### TC-PWRESET-001: Request Password Reset with Valid Email

**Test ID:** TC-PWRESET-001  
**Title:** Request Password Reset with Valid Email  
**Description:** Verify that a user can request a password reset using a registered email address  
**Priority:** P1  
**Severity:** High  
**Traceability:** AC-1  
**Precondition:** User account exists with registered email address  
**Steps:**
1. Navigate to the login page
2. Select the "Forgot Password" option
3. Enter a registered email address
4. Submit the password reset request

**Expected Result:** Password reset email is generated and sent to the registered user  
**Estimated Execution Time:** 3 minutes  
**Test Data:** Valid email: user@example.com

### TC-PWRESET-002: Password Reset Request with Invalid Email

**Test ID:** TC-PWRESET-002  
**Title:** Password Reset Request with Invalid Email  
**Description:** Verify that the system validates email format during password reset request  
**Priority:** P1  
**Severity:** High  
**Traceability:** AC-1  
**Precondition:** Password reset page is accessible  
**Steps:**
1. Navigate to the password reset page
2. Enter an invalid email format
3. Submit the request

**Expected Result:** System displays appropriate validation message and does not create a reset request  
**Estimated Execution Time:** 1 minute  
**Test Data:** Invalid email: invalid-email, Missing @: userexample.com

### TC-PWRESET-003: Expired Password Reset Link

**Test ID:** TC-PWRESET-003  
**Title:** Expired Password Reset Link  
**Description:** Verify that expired password reset links are rejected  
**Priority:** P0  
**Severity:** Critical  
**Traceability:** AC-3  
**Precondition:** Password reset link has been generated  
**Steps:**
1. Request a password reset link
2. Wait until the expiration period has passed (1 hour)
3. Attempt to use the expired link

**Expected Result:** System rejects the expired link and requires the user to request a new password reset  
**Estimated Execution Time:** 65 minutes  
**Test Data:** Valid email: user@example.com, Expiration time: 1 hour

### TC-PWRESET-004: Password History Validation

**Test ID:** TC-PWRESET-004  
**Title:** Password History Validation  
**Description:** Verify that users cannot reuse previous passwords  
**Priority:** P1  
**Severity:** High  
**Traceability:** AC-5  
**Precondition:** User has password history with previous passwords  
**Steps:**
1. Open a valid password reset link
2. Enter a previously used password
3. Submit the new password

**Expected Result:** System prevents password reuse and displays appropriate validation message  
**Estimated Execution Time:** 2 minutes  
**Test Data:** Previous password: OldPass123!, New password attempt: OldPass123!

---

## Conclusion

The QA Test Suite Generator prompt successfully generated a comprehensive test suite for the password reset workflow, achieving a score of 87/100. The prompt demonstrated strong performance across all evaluation criteria, particularly in functional coverage, negative testing, and integration testing. The test suite effectively covers the multi-step authentication process including email delivery, token expiration, and password validation.