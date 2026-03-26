# Sync_AISkills

A personal collection of Claude Code custom skills (slash commands), synced across multiple machines via Git.

## What's Inside

| File | Skill | Description |
|------|-------|-------------|
| `vfx-td.md` | `/vfx-td` | Senior VFX TD persona — Houdini, Deadline render farm, and pipeline troubleshooting |

## Usage

In Claude Code, invoke a skill with its slash command:

```
/vfx-td <your question or paste logs here>
```

## Setup on a New Machine

**Windows** (run as Administrator in cmd):
```cmd
rmdir "C:\Users\<username>\.claude\commands"
git clone https://github.com/HongYuHu/Sync_AISkills.git "C:\Users\<username>\.claude\commands"
```

**macOS / Linux:**
```bash
rm -rf ~/.claude/commands
git clone https://github.com/HongYuHu/Sync_AISkills.git ~/.claude/commands
```

## Syncing Updates

After adding or editing a skill on any machine:
```bash
cd ~/.claude/commands   # or the Windows path
git add .
git commit -m "add: skill-name"
git push
```

Pull updates on other machines:
```bash
git pull
```

## Adding a New Skill

1. Create a new `.md` file in the commands folder
2. Follow the Claude Code skill format (frontmatter + prompt body)
3. Commit and push — all machines get it on next `git pull`
