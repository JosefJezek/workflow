# SpecKit

SpecKit is a powerful tool designed to help developers create and manage specifications for their software projects. It provides a structured approach to defining requirements, ensuring that all stakeholders have a clear understanding of the project's goals and expectations.

## 🔄 Spec files can be updated

To update the spec file, you need to create a new git branch with the same prefix as the spec file folder.
For example, to update `specs/001-login-page/spec.md`, create a branch named `001-fix-submit-button`.

```sh
git checkout -b 001-fix-submit-button
/speckit.clarify Update the login page to fix the alignment issue of the submit button.
/speckit.plan Test cases should be updated accordingly to cover the new changes.
/speckit.tasks
/speckit.implement
```

## constitution.md vs AGENTS.md

- File `.specify/memory/constitution.md` is used to define the project's principles and guidelines that govern the development process.
