# agent-skills

A shelf for agent skills. Each skill is its own repository, included here as a git submodule. Install the skill you want. You do not have to take the set.

## Clone

```bash
git clone --recurse-submodules https://github.com/iammikek/agent-skills.git
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

## Skills

| Skill | What it does |
|---|---|
| [job-search-skill](https://github.com/iammikek/job-search-skill) | Weekly employment search. The agent drafts. You send. |

## Install one skill

Cursor and Claude Code load the folder called `skill`, inside the submodule.

### Cursor

```bash
mkdir -p ~/.cursor/skills
ln -s /path/to/agent-skills/job-search-skill/skill ~/.cursor/skills/job-search-pipeline
```

### Claude Code

```bash
mkdir -p ~/.claude/skills
ln -s /path/to/agent-skills/job-search-skill/skill ~/.claude/skills/job-search-pipeline
```

In Claude Code the command is `/job-search-pipeline`.

You can clone [job-search-skill](https://github.com/iammikek/job-search-skill) on its own and symlink that `skill/` folder instead.
