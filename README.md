# Claude iMessage

A Claude Code plugin that monitors your incoming iMessages and lets Claude respond intelligently — all from your terminal.

## What it does

Claude watches your Messages.app for new incoming texts, reads the conversation context, and crafts responses on your behalf. You can also read message history and send one-off replies.

- **Monitor & auto-respond** — Claude watches for new messages and responds in real-time
- **Read conversations** — Query your iMessage history by contact or time
- **Send messages** — Fire off iMessages to any contact

## Install

```bash
git clone https://github.com/dylangroos/claude-imessage.git ~/.claude/plugins/imessage
```

Then restart Claude Code and grant **Full Disk Access** to your terminal (System Settings > Privacy & Security > Full Disk Access).

## Usage

```
# Start monitoring — Claude watches for messages and responds
/imessage monitor

# Read recent messages
/imessage read

# Send a message
/imessage send +1234567890 "Hey, what's up?"
```

## How it works

- Reads from `~/Library/Messages/chat.db` (SQLite)
- Sends via AppleScript automation
- Monitors for new messages with a polling loop
- Uses Claude to generate context-aware responses

## Requirements

- macOS with Messages.app
- Full Disk Access permission for your terminal/IDE
- Claude Code

## License

MIT
