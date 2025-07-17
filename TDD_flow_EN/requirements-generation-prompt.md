# Generic Requirements.md Generation Prompt (TDD Enhanced Version)

## Prompt

Based on the content of `user_request.md`, create a requirements definition document for the application, **assuming a Test-Driven Development (TDD) approach**.

**Input File:**
- `user_request.md` (A file describing the user's request)

**Specifications for the generated requirements definition document:**

1.  **Format Requirements**
    *   Describe in user story format (e.g., "As a user, I want to..., so that I can...").
    *   Clearly state the acceptance criteria for each requirement.
    *   Describe the acceptance criteria in a verifiable format (e.g., GIVEN-WHEN-THEN format), including concrete examples.

2.  **TDD-Oriented Content Requirements**
    *   **Decomposition into Minimum Viable Behaviors**: Analyze the **content of the input file** and break down the functional requirements into **independently testable, minimum viable behaviors**. These will be the target of each TDD cycle.
    *   **Acceptance Criteria as Test Scenarios**: Describe the acceptance criteria for each behavior with a level of specificity that allows them to be directly converted into test code (e.g., "Given two positive numbers, it returns their sum").
    *   **Comprehensive Coverage of Normal and Abnormal Cases**: For each behavior, define not only the expected normal result (happy path) but also edge cases and error conditions (e.g., invalid input, empty input) as acceptance criteria.
    *   **Unique IDs**: Assign unique IDs to each requirement and each acceptance criterion for later reference.
    *   **Non-Functional Requirements**: If possible, define non-functional requirements such as performance, security, and usability in an observable and testable manner.

This requirements definition document aims to be directly usable by developers as input for the "Red (write a failing test)" step of TDD.