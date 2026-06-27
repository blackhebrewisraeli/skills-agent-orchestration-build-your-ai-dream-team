# Agent team

The Project Pulse dashboard is built by a specialized team of AI agents, orchestrated from GitHub Copilot CLI in a Codespace. Each agent has a distinct role and operates with a specific model optimized for its task.

## The Team

### Planner
- **Model**: Claude Opus 4.7 (copilot)
- **Definition**: `.github/agents/planner.agent.md`
- **Responsibility**: Creates implementation plans by researching the codebase, documentation, dependencies, and edge cases. Produces ordered implementation steps with file assignments, dependency mappings, and validation expectations. Acts as the strategic lead for all work.

### Coder
- **Model**: GPT-5.5 (copilot)
- **Definition**: `.github/agents/coder.agent.md`
- **Responsibility**: Implements code-oriented tasks with clear structure, explicit errors, and testable behavior. Writes application logic, fixes bugs, and handles runnable app configuration including `.vscode/launch.json` support for Project Pulse.

### Designer
- **Model**: Gemini 3.1 Pro (copilot)
- **Definition**: `.github/agents/designer.agent.md`
- **Responsibility**: Handles UI/UX, accessibility, information architecture, and visual design. Creates a polished dashboard with project cards, status badges, responsive layout, and deterministic CSS hooks. Prioritizes usability and user outcomes.

### Orchestrator
- **Model**: Claude Opus 4.7 (copilot)
- **Definition**: `.github/agents/orchestrator.agent.md`
- **Responsibility**: Coordinates the Planner, Coder, and Designer agents. Breaks down complex requests into phases, manages parallel and sequential execution, prevents file scope conflicts, and verifies integrated results.

## Orchestration

All work is orchestrated through **GitHub Copilot CLI in a Codespace**. The Copilot CLI launches specialist agents via the task tool, delegates explicit file scopes, and coordinates parallel execution where possible. The learner retains full control over all git operations.
