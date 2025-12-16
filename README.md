# skill-creator-skill

This is an improved version of the [official skill creator by Anthropic](https://github.com/anthropics/skills/tree/main/skills/skill-creator).

- Updated `SKILL.md`: replace all claude-specific terms with generic `agents`.
- Added `reference/scripts.md`: provide detailed instructions on creating scripts for the skill:
  - Use `uv` to run the script with third-party dependencies.
  - Add dry-run mode for dangerous operations.

## Motivation

While Anthropic is an impressive company, their leadership in software design is a complete disaster.

They enthusiastically introduce new concepts like `mcp` and `skills`, drawing widespread interest. However, they consistently fail to provide robust implementations for these concepts and have not established a unified distribution method.

In essence, Anthropic behaves like a politician who rallies voters with catchy slogans but, once in office, completely neglects the fundamental responsibilities of governance.

Compounding this chaotic approach is their refusal to cooperate with the broader community or other vendors, often prioritizing their own uniqueness. For instance, they persist in using the term `Claude` in generic documentation (e.g., the original `SKILL.md`). Furthermore, Claude Code remains closed-source and incompatible with the `AGENTS.md` standard. These are just a few examples of a persistent pattern.

**SHAME ON YOU, ANTHROPIC!**