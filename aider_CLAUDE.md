# Aider Project Context

Welcome to the **Aider** repository. This project is a specialized AI-powered coding assistant that works directly in your terminal, allowing you to edit code in your local git repository using LLMs.

## Project Goal
To provide a seamless, high-performance CLI interface for AI to write, edit, and refactor code, while maintaining proper version control (Git) integration.

## Key Principles for AI Assistants
When modifying or extending this codebase, please keep these priorities in mind:

1.  **Git-Centric Workflow:** Every change must respect Git. Aider automatically commits changes to the repository, so ensure all file operations are compatible with standard Git workflows.
2.  **Terminal-First UX:** The interface and logic should be optimized for terminal usage. Keep output clean, concise, and informative.
3.  **LLM Context Management:** Efficiently manage the "context window" when passing files to the AI. Only send relevant code snippets to minimize token usage while maintaining accuracy.
4.  **Robust Error Handling:** Since this tool interacts directly with user code, it must handle file I/O errors, git conflicts, and LLM failures gracefully without crashing the user's workflow.
5.  **Code Safety:** When performing automated edits, prioritize safety. Use dry-runs or validation checks whenever possible.

## Key Architectural Components
*   `aider/`: The core logic, including LLM interaction, git management, and command parsing.
*   `aider/coders/`: Logic for handling different coding tasks and conversation strategies.
*   `aider/models/`: Configuration and adapters for different LLM providers.
*   `tests/`: Comprehensive test suite to ensure no regressions in code editing capabilities.

## Workflow Guidelines
*   **Testing:** Run the full test suite before proposing significant architectural changes.
*   **Performance:** Aider is used by developers to speed up workflows. Ensure new features do not introduce latency.
*   **Compliance:** Maintain compatibility with existing Aider/aider features while adding custom improvements.

---
*Last updated: 2026-06-16*
