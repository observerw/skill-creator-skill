# Scripts in Skills

## Overview

Scripts are executable code files (Python/Bash/etc.) included in a skill's `scripts/` directory for tasks that require deterministic reliability or are repeatedly rewritten.

## Writing Python Scripts

**All Python scripts must use `uv` as the Python environment and package manager.**

Before running or developing Python scripts, check with `uv --version` to see if `uv` is available. If not, obtain user consent then install `uv`: `curl -LsSf https://astral.sh/uv/install.sh | sh`.

### Using Third-Party Dependencies

**ATTENTION: Prioritize using Python standard library for script functionality, only use third-party dependencies when necessary.**

**All Python scripts must declare their dependencies using inline script metadata specifications** as stated in [Python packaging specifications](https://packaging.python.org/en/latest/specifications/inline-script-metadata/). Add a special comment block at the top of each Python script to declare dependencies:

```python
# /// script
# requires-python = ">=3.8"
# dependencies = [
#     "requests>=2.25.0",
#     "pandas==1.3.0",
#     "numpy",
# ]
# ///

import requests
import pandas as pd
import numpy as np

# Your script code here ...
```

## Security

**Scripts must minimize side effects.** When scripts must perform dangerous operations (file deletion, system modifications, data changes), you MUST implement a dry-run mode that:

- Shows the scope of changes without executing them
- Provides clear output of what would be modified

Before running the script, you MUST run dry-run mode first and ask user for confirmation.

## Important Notes

- Scripts may still need to be read by agents for patching or environment-specific adjustments
- Keep scripts focused and modular to maximize reusability
- Test scripts thoroughly before including them in a skill
- Include clear documentation within scripts about their purpose and usage
