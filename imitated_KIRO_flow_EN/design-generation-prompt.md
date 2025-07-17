# Generic Design.md Generation Prompt

## Prompt

Based on `requirements.md`, create a technical selection and detailed design document for the application.

**Input File:**
- `requirements.md` (Requirements Definition Document)

**Content to include in the design document:**

1.  **Technology Stack Proposal**
    *   Propose the optimal technology stack (frontend, backend, database, etc.) to meet the requirements in `requirements.md`.
    *   Clearly state the reasons for your selection.

2.  **Architecture Design**
    *   Describe the overall system configuration in Mermaid format (e.g., component diagram, infrastructure diagram).
    *   Explain the data flow and processing flow.
    *   Describe the design principles to be adopted (e.g., loose coupling, high cohesion).

3.  **Data Model Design**
    *   Define the structure of the main data handled by the application.
    *   Use an appropriate format such as a class diagram, ER diagram, or type definitions in the selected language, as needed.

4.  **API Design (if necessary)**
    *   If the frontend and backend communicate, define the API endpoints and request/response specifications.

5.  **Error Handling Strategy**
    *   Define a policy for handling unexpected errors (e.g., input validation errors, API communication failures).
    *   Consider how to provide feedback to the user.

6.  **Test Strategy**
    *   Define a testing policy (unit tests, integration tests, E2E tests) to ensure quality.
    *   Clarify the scope and objectives of each test.

Create each section with a level of detail that allows the person in charge of the subsequent task creation and implementation phases to understand the specific work involved.