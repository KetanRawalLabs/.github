# Repository Standards

Use these defaults for new and maintained repositories in KetanRawalLabs. Keep each repository focused on one product, library, or service. The organization owns repositories; the AI Portfolio project tracks work across them.

## Naming and metadata

- Use a short, descriptive, lowercase kebab-case repository name.
- Add a one-sentence description and only accurate GitHub topics.
- Choose public or private deliberately. Before making a repository public, inspect its full history and files for secrets, personal data, and licensed material.
- Select a license that matches the project’s intent. An organization profile or README does not grant users a software license.

## Minimum repository contents

Add what the project actually needs: a useful README.md, .gitignore, .editorconfig, license, contribution guidance, security contact, and issue or pull-request templates. Document installation, configuration, usage, support status, and known limits. Use a changelog for releases and document significant design decisions. Do not add empty boilerplate files that imply unsupported processes.

## Software quality and security

- Keep secrets, tokens, credentials, private customer data, and real .env files out of Git. Provide .env.example with placeholders only.
- Validate inputs, handle errors clearly, and use least-privilege permissions.
- Add CI checks that reflect the actual stack: formatting, linting, type checks, tests, and build. Keep checks actionable and maintained.
- Enable dependency updates and secret scanning where available. Review dependencies before adopting them.
- State supported versions, deployment assumptions, and data flows where relevant.

## AI and agent repositories

- Put the project’s top-level instructions in AGENTS.md; keep them concise, scoped, and actionable. Add more specific AGENTS.md files only when a subdirectory needs different guidance.
- Treat host-specific files such as .github/agents/*.agent.md as profiles for that host. They do not create runtime agents, delegation, hooks, or loops by themselves. Document the host and runtime that actually interpret them.
- Document tools, permissions, data handling, human approval points, failure behavior, and setup steps. Never claim that an agent can perform a capability that is not implemented and available in its runtime.
- Keep evaluation examples in evals/ or equivalent. Include expected outcomes and safety cases; do not store private conversation data.
- Distinguish model instructions, executable code, platform hooks, and workflow configuration.

## Maintenance

- Keep the default branch buildable and review changes before merging.
- Prefer issues and pull requests for work that benefits from history or collaboration; link relevant items to the AI Portfolio project.
- Archive inactive repositories with a short explanation. Delete repositories only when their contents and history are no longer needed.
- Update documentation when behavior or setup changes.
