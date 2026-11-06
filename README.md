# claude-profile 👯‍♀️💅

**English** | [日本語](README.ja.md)

This command lets multiple Claude Code accounts share the same `~/.claude` settings 💖✨

It makes a `~/.claude-<name>` for each account and launches Claude Code with `CLAUDE_CONFIG_DIR` pointing at it.  
Only account-bound stuff like credentials lives there 🔐, and settings, skills, `projects/` and friends are symlinks to `~/.claude` 🔗  
Since `projects/` is shared, you can `claude --resume` from a different account and keep the conversation going 💬✨

## 🛍️ Requirements

- bash
- Claude Code (the `claude` command)

## 📦 Install

```sh
install -m 755 claude-profile ~/.local/bin/claude-profile
```

## 🎀 Usage

```sh
claude-profile init sub            # create ~/.claude-sub. Same result no matter how many times you run it
claude-profile init sub --dry-run  # only print what it would do
claude-profile run sub             # launch. Do /login the first time
claude-profile list                # list profiles
```

Arguments written before or after `run` are passed through to `claude` 🎁

```sh
claude-profile --resume run sub
```

## 📜 License

MIT 💖
