# Rulebook
This document defines the conventions and rules for this project. It covers documentation structure, design specifications, and development practices.


## Documentation

### Structure
All documentation lives in the `/docs` folder. Create it if it doesn't exist yet.

#### `docs/index.md` — Main Entry Point
This is the root of all documentation. Keep it updated. It must follow this structure:

**Introduction**
A brief summary of the project and its main goals.

**Features**
A list of key features. Each entry should include:
- Feature name
- Brief, one-line summary
- Link to its dedicated file at `docs/features/{feature}.md`

**Get Started**
Essential information for anyone setting up or using the project.

#### `docs/features/{feature}.md` — Feature Pages
Each feature gets its own file. It should cover what the feature does, how to use it, and any relevant configuration or caveats.

### Guidelines
- **Stay current.** Keep documentation up-to-date after every meaningful change.
- **Be concise.** Avoid over-explanation and repetition. Record only essential information.
- **Write for the next reader.** Not just the current context.
- **Treat docs as a living structure.** Challenge, summarize, or restructure any file when it no longer serves its purpose clearly. Prefer a shorter, accurate document over a longer, comprehensive one.

### When to Update
- After adding or removing a feature → update `index.md` and create or remove the feature file.
- After changing behavior → update the relevant feature file.
- After structural changes → verify all `index.md` links are still valid.


## Design
All design resources, specifications, and decisions are defined in `/design.md`. If it doesn't exist yet, create it. 

### Guidelines
- **No assumptions.** If a design intent is unclear, ask before proceeding.
- **Favor the design system.** Always use existing components over recreating them from scratch.
- **Check component properties.** Before implementing a component, review its available variants and properties to use the right flavor.
- **No access to a resource?** Stop and ask the user for the asset link or relevant specifications before proceeding.
- **Work in small iterations.** Implement incrementally, but make sure each step is accurate before moving forward.

### When to Update
When a new design decision is made, a resource is added, or a preference is established, log it in `/design.md` immediately. If the file was just created, populate it with any relevant context already established in the current session.


## Code
All coding conventions, preferences, and decisions are defined in `/code.md`. If it doesn't exist yet, create it. 

### Guidelines
- **Keep it simple.** Write the simplest implementation that satisfies the requirements. Avoid unnecessary abstractions, premature generalization, or clever code.
- **Favor reuse.** Extract reusable functions, classes, or modules when logic is used more than once or is clearly independent. Refactor proactively when you notice duplication.
- **Comment intentionally.** Add comments only for non-obvious logic or important decisions. Prefer self-documenting names over explanatory comments.
- **Use existing libraries.** Before installing any new dependency, stop and ask for confirmation.
- **When in doubt, ask.** If the right approach is unclear, stop and ask rather than assuming.

### When to Update
When a new coding decision is made or a preference is established, log it in `/code.md` immediately. If the file was just created, populate it with any relevant context already established in the current session.