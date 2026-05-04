# SpecKit

SpecKit is a powerful tool designed to help developers create and manage specifications for their software projects. It provides a structured approach to defining requirements, ensuring that all stakeholders have a clear understanding of the project's goals and expectations.

## Key Features

- **Specification Creation**: Easily create detailed specifications for your projects, outlining the requirements and expectations.
- **Version Control**: Manage different versions of your specifications, allowing for easy updates and tracking of changes over time.
- **Collaboration**: Collaborate with team members and stakeholders to ensure that everyone is on the same page regarding the project's requirements and goals.
- **Documentation**: Generate comprehensive documentation from your specifications, providing a clear reference for developers and stakeholders throughout the project lifecycle.

## Facts

- Your agents never see other people's runs, they never see your entire code base, they never see all the decisions you or other agents have made before they make a change. So the agent's decisions are always local, which leads to exactly the problems described above. A huge amount of duplicate code, abstractions for the sake of abstractions.
- The agent misses existing code, duplicates things, introduces inconsistencies. And then they blossom into a beautiful shit flower of complexity.
- The point is: let the agent do boring things, things that don't teach you anything new, or try different things that you wouldn't otherwise have time to do. Then you evaluate what the agent came up with, take the ideas that are actually reasonable and correct, and finish the implementation. Yes, sure, you can use an agent for this last step too.
- Using AI / agents does not mean that you do not need to know how your code works inside, for us it means that we can deliver quality that would not have been possible before.

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

## Resources

- <https://mariozechner.at/posts/2026-03-25-thoughts-on-slowing-the-fuck-down/>
