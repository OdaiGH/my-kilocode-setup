# My Kilo AI CLI Setup

Kilo AI configuration.

## Structure

```
├── kilo.json           # Model & permission config
├── mcp.json            # MCP server integrations (GitHub)
└── .kilocode/          # Per-mode rules

    ├── general.md
    ├── rules-code/
    ├── rules-architect/
    ├── rules-debugger/
    ├── rules-security-audit/
    ├── rules-test-writer/
    ├── rules-code-reviewer/
    └── rules-docs-writer/
    └── skills/
    └── commands/
    └── workflows/
```

## Models

|Context    |Model                                   |
|-----------|----------------------------------------|
|**Primary**|`nvidia/nemotron-3-super-120b-a12b:free`|
|**Code**   |`kilo/minimax/minimax-m2.5:free`        |

## Available Modes

|Mode          |Command                    |Use                     |
|--------------|---------------------------|------------------------|
|Code          |`kilo code "..."`          |Generate/modify code    |
|Architect     |`kilo architect "..."`     |System design & planning|
|Debug         |`kilo debug "..."`         |Find & fix bugs         |
|Security Audit|`kilo security-audit "..."`|Vulnerability review    |
|Test Writer   |`kilo test-writer "..."`   |Generate tests          |
|Code Reviewer |`kilo code-reviewer "..."` |Code quality analysis   |
|Docs Writer   |`kilo docs-writer "..."`   |Documentation           |

## Setup

```bash
npm install -g kilo
cp kilo.json mcp.json .kilocode ~/.kilo/config/
# Add GitHub token to mcp.json
kilo code "Your task here"
```