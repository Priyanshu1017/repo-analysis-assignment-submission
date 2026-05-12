# Part 3: Prompt Preparation

Repository: beets  
Selected PR: PR #3509

---

## 3.1.1 Repository Context

Beets is an open-source Python application used for organizing and managing digital music libraries. It allows users to automatically update metadata, rename files, and structure music folders using customizable rules. The system mainly operates through a command-line interface and supports plugins for additional functionality.

The repository is intended for music collectors, developers, and users managing large music libraries. Instead of manually editing metadata and organizing folders, users can automate the process using beets.

The project addresses issues such as inconsistent metadata, duplicate tracks, and unorganized file structures. By integrating metadata services and automation workflows, beets helps users maintain clean and organized music collections.

---

## 3.1.2 Pull Request Description

PR #3509 improves reliability and validation during command execution inside beets. Previously, some commands could continue processing even when invalid states or unexpected inputs occurred. This occasionally caused unstable behavior or incomplete operations.

The PR introduces additional validation checks and improves error handling so that invalid conditions are detected earlier. Instead of allowing unstable execution to continue, the updated implementation safely stops processing when necessary.

The update also improves test coverage to ensure edge-case scenarios are handled correctly. Overall, the PR improves system stability without changing the repository architecture.

---

## 3.1.3 Acceptance Criteria

- When invalid input is detected, the system should stop safely without crashing.
- Commands should fail gracefully during unexpected conditions.
- Existing workflows should continue functioning normally.
- Unit tests should pass successfully after implementation.
- The system should prevent inconsistent library updates.
- Edge-case scenarios should be handled safely.

---

## 3.1.4 Edge Cases

1. Missing or empty metadata values.
2. Interrupted processing during command execution.
3. Unexpected plugin interactions.
4. Invalid internal execution states.

---

## 3.1.5 Initial Prompt

You are working on the beets repository, a Python-based music library management system.

Your task is to implement the changes described in PR #3509. Improve command reliability and validation so that operations fail safely when invalid states or unexpected inputs occur.

Requirements:
- Improve validation checks before processing begins.
- Add safer error-handling behavior.
- Prevent inconsistent library updates.
- Maintain compatibility with existing workflows and plugins.

Acceptance Criteria:
- Invalid inputs should not crash the application.
- Commands should fail gracefully.
- Existing workflows should continue working.
- All related unit tests must pass.

Edge Cases:
- Missing metadata values
- Interrupted processing
- Invalid command states
- Unexpected plugin behavior

Testing Requirements:
- Add or update unit tests.
- Verify stable execution under edge cases.
- Ensure no regressions are introduced.

---
