# para-agents
Agents and commands to organize knowledge via the PARA method.

How to Use

cursor: as-is
antigravity: put the slash commands in .agent/workflows (why google)
claude: .claude/commands
vscode: .github/prompts (wtf microsoft)


## Usage Example

To categorize a file or folder into your PARA system, use the `para-classifier-anytime.md` rule.

Example:
```
/para-classifier-anytime.md @context_format [paste content or @file]
```

> [!IMPORTANT]
> **Before using:** Open `.para/context_format.md` and update the `PARA root` field (currently set to a placeholder) to point to your actual PARA root directory on your filesystem as an absolute path.