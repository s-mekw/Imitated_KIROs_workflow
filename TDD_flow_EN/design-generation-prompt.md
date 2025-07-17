# Generic Design.md Generation Prompt (TDD Enhanced Version)

## Prompt

Based on `requirements.md`, create an initial design document for the application that **reflects the principles of Test-Driven Development (TDD) and "Tidy First"**. This design is intended to evolve and be refactored through TDD cycles.

**Input File:**
- `requirements.md` (TDD-Oriented Requirements Definition Document)

**Content to include in the design document:**

1.  **Technology Stack Proposal**
    *   Propose a technology stack that meets the requirements of `requirements.md` and is **easy to automate tests for**.
    *   Clearly state the reasons for your selection, including testing frameworks and libraries.

2.  **Initial Architecture Design**
    *   **Simple Design**: Following the "You Aren't Gonna Need It" (YAGNI) principle, propose the minimum necessary architecture at this time.
    *   **Separation of Concerns**: Strive for a design that clearly separates concerns such as UI, business logic, and data access to enhance testability.
    *   Describe the overall system configuration in a simple form using Mermaid format.

3.  **Data Model Design**
    *   Define an initial draft of the main data structures handled by the application.
    *   Keep it flexible enough to be extended as TDD progresses, without being too detailed at this stage.

4.  **API Design (Interface Definition)**
    *   Define the interfaces (APIs) that will serve as boundaries between components or modules.
    *   Design each interface to have a single responsibility.

5.  **Test Strategy**
    *   **Concrete TDD Cycle**: Show a concrete plan for how to practice the Red-Green-Refactor cycle in this project.
    *   **Test Classification**: Define the roles of unit tests, integration tests, and E2E tests, and what each test will verify.
    *   **Test Doubles**: If necessary, describe the strategy for using test doubles such as stubs and mocks.

6.  **"Tidy First" Initial Plan**
    *   **Refactoring Candidates**: Look at `requirements.md` and predict and list areas that are likely to require refactoring in the future (e.g., logic that could become complex, potentially duplicate processing).
    *   This will serve as an initial guide to be mindful of "structural changes" versus "behavioral changes" during development.

This design document is not a perfect final design, but rather a "starting point" for initiating the TDD process.