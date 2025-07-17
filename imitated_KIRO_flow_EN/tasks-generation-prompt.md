# Generic Tasks.md Generation Prompt

## Prompt

Based on `requirements.md` and `design.md`, create a concrete implementation task list for application development.

**Input Files:**
- `requirements.md` (Requirements Definition Document)
- `design.md` (Design Document)

**Task List Specifications:**

1.  **Structured Implementation Plan**
    *   Organize tasks in a logical development order (e.g., infrastructure setup → feature implementation → testing → deployment).
    *   Consider dependencies between tasks and plan for a phased progression.
    *   Describe so that the deliverables (what will be completed) at each stage are clear.

2.  **Task Granularity**
    *   Break down each task into concrete units that an engineer can complete in about 1-3 days.
    *   Describe with executable content so that it is clear "what" and "how" to implement.

3.  **Traceability with Requirements**
    *   Clearly state which requirement (requirement ID) in `requirements.md` each task corresponds to.

4.  **Progress Management**
    *   Use Markdown checkboxes `[ ]` to manage progress.
    *   Organize tasks in a hierarchical structure as needed.

**Task List Configuration Example:**
*   **Phase 1: Initial Project Setup**
    *   `[ ]` Set up the development environment (based on the technology stack in design.md)
    *   `[ ]` Initialize the version control system (e.g., `git init`)
*   **Phase 2: Backend/API Development (if necessary)**
    *   `[ ]` Design the database schema (based on the data model in design.md)
*   **Phase 3: Frontend Development**
    *   `[ ]` Create skeletons for major components
*   **Phase 4: Testing**
    *   `[ ]` Set up unit tests
*   **Phase 5: Deployment**
    *   `[ ]` Prepare the deployment environment

Referring to the configuration example above, create a concrete and executable task list tailored to the architecture defined in `design.md`.