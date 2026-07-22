# Evaluation Rubric

**Prompt:** QA Test Suite Generator  
**Version:** 3.0  
**Last Updated:** 2026-07-22

---

## Overview

This rubric defines the scoring system, pass thresholds, and quality criteria for evaluating the QA Test Suite Generator prompt. The rubric ensures consistent, objective assessment of prompt performance across different user story types and complexity levels.

---

## Scoring System

### Total Score Calculation

Each evaluation uses a 100-point scale distributed across five distinct criteria. The total score is the sum of all individual criterion scores.

**Score Range:** 0-100 points

### Grade Classification

- **95-100 points:** Excellent - Production-ready with minor refinements
- **90-94 points:** Very Good - High quality, ready for production use
- **85-89 points:** Good - Meets standards with some improvements needed
- **70-84 points:** Fair - Requires significant improvements
- **50-69 points:** Poor - Major gaps and deficiencies
- **0-49 points:** Unacceptable - Fails to meet basic requirements

---

## Pass Threshold

### Overall Pass Criteria

An evaluation **PASSES** when:

1. Total score ≥ 85 points **AND**
2. All individual criteria meet their minimum pass thresholds

An evaluation **FAILS** when:

1. Total score < 85 points **OR**
2. Any individual criterion fails its pass threshold

### Rationale for 85-Point Threshold

The 85-point threshold ensures that the prompt consistently generates high-quality test suites across all evaluation criteria. This threshold balances:

- **Quality assurance:** Ensures comprehensive coverage across all testing dimensions
- **Practical applicability:** Guarantees that generated test suites are production-ready
- **Continuous improvement:** Provides clear targets for prompt optimization

---

## Quality Rubric

### Criterion 1: Functional Test Coverage (30 points)

**Definition:** Extent to which the generated test suite covers all functional requirements specified in the acceptance criteria.

**Scoring Levels:**

| Score Range | Description | Characteristics |
|-------------|-------------|-----------------|
| 25-30 points | Excellent | All acceptance criteria have corresponding test cases with complete steps, expected results, and edge cases |
| 20-24 points | Good | Most acceptance criteria covered, minor gaps in coverage or edge cases |
| 15-19 points | Fair | Basic coverage with significant gaps, some acceptance criteria missing |
| 0-14 points | Poor | Incomplete or missing functional coverage, critical gaps |

**Pass Threshold:** 20 points

**Evaluation Checklist:**

- [ ] All acceptance criteria have corresponding test cases
- [ ] Happy path scenarios are comprehensive
- [ ] Core functionality workflows are complete
- [ ] Feature flag variations are considered
- [ ] Configuration-based scenarios are included
- [ ] Test case steps are actionable and clear
- [ ] Expected results are specific and verifiable

---

### Criterion 2: Negative Test Coverage (25 points)

**Definition:** Extent to which the generated test suite includes comprehensive negative testing scenarios including invalid inputs, error conditions, and security vulnerabilities.

**Scoring Levels:**

| Score Range | Description | Characteristics |
|-------------|-------------|-----------------|
| 20-25 points | Excellent | Comprehensive negative scenarios including SQL injection, XSS, CSRF, authentication bypass, authorization testing, and edge cases |
| 15-19 points | Good | Good negative coverage with some security scenarios missing |
| 10-14 points | Fair | Basic negative testing with limited security coverage |
| 0-9 points | Poor | Minimal or no negative testing |

**Pass Threshold:** 15 points

**Evaluation Checklist:**

- [ ] Invalid input scenarios are covered
- [ ] Error condition testing is included
- [ ] Security vulnerability testing (SQL injection, XSS, CSRF) is present
- [ ] Authentication bypass scenarios are tested
- [ ] Authorization testing (privilege escalation) is included
- [ ] Edge cases and unusual user behavior are addressed
- [ ] Session fixation and token theft scenarios are considered

---

### Criterion 3: Requirement Traceability (20 points)

**Definition:** Extent to which each test case is explicitly mapped to specific acceptance criteria or business requirements.

**Scoring Levels:**

| Score Range | Description | Characteristics |
|-------------|-------------|-----------------|
| 17-20 points | Excellent | All test cases have explicit traceability references to acceptance criteria with clear mapping |
| 13-16 points | Good | Most test cases have traceability, some missing references or unclear mapping |
| 9-12 points | Fair | Partial traceability with significant gaps and inconsistencies |
| 0-8 points | Poor | No or minimal traceability |

**Pass Threshold:** 13 points

**Evaluation Checklist:**

- [ ] All test cases include traceability references
- [ ] Traceability references are specific (e.g., AC-1, AC-2)
- [ ] Clear mapping to acceptance criteria
- [ ] Consistent traceability format across all test cases
- [ ] Traceability matrix is explicit and complete
- [ ] No orphaned test cases without traceability

---

### Criterion 4: Test Data Completeness (15 points)

**Definition:** Extent to which test data requirements are documented including valid, invalid, boundary, and PII considerations.

**Scoring Levels:**

| Score Range | Description | Characteristics |
|-------------|-------------|-----------------|
| 13-15 points | Excellent | Complete test data documentation including valid, invalid, boundary data, PII considerations, and data management strategies |
| 10-12 points | Good | Good test data coverage with some elements missing |
| 7-9 points | Fair | Basic test data documentation with significant gaps |
| 0-6 points | Poor | Minimal or no test data documentation |

**Pass Threshold:** 10 points

**Evaluation Checklist:**

- [ ] Valid test data is documented with expected behavior
- [ ] Invalid test data is listed with expected errors
- [ ] Boundary test data is specified (minimum, maximum, just beyond limits)
- [ ] Data combination strategies are defined
- [ ] Test data versioning approach is specified
- [ ] Data relationship testing is considered
- [ ] PII considerations are noted when applicable
- [ ] Data cleanup instructions are provided

---

### Criterion 5: Preconditions Documentation (10 points)

**Definition:** Extent to which preconditions are documented including application deployment status, database state, user accounts, configuration settings, and dependencies.

**Scoring Levels:**

| Score Range | Description | Characteristics |
|-------------|-------------|-----------------|
| 9-10 points | Excellent | Complete preconditions documentation covering all required elements with specific details |
| 7-8 points | Good | Good preconditions coverage with some elements missing or generic |
| 5-6 points | Fair | Basic preconditions documentation with significant gaps |
| 0-4 points | Poor | Minimal or no preconditions documentation |

**Pass Threshold:** 7 points

**Evaluation Checklist:**

- [ ] Application deployment status is specified (dev/test/staging/production)
- [ ] Database state and test data requirements are documented
- [ ] User account requirements are included
- [ ] Configuration settings are covered (including feature flags)
- [ ] Third-party service dependencies are listed
- [ ] Performance baseline establishment is specified (if applicable)
- [ ] Security tools setup is documented (if applicable)

---

## Alternative Criteria Sets

The evaluation framework supports different criteria sets based on the type of user story being evaluated. The following are validated alternative criteria that can be used instead of the standard set above.

### Alternative Set A: Boundary Testing Focus

**Use Case:** User stories with complex input validation and data limits

1. **Functional Test Coverage (30 points)** - Same as standard
2. **Negative Test Coverage (25 points)** - Same as standard
3. **Boundary Testing (20 points)** - Focus on minimum/maximum values, limit testing, threshold validation, data type boundaries
4. **Integration Testing (15 points)** - Focus on service-to-service communication, third-party integrations
5. **Output Formatting (10 points)** - Focus on adherence to test case format with all required fields

### Alternative Set B: Cross-Platform Focus

**Use Case:** Mobile or multi-platform user stories

1. **Functional Test Coverage (30 points)** - Same as standard
2. **Cross-Platform Testing (25 points)** - Focus on platform-specific behaviors, permissions, device settings
3. **Device Compatibility (20 points)** - Focus on different device settings, configurations, and behaviors
4. **Integration Testing (15 points)** - Focus on push notification providers, backend integration
5. **Automation Recommendations (10 points)** - Focus on tool-specific guidance for mobile UI and API testing

---

## Evaluation Process

### Step 1: Select Criteria Set

Choose the appropriate criteria set based on the user story type:
- **Standard set:** Web applications, general features
- **Alternative Set A:** Features with complex input validation
- **Alternative Set B:** Mobile or multi-platform features

### Step 2: Apply Scoring Rules

For each criterion, apply the scoring rules to determine the point value based on the characteristics present in the generated test suite.

### Step 3: Calculate Total Score

Sum the individual criterion scores to obtain the total score.

### Step 4: Determine Pass/Fail Status

Apply the pass threshold rules:
- Total score ≥ 85 points AND all criteria meet pass thresholds = PASS
- Total score < 85 points OR any criterion fails pass threshold = FAIL

### Step 5: Document Findings

Record strengths, areas for improvement, and specific recommendations for each criterion.

---

## Quality Benchmarks

### Historical Performance

The following benchmarks are based on iterative prompt improvements:

| Version | Average Score | Pass Rate | Key Improvements |
|---------|---------------|-----------|------------------|
| Version 1.0 | 72% | 33% | Initial baseline, basic structure |
| Version 2.0 | 88% | 100% | Added explicit negative testing, improved traceability |
| Version 3.0 | 95%+ | 100% | RTCC methodology, load-bearing instructions only |

### Target Performance

**Current Target:** 95%+ average score across all evaluations

**Rationale:** A 95%+ score demonstrates that the prompt consistently generates production-ready test suites with minimal manual intervention required.

---

## Continuous Improvement

### Iteration Guidance

When an evaluation fails or scores below 95%, use the following process:

1. **Identify failing criteria:** Determine which criteria did not meet pass thresholds or scored below target
2. **Analyze root cause:** Review the prompt instructions related to the failing criteria
3. **Formulate hypothesis:** Propose a specific prompt modification to address the gap
4. **Implement change:** Update the prompt with the modification
5. **Re-evaluate:** Run the evaluation again to measure improvement
6. **Document lessons:** Record what worked and what didn't in the iteration log

### Common Improvement Areas

Based on historical iterations, common areas for improvement include:

- **Negative test coverage:** Adding explicit instructions for security vulnerability testing
- **Requirement traceability:** Strengthening instructions for mapping test cases to acceptance criteria
- **Test data completeness:** Expanding requirements for boundary data and PII considerations
- **Preconditions documentation:** Adding specific requirements for environment and dependency documentation

---

## Appendix: Evaluation Template

```markdown
# Evaluation [ID]: [Title]

**Prompt Evaluated:** QA Test Suite Generator  
**Evaluation ID:** EVAL-[XXX]  
**Date:** [YYYY-MM-DD]

---

## Objective

[Brief description of evaluation objective]

---

## Input

[User story and acceptance criteria]

---

## Expected Output

[List of expected outputs]

---

## Evaluation Criteria

[Insert criteria from rubric]

---

## Pass/Fail Rules

[Insert pass/fail rules from rubric]

---

## Evaluation Results

### Criterion Scores

- [Criterion 1]: [Score]/[Max] (Pass/Fail)
- [Criterion 2]: [Score]/[Max] (Pass/Fail)
- [Criterion 3]: [Score]/[Max] (Pass/Fail)
- [Criterion 4]: [Score]/[Max] (Pass/Fail)
- [Criterion 5]: [Score]/[Max] (Pass/Fail)

### Total Score

**[Total]/100 ([Percentage]%)**

### Pass/Fail Status

[PASS/FAIL] - [Reason]

---

## Detailed Analysis

[Detailed analysis for each criterion]

---

## Sample Generated Output

[Sample test cases from the evaluation]

---

## Conclusion

[Summary of evaluation results and recommendations]
```
