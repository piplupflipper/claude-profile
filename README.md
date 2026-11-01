# claude-profile

Claude Code の複数のアカウントで、`~/.claude` の設定を共有するコマンドです。

アカウントごとに `~/.claude-<名前>` を作り、`CLAUDE_CONFIG_DIR` で指して起動します。
認証情報のようにアカウントに紐づくものだけをそこへ置き、設定、skills、`projects/` などは `~/.claude` への symlink にします。
`projects/` を共有するので、別のアカウントで `claude --resume` して会話を続けられます。

## 必要なもの

- bash
- Claude Code (`claude` コマンド)

## 導入

```sh
install -m 755 claude-profile ~/.local/bin/claude-profile
```

## 使い方

```sh
claude-profile init sub            # ~/.claude-sub を作る。何度実行しても結果は同じ
claude-profile init sub --dry-run  # 実行内容だけを表示する
claude-profile run sub             # 起動する。初回は /login する
claude-profile list                # プロファイルの一覧
```

`run` の前後に書いた引数は `claude` へ渡します。

```sh
claude-profile --resume run sub
```

## ライセンス

MIT
