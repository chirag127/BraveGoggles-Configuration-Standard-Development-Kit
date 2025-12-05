# Contributing to Brave-Search-Goggles-Dev-Guide

This repository is maintained by the Apex Technical Authority. We adhere to a strict **Zero-Defect, High-Velocity, Future-Proof** philosophy. Contributions that align with **December 2025/2026 standards** and the Apex Toolchain are highly valued.

## 1. Core Philosophy: Architect First

Before submitting code, ensure your changes uphold the following principles:

*   **SOLID:** Adherence to Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion principles.
*   **DRY (Don't Repeat Yourself):** Refactor immediately if patterns emerge.
*   **YAGNI (You Aren't Gonna Need It):** Only implement what is strictly necessary for the current documented goal.
*   **Clarity Over Cleverness:** Code must be maintainable by the next developer (or AI agent) onboarding.

## 2. Initial Setup & Environment

This project documentation focuses on the *understanding and building* process for Brave Goggles. The primary development environment is assumed to be a modern Linux/macOS system or WSL2 on Windows.

1.  **Fork the Repository:** Create your own fork of `chirag127/Brave-Search-Goggles-Dev-Guide`.
2.  **Clone Locally:**
    bash
    git clone https://github.com/YOUR_USERNAME/Brave-Search-Goggles-Dev-Guide.git
    cd Brave-Search-Goggles-Dev-Guide
    
3.  **Establish Upstream:**
    bash
    git remote add upstream https://github.com/chirag127/Brave-Search-Goggles-Dev-Guide.git
    
4.  **Sync Branches:** Ensure your `main` or `master` branch is up-to-date.
    bash
    git fetch upstream
    git checkout main
    git rebase upstream/main
    

## 3. Development Workflow

All contributions must originate from a feature branch following the pattern `feat/<short-description>` or `fix/<issue-number>-<short-description>`.

### A. Documentation & Guide Contributions (Markdown/Assets)

*   Ensure all Markdown adheres to common tooling standards (e.g., using Biome configuration standards for formatting, if applicable to static docs).
*   Verify all links resolve correctly within the context of the repository structure.

### B. Algorithmic & Structural Contributions (If Code is Present)

If you are contributing actual *implementation* guides or reference code (assuming a **Python/TypeScript** context based on the Apex standard, tailored to the documentation's focus):

1.  **Lint & Format:** Run local tooling *before* committing.
    bash
    # If Python environment is set up for reference code examples:
    # uv run lint
    # python -m ruff check --fix .
    
2.  **Testing:** If modifications impact technical correctness or reference code, ensure any associated unit/integration tests pass. For guides, this means manual verification against the latest Brave client behavior.
    bash
    # Example for reference code verification:
    # pytest tests/
    
3.  **Agent Directives Alignment:** Verify that your contribution does not contradict the spirit or mandates laid out in `.github/AGENTS.md`.

## 4. Pull Request Submission (The Verification Gate)

All Pull Requests (PRs) must use the provided template (`.github/PULL_REQUEST_TEMPLATE.md`).

1.  **Squash & Rebase:** PRs must be clean. Rebase your feature branch onto the latest `upstream/main` before submitting. Use interactive rebase to consolidate commits into logical steps.
2.  **Description:** Clearly state *what* you changed, *why* you changed it, and *which section* of the guide/concept it addresses.
3.  **Linking:** Link the PR to any relevant existing Issues using `Closes #XXXX` or `Addresses #XXXX`.
4.  **Reviewer Protocol:** Be prepared to address feedback promptly. Remember, the review process acts as the final human layer of QA before integration.

## 5. Reporting Issues

If you find outdated information, technical inaccuracies, or missing concepts, please open a detailed Issue using the template in `.github/ISSUE_TEMPLATE/bug_report.md`. Treat documentation gaps as critical bugs.

---