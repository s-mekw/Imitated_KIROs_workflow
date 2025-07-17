# Generic Requirements.md Generation Prompt

## Prompt

Based on the content of `user_request.md`, create a requirements definition document for the application.

**Input File:**
- `user_request.md` (A file describing the user's request)

**Specifications for the generated requirements definition document:**

1.  **Format Requirements**
    *   Describe in user story format (e.g., "As a user, I want to..., so that I can...").
    *   Clearly state the acceptance criteria for each requirement.
    *   Write acceptance criteria in a verifiable format (e.g., GIVEN-WHEN-THEN format).
    *   Describe in English.

2.  **Content Requirements**
    *   Analyze the **content of the input file** and comprehensively identify the functional and non-functional requirements that the application must satisfy.
    *   Define functional requirements focusing on features that the user directly interacts with.
    *   Also consider non-functional requirements such as performance, security, and usability.
    *   Assign a unique ID to each requirement.