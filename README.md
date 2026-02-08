# Claude iMessage Skill

A Claude Code skill for reading and sending iMessages directly from your Claude sessions.

## Features

- `/imessage read` - Read recent iMessages
- `/imessage send <recipient> <message>` - Send an iMessage
- `/imessage monitor` - Monitor for new messages and auto-respond

## Quick Install

One command to install:

```bash
git clone https://github.com/dylangroos/claude-imessage.git ~/.claude/plugins/imessage && echo "✓ iMessage skill installed! Restart Claude Code to use it."
```

Then:
1. **Restart Claude Code** (important!)
2. **Grant Full Disk Access**:
   - Open System Settings > Privacy & Security > Full Disk Access
   - Click the + button and add Terminal.app (or your IDE)
   - Restart your terminal/IDE

That's it! The skill is now available in Claude Code.

## Manual Installation

If you prefer manual setup:

1. Clone this repo:
   ```bash
   git clone https://github.com/dylangroos/claude-imessage.git
   ```

2. Create symlink to Claude plugins:
   ```bash
   ln -s ~/claude-imessage ~/.claude/plugins/imessage
   ```

3. Restart Claude Code

## Requirements

- macOS with Messages.app
- Full Disk Access permission
- Claude Code CLI

## Usage

### Read recent messages
```
/imessage read
```

### Send a message
```
/imessage send +16158819950 "Hello from Claude!"
```

### Start monitoring (auto-respond mode)
```
/imessage monitor
```

## How it works

- Reads from `~/Library/Messages/chat.db` (SQLite)
- Sends via AppleScript automation
- Uses Claude to generate intelligent responses

## License

MIT
