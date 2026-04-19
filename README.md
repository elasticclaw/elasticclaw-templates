# elasticclaw-templates

Official template registry for [ElasticClaw](https://github.com/elasticclaw/elasticclaw).

Templates define the starting context for AI agent claws — personality, tools, memory, and workspace configuration.

## Available templates

| Template | Description |
|---|---|
| `base` | Minimal starting point. A blank-slate agent ready for any task. |

## Using templates

```bash
# Default — uses 'base' template
elasticclaw create --name my-claw

# Specify a template
elasticclaw create --template base --name my-claw

# List available templates
elasticclaw template list
```

## Template structure

Each template is a directory containing:

```
templates/<name>/
  elasticclaw-config.yaml  # provider, instance type, TTL, tags, color
  SOUL.md                  # agent personality and values
  AGENTS.md                # workspace instructions and session startup
  TOOLS.md                 # environment-specific notes and tool references
  IDENTITY.md              # agent name and metadata
  USER.md                  # about the human the agent works with
  MEMORY.md                # pre-seeded long-term memory (optional)
  memory/                  # daily memory files (optional)
```

## Contributing a template

1. Fork this repo
2. Create `templates/<your-template-name>/`
3. Add the required files (at minimum: `elasticclaw-config.yaml`, `SOUL.md`, `AGENTS.md`)
4. Open a PR

Templates must not contain secrets, API keys, or personal information.
