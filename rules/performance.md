# Performance Optimization

## Model Strategy

Use the model that best fits the task complexity:

**Standard Tasks** (90% of work):
- Code generation and editing
- Pair programming
- Worker agents in multi-agent systems
- Simple debugging

**Complex Tasks** (Deep reasoning needed):
- Architectural decisions
- Complex debugging
- Research and analysis tasks
- Multi-system refactoring

## Context Window Management

Avoid last 20% of context window for:
- Large-scale refactoring
- Feature implementation spanning multiple files
- Debugging complex interactions

Lower context sensitivity tasks:
- Single-file edits
- Independent utility creation
- Documentation updates
- Simple bug fixes

## Deep Reasoning + Plan Mode

For complex tasks requiring deep reasoning:
1. Use `enter_plan_mode` for structured approach
2. Break into smaller sub-tasks
3. Delegate to sub-agents to keep main context lean
4. Use split role sub-agents for diverse analysis

## Build Troubleshooting

If build fails:
1. Use **build-error-resolver** agent
2. Analyze error messages
3. Fix incrementally
4. Verify after each fix

## Context Efficiency Tips

- Use `grep_search` before reading full files
- Combine independent tool calls in parallel
- Delegate heavy research to sub-agents
- Keep main session focused on orchestration
