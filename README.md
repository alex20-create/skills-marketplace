# corvus-skills

A Claude Code plugin marketplace for my agent skills. Each plugin points at the skill's own repository, pinned to its latest release tag.

## Install

```
/plugin marketplace add alex20-create/skills-marketplace
/plugin install code-care-skills@corvus-skills
```

Or from a terminal:

```
claude plugin marketplace add alex20-create/skills-marketplace
claude plugin install code-care-skills@corvus-skills
```

Installed skills are namespaced by plugin, for example `code-care-skills:branch-review`.

## Plugins

| Plugin | Skills | Release |
|---|---|---|
| [security-skills](https://github.com/alex20-create/security-skills) | vet-before-install, fork-keeper | v1.5.2 |
| [code-care-skills](https://github.com/alex20-create/code-care-skills) | code-cleanup, branch-cleanup, branch-review, project-review, branch-ship | v1.3.0 |
| [session-routines](https://github.com/alex20-create/session-routines) | resume-project, skill-picker, plan-admin, wrap-up, project-director | v1.3.0 |
| [thinking-skills](https://github.com/alex20-create/thinking-skills) | aim-higher, skill-improver | v1.1.0 |
| [obsidian-project-sync](https://github.com/alex20-create/obsidian-project-sync-skill) | obsidian-project-sync | v1.1.0 |
| [workspace-setup](https://github.com/alex20-create/workspace-setup-skill) | workspace-setup | v1.2.0 |
| [deslop](https://github.com/alex20-create/deslop-skill) | deslop | v1.0.0 |

`branch-ship` and `project-director` need the Claude desktop app's session tools. Hooks that some skills offer (the wrap-up prompt hook, the code-care push gate, the Obsidian session log) are not installed by the plugins; see each skill's repository.

For claude.ai, use the `.skill` files on each repository's releases page instead.

## Updating

When a skill repository publishes a new release, bump its `ref` and `version` in `.claude-plugin/marketplace.json` and run `claude plugin validate .` before pushing.

## License

MIT. Each plugin carries its own license in its repository.
