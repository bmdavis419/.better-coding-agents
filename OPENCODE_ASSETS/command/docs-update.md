---
description: Update the linked codebases to the latest version
agent: build
---

# Update Command

This command updates all the linked codebases (svelte.dev, effect, and neverthrow) to their latest versions by pulling fresh changes from the upstream repositories.

You will need to run the following commands in this directory: `~/.better-coding-agents`

## Instructions

Execute the following git subtree pull commands in sequence to update each repository:

1. **Update Svelte docs**

   ```bash
   git subtree pull --prefix resources/svelte.dev https://github.com/sveltejs/svelte.dev.git main
   ```

2. **Update Effect repository**

   ```bash
   git subtree pull --prefix resources/effect https://github.com/Effect-TS/effect.git main
   ```

3. **Update neverthrow repository**
   ```bash
   git subtree pull --prefix resources/neverthrow https://github.com/supermacro/neverthrow.git master
   ```

Each command will fetch the latest changes from the upstream repository and merge them into the local subtree. There should be no conflicts, if there are ask the user what they want to do.
