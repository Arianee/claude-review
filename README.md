# test-claude-review

Test repo pour itérer sur le workflow de PR Review par Claude Code AI.

**Ticket**: [ARI-2951](https://linear.app/arianee/issue/ARI-2951)

## Setup

Ce repo utilise l'action [`anthropics/claude-code-action@v1`](https://github.com/anthropics/claude-code-action) pour reviewer automatiquement les PRs.

### Secrets requis (niveau org)

| Secret | Description |
|--------|-------------|
| `CLAUDE_CODE_OAUTH_TOKEN` | OAuth token pour Claude Code |
| `ANTHROPIC_API_KEY` | Clé API Anthropic (alternative à OAuth) |

### Workflow

Le workflow `.github/workflows/claude-code-review.yml` se déclenche sur :
- `pull_request: [opened, synchronize, ready_for_review, reopened]`
