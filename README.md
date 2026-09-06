# Claude Code — Custom AgentRouter Setup

A clean setup guide for running Claude Code with a custom AgentRouter endpoint and model configuration.

---

## Installation

### Native Install (Recommended)

**macOS, Linux, WSL:**

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

**Windows PowerShell:**

```powershell
irm https://claude.ai/install.ps1 | iex
```

**Windows CMD:**

```cmd
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd
```

Other supported installation methods include **Homebrew** and **WinGet**.

Verify:

```bash
claude --version
```

---

## AgentRouter

Register for an AgentRouter account:

[Register on AgentRouter](https://agentrouter.org/register?aff=72J0&utm_source=chatgpt.com)

After registration, obtain your API key and keep it private.

---

## Configuration

### Linux — Zsh

```bash
cat <<'EOF' >> ~/.zshrc
export ANTHROPIC_BASE_URL="https://agentrouter.org"
export ANTHROPIC_AUTH_TOKEN="YOUR_API_KEY"
export ANTHROPIC_MODEL="deepseek-v4-flash"
export CLAUDE_CODE_USE_AUTH_TOKEN="true"
export CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC="1"
EOF

source ~/.zshrc
```

### Linux — Bash

```bash
cat <<'EOF' >> ~/.bashrc
export ANTHROPIC_BASE_URL="https://agentrouter.org"
export ANTHROPIC_AUTH_TOKEN="YOUR_API_KEY"
export ANTHROPIC_MODEL="deepseek-v4-flash"
export CLAUDE_CODE_USE_AUTH_TOKEN="true"
export CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC="1"
EOF

source ~/.bashrc
```

Replace `YOUR_API_KEY` with your own API key.

---

## Verify Configuration

```bash
echo "$ANTHROPIC_BASE_URL"
echo "$ANTHROPIC_MODEL"
echo "$CLAUDE_CODE_USE_AUTH_TOKEN"
```

Never print or expose your authentication token.

---

## Launch Claude Code

```bash
cd /path/to/your/project
claude
```

---

## Environment Variables

| Variable                                   | Description                   |
| ------------------------------------------ | ----------------------------- |
| `ANTHROPIC_BASE_URL`                       | Custom API endpoint           |
| `ANTHROPIC_AUTH_TOKEN`                     | Authentication token          |
| `ANTHROPIC_MODEL`                          | Configured model              |
| `CLAUDE_CODE_USE_AUTH_TOKEN`               | Token-based authentication    |
| `CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC` | Disables nonessential traffic |

---

## Installation Troubleshooting

If installation fails with errors such as:

```text
syntax error near unexpected token '<'
403
curl error
```

check the official installation troubleshooting documentation:

[Troubleshoot Claude Code Installation](https://code.claude.com/docs/en/troubleshoot-install?utm_source=chatgpt.com#find-your-error)

On Windows:

* `PS C:\>` → PowerShell
* `C:\>` → CMD

---

## Security

* Never publish API keys.
* Do not commit credentials to Git.
* Use environment variables for secrets.
* Review commands before executing them.
* Use Claude Code only on systems you are authorized to access.

---

## Credits

- **Author:** [INTELEON404](https://github.com/INTELEON404)
- **Inspired by:** [HaxShadow](https://github.com/haxshadow)  
- **Claude Code:** [Anthropic](https://code.claude.com/docs/en/overview)
- **AgentRouter:** [AgentRouter](https://agentrouter.org/register?aff=72J0)

**AgentRouter Registration:**
[agentrouter](https://agentrouter.org/register?aff=72J0)

---

## Quick Start

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Configure your AgentRouter environment variables, then:

```bash
claude
```

---

**Built for security research, development, and authorized testing.**
