# Hooks & Automation

## Hook Types

- **PreToolUse**: Before tool execution (validation, parameter modification)
- **PostToolUse**: After tool execution (auto-format, checks)
- **Stop**: When session ends (final verification)

## Recommended Hooks (in ~/.gemini/settings.json)

### PreToolUse
- **Long command reminder**: Suggests background execution for long-running commands (npm, pnpm, yarn, cargo, etc.)
- **Git push review**: Review changes before push
- **Doc blocker**: Blocks creation of unnecessary .md/.txt files

### PostToolUse
- **Prettier**: Auto-formats JS/TS files after edit
- **TypeScript check**: Runs tsc after editing .ts/.tsx files
- **console.log warning**: Warns about console.log in edited files

### Stop
- **console.log audit**: Checks all modified files for console.log before session ends

## Auto-Accept Permissions

Use with caution:
- Enable for trusted, well-defined plans
- Disable for exploratory work
- Configure `allowedTools` in `~/.gemini/settings.json`

## Task Tracking Best Practices

Use structured task tracking to:
- Track progress on multi-step tasks
- Verify understanding of instructions
- Enable real-time steering
- Show granular implementation steps

Task lists reveal:
- Out of order steps
- Missing items
- Extra unnecessary items
- Wrong granularity
- Misinterpreted requirements
