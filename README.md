# para-agents
Agents and commands to organize knowledge via the PARA method.

How to Use

cursor: as-is
antigravity: put the slash commands in .agent/workflows (why google)
claude: .claude/commands
vscode: .github/prompts (wtf microsoft)

## Setup

Run the init command to scaffold your PARA workspace:

```
/para-init
```

This will:
1. Ask if this is a work or personal context
2. Create the base PARA folders (`Areas/`, `Projects/`, `Archives/`, `Resources/`)
3. Configure `.para/context_format.md` with your root path

## Usage Example

To categorize a file or folder into your PARA system, use the `para-classifier-anytime.md` rule.

Example:
```
/para-classifier-anytime.md @context_format [paste content or @file]
```

> [!IMPORTANT]
> **Before using:** Ensure `.para/context_format.md` has your `PARA root` set to the correct absolute path. Running `/para-init` will do this for you.