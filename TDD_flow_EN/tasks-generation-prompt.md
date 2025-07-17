# Generic Tasks.md Generation Prompt (TDD Enhanced Version)

## Prompt

Based on `requirements.md` and `design.md`, create a task list to **specifically execute the Test-Driven Development (TDD) cycle**.

**Input Files:**
- `requirements.md` (TDD-Oriented Requirements Definition Document)
- `design.md` (TDD-Oriented Design Document)

**Task List Specifications:**

1.  **Task Structure Based on TDD Cycle**
    *   Create a task group for each **minimum viable behavior** defined in `requirements.md`.
    *   Clearly break down each task group into **Red → Green → Refactor** steps.

2.  **Concrete and Executable Tasks**
    *   **Red (Write Test)**: Describe in the format "Write a failing test to verify...". Specify the target requirement ID.
    *   **Green (Implement)**: Describe in the format "Implement the minimum code to pass the test".
    *   **Refactor**: Describe in the format "Clean the code (e.g., eliminate duplication, improve naming)". If refactoring is not necessary, state so.

3.  **Incorporation of "Tidy First"**
    *   If a major structural change is deemed necessary based on the "Refactoring Candidates" in `design.md` or the development context, insert it as a separate task at the appropriate position in the list.
    *   Describe structural change tasks distinctly from behavioral change tasks (e.g., with a `[STRUCTURAL]` prefix).

4.  **Progress Management and Traceability**
    *   Use Markdown checkboxes `[ ]`.
    *   Clearly indicate which requirement each TDD cycle is based on.

**Task List Configuration Example:**

*   **Requirement ID: REQ-001 (User Login Feature)**
    *   **Behavior: Can log in with valid credentials**
        *   `[ ]` **Red**: Add a failing API-level test to verify successful login with a valid ID and password (REQ-001-AC1)
        *   `[ ]` **Green**: Implement the login API to pass the test
        *   `[ ]` **Refactor**: Improve the authentication logic for duplication and naming
    *   **Behavior: Cannot log in with invalid credentials**
        *   `[ ]` **Red**: Add a test to verify login failure with an invalid password (REQ-001-AC2)
        *   `[ ]` **Green**: Implement the password validation logic to pass the test
        *   `[ ]` **Refactor**: No refactoring needed at this time

*   **[STRUCTURAL] Structural Change: Extract Authentication Module**
    *   `[ ]` Move related authentication code to `AuthService`
    *   `[ ]` Confirm that all tests pass

This task list serves as a concrete guide for developers to follow the discipline of TDD and proceed with development step by step.