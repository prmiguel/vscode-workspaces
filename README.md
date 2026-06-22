# VS Code Workspaces

Multi-profile workspace files for different contexts and device types.

## Role in the Workspace

`vscode-workspaces` provides the VS Code project layout for the 5-repo workspace ecosystem. It consumes the `core` tag from `repo-registry/repos.yaml` to determine which folders appear in `core*` profiles.

See [`ai/rules/workspace-structure.md`](https://github.com/prmiguel/ai/blob/main/rules/workspace-structure.md) for the full architecture.

## Profiles

| File | Purpose |
|------|---------|
| `core.code-workspace` | All core repos, default settings |
| `core-phone.code-workspace` | Core repos + phone-optimized UI settings |
| `{profile}.code-workspace` | Custom profile for a specific project context |

## Convention

- `core*` profiles include all repos tagged `"core"` in `repo-registry/repos.yaml`
- When adding/removing a core repo, update **all** `core*.code-workspace` files
- Custom profiles extend the core set with project-specific repos

See `ai/rules/workspace-sync.md` for the full sync rule.
