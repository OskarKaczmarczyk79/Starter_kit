# Claude Code Starter Kit
### by AI Agents Accelerator

A ready-to-use `.claude/` configuration folder that gives you a professional Claude Code setup in 30 seconds.

---

## What's Inside

```
.claude/
├── CLAUDE.md              # Project memory (customize this!)
├── settings.json          # Permissions + safety hooks
├── rules/
│   └── testing.md         # Auto-applied rules for test files
├── skills/
│   ├── commit-msg/        # /commit-msg — generate perfect commits
│   │   └── SKILL.md
│   ├── explain-code/      # /explain-code — understand any code
│   │   └── SKILL.md
│   ├── code-review/       # /code-review — find bugs & issues
│   │   └── SKILL.md
│   └── test-writer/       # /test-writer — generate tests
│       └── SKILL.md
└── agents/
    └── reviewer.yml       # Subagent for isolated code reviews
```

## Quick Setup (30 seconds)

### 1. Copy to your project
```bash
# Clone or download this folder
cp -r .claude/ /path/to/your/project/.claude/
```

### 2. Customize CLAUDE.md
Open `.claude/CLAUDE.md` and replace the placeholder sections with your actual:
- Project stack and description
- Build/test/lint commands
- Code conventions
- Folder structure

### 3. Start using it
```bash
cd your-project
claude
```

That's it! Claude Code will automatically load your config.

## Pre-configured Safety Hooks

Your `settings.json` includes two hooks out of the box:

### PreToolUse: Dangerous Command Blocker
Automatically **blocks** (exit code 2) any command matching:
- `rm -rf /`, `rm -rf ~`, `rm -rf .`
- `git push --force` or `git push -f`
- `DROP TABLE`, `DROP DATABASE`, `TRUNCATE`
- Fork bombs

### PostToolUse: Auto-format on Save
After Claude writes any `.ts`, `.tsx`, `.js`, or `.jsx` file, it automatically runs Prettier. Your code stays formatted without thinking about it.

## Available Skills (Slash Commands)

| Command | What it does |
|---------|-------------|
| `/commit-msg` | Generates conventional commit message from staged changes |
| `/explain-code` | Explains code in plain English, step by step |
| `/code-review` | Reviews code for bugs, security, and improvements |
| `/test-writer` | Writes comprehensive tests for existing code |

## Available Subagents

| Agent | Purpose |
|-------|---------|
| `reviewer` | Isolated code review in its own context window |

## Customization Tips

- **Add more skills**: Create a new folder in `.claude/skills/your-skill/SKILL.md`
- **Add more hooks**: Edit `settings.json` → `hooks` section
- **Add more rules**: Create `.md` files in `.claude/rules/`
- **Add more agents**: Create `.yml` files in `.claude/agents/`
- **Personal overrides**: Use `settings.local.json` (gitignored) for personal prefs

## Recommended Next Steps

1. Run `/init` to let Claude enhance your CLAUDE.md with codebase-specific details
2. Add a `.claudeignore` file to exclude large/irrelevant directories
3. Set up an MCP server for your tools (GitHub, database, etc.)
4. Install the GitHub App: `/install-github-app` for automatic PR reviews

---

**Free resource from the Claude Code course by AI Agents Accelerator**
# Starter_kit
