# Agent team

I will use GitHub Copilot CLI in a Codespace to orchestrate the custom agent team building Mona's Project Pulse dashboard.

The Planner researches the repository and prepares an implementation plan first. The Orchestrator turns that plan into phases and assigns clear file scopes. The Designer and Coder then handle design and implementation work in parallel only when their scopes and dependencies do not conflict; otherwise, the Orchestrator runs the work in sequence. Finally, the Orchestrator checks that the pieces are integrated and reports the result.

| Agent | Target model | Responsibility | Definition |
|---|---|---|---|
| Orchestrator | Claude Opus 5.5 (copilot) | Breaks work into phases, delegates to specialists with explicit file scopes, coordinates dependencies, and verifies the integrated result. | `.github/agents/orchestrator.agent.md` |
| Planner | Claude Opus 5.5 (copilot) | Researches the repository and relevant documentation, then produces an implementation plan with steps, file assignments, dependencies, risks, edge cases, and validation expectations. | `.github/agents/planner.agent.md` |
| Coder | GPT-5.5 (copilot) | Implements assigned application logic and runnable-app support, following repository patterns and validating changes. | `.github/agents/coder.agent.md` |
| Designer | Gemini 3.7 Flash (copilot) | Shapes the dashboard's user experience, visual hierarchy, accessibility, interactions, and responsive design. | `.github/agents/designer.agent.md` |
