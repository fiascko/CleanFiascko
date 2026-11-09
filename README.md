# CleanFiascko

**Clean code. Simple solutions. Consistent development.**

CleanFiascko is a collection of personal AI agent skills I created to bring my coding standards, development philosophy, and preferred workflows into AI-assisted development.

It focuses on writing clean, readable, maintainable, and efficient code while keeping implementations simple, minimizing dependencies, and avoiding unnecessary complexity.

The goal is simple: keep AI-assisted development aligned with my standards and avoid unnecessary fiascos caused by poorly guided AI.

## Philosophy

CleanFiascko follows a few core principles:

- **Simplicity:** Prefer straightforward solutions over unnecessary complexity.
- **Clean Code:** Write readable, maintainable, and efficient code.
- **Reusability:** Reuse existing code and avoid unnecessary duplication.
- **Minimal Dependencies:** Prefer built-in functionality over external packages and frameworks.
- **Focused Changes:** Preserve existing behavior and avoid unrelated modifications.
- **Efficient Collaboration:** Keep communication concise and use only relevant context.
- **Compatibility:** Respect existing project conventions, technologies, and requirements.

The goal is not to enforce a complex development methodology, but to make AI-assisted development more consistent with how I work.

## Available Skills

### Fiascko Philosophy

General development guidelines applicable to all programming projects.

- Code quality and refactoring
- Communication and collaboration
- Context and token efficiency
- Git workflow and commit conventions
- Dependencies and security
- Testing and verification

[View Skill](skills/fiascko-philosophy/SKILL.md)

### Unity Development

Development guidelines for Unity and C# projects.

- Component-based architecture
- Inspector references and serialization
- Performance and memory management
- Unity lifecycle and C# conventions
- Editor and runtime compatibility
- Verification and testing

[View Skill](skills/unity-development/SKILL.md)

### Web Development

Development guidelines for web projects, with a preference for native technologies.

- Vanilla HTML, CSS, and JavaScript
- Simple and reusable architecture
- Visual identity and design consistency
- Performance and DOM optimization
- Accessibility and responsive design
- Security and browser compatibility
- Local-first and static project compatibility

[View Skill](skills/web-development/SKILL.md)

## How It Works

CleanFiascko uses Markdown-based instructions to guide AI assistants when analyzing, writing, reviewing, or modifying code.

The skills are organized into two categories:

- **General:** `fiascko-philosophy` defines the core development philosophy.
- **Specialized:** `unity-development` and `web-development` provide additional guidelines for their respective technologies.

The `AGENTS.md` file provides an index and defines how the skills should be combined.

## Usage

CleanFiascko can be used with AI assistants that support custom instructions, project files, or agent skills.

1. Download or clone this repository.
2. Provide the relevant `SKILL.md` files to your AI assistant or development environment.
3. Apply `fiascko-philosophy` alongside the appropriate specialized skill.
4. Use the skills when discussing, reviewing, or modifying code.

For ChatGPT or Claude web conversations, the skills can be provided as project files or conversation attachments, with instructions to follow the relevant guidelines.

Support for automatic skill discovery and loading depends on the AI tool and its configuration.

## Project Structure

```text
CleanFiascko/
├── skills/
│   ├── fiascko-philosophy/
│   │   └── SKILL.md
│   ├── unity-development/
│   │   └── SKILL.md
│   └── web-development/
│       └── SKILL.md
├── .gitattributes
├── .gitignore
├── AGENTS.md
├── LICENSE
└── README.md
```

## Privacy by Design

CleanFiascko consists entirely of local instruction files.

- No accounts
- No database
- No cloud services required by the repository
- No telemetry or tracking
- No external dependencies

When using these skills with an AI assistant, data handling depends on the selected AI service.

## License

CleanFiascko is released under the MIT License. See [LICENSE](LICENSE) for details.
