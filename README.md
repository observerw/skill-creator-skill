# skill-creator-skill

This is an improved version of the [official skill creator by Anthropic](https://github.com/anthropics/skills/tree/main/skills/skill-creator).

- Updated `SKILL.md`: replace all claude-specific terms with generic `agents`.
- Added `reference/scripts.md`: provide detailed instructions on creating scripts for the skill:
  - Use `uv` to run the script with third-party dependencies.
  - Add dry-run mode for dangerous operations.

## Motivation

Anthropic is a great company, but their leadership in software design is a complete disaster. 

Anthropic enthusiastically proposes new concepts like `mcp` or `skills`, attracting everyone to use them, but they completely fail to design the actual implementation of these concepts and haven't established a unified distribution method. 

In other words, Anthropic is like a politician who enthusiastically shouts political slogans to attract voters, but after taking office, completely fails to fulfill the responsibilities that a manager should undertake. 

Despite the chaos in their software design, Anthropic shows an attitude of refusing to cooperate with the community or other vendors, always trying to highlight their own uniqueness. For example, they always use the term `Claude` in generic documentation (e.g., the original `SKILL.md`). To this day, Claude Code remains closed-source and incompatible with the `AGENTS.md` standard. There are many such examples.

**SHAME ON YOU, ANTHROPIC!**