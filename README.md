````md
# Init Command

This command sets up opencode commands and agents, as well as cursor commands on the user's machine. It works as an upsert operation - updating existing files or creating new ones as needed.

## Instructions

Execute the following steps to initialize the configurations:

### 1. Setup OpenCode Configuration

Create the OpenCode directories if they don't exist and copy all files from @OPENCODE_ASSETS/:

```bash
# Create directories if they don't exist
mkdir -p ~/.opencode/agent
mkdir -p ~/.opencode/command
mkdir -p ~/.opencode/themes

# Copy agent files
cp -u OPENCODE_ASSETS/agent/*.md ~/.opencode/agent/

# Copy command files
cp -u OPENCODE_ASSETS/command/*.md ~/.opencode/command/

# Copy theme files
cp -u OPENCODE_ASSETS/themes/*.json ~/.opencode/themes/
```
````

````

### 2. Setup Cursor Configuration

Create the Cursor commands directory if it doesn't exist and copy all files from @CURSOR_ASSETS/commands/:

```bash
# Create directory if it doesn't exist
mkdir -p ~/.cursor/commands

# Copy cursor command files
cp -u CURSOR_ASSETS/commands/*.md ~/.cursor/commands/
```

## Notes

- The `cp -u` flag ensures existing files are only overwritten if the source is newer
- All necessary parent directories will be created if they don't already exist
- After setup, users can run OpenCode commands and Cursor commands from their respective directories

```
````
