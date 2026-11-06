# claude-profile 👯‍♀️💅

[English](README.md) | **日本語**

Claude Code の複数のアカウントで、`~/.claude` の設定を共有できちゃうコマンドだよ💖✨

アカウントごとに `~/.claude-<名前>` を作って、`CLAUDE_CONFIG_DIR` でそこを指して起動するよ。  
認証情報みたいにアカウントに紐づくものだけをそこに置いて🔐、設定、skills、`projects/` とかは `~/.claude` への symlink にするよ🔗  
`projects/` を共有してるから、別のアカウントで `claude --resume` しても会話の続きができちゃう💬✨

## 🛍️ 必要なもの

- bash
- Claude Code (`claude` コマンド)

## 📦 導入

```sh
install -m 755 claude-profile ~/.local/bin/claude-profile
```

## 🎀 使い方

```sh
claude-profile init sub            # ~/.claude-sub を作る。何度実行しても結果は同じ
claude-profile init sub --dry-run  # 実行内容だけを表示する
claude-profile run sub             # 起動する。初回は /login する
claude-profile list                # プロファイルの一覧
```

`run` の前後に書いた引数は `claude` に渡すよ🎁

```sh
claude-profile --resume run sub
```

## 📜 ライセンス

MIT 💖
