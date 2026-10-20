# ai-news-routine

Claude Sonnet 5 / Opus 4.8 で、Fable 5 に近い品質の仕事を再現するための運用セット。

## ファイル

| ファイル | 役割 |
|---|---|
| `docs/system-prompt.md` | 常に適用する基本方針。ルールの正本はここだけ |
| `CLAUDE.md` | Claude Code 用の入口。基本方針と学びログを読み込み、作業時の追加ルールを足す |
| `.claude/skills/deep-mode/SKILL.md` | 企画・コピー・note・壁打ち・レポートを作るときの手順 |
| `docs/templates.md` | 人が依頼するときのコピペ集と、モデル・思考の深さの使い分け |
| `docs/lessons.md` | 受けた修正・好みを溜めていく学びログ |

## 使い始め方

### Claude Code でこのリポジトリを開いて作業する

追加の準備は不要。`CLAUDE.md` とスキルが自動で読み込まれる。

### Claude Code のどのリポジトリでも使う

1. `docs/system-prompt.md` の中身を `~/.claude/CLAUDE.md` に追記する。
2. `.claude/skills/deep-mode` フォルダを `~/.claude/skills/` にコピーする。

### claude.ai で使う

1. `docs/system-prompt.md` の中身を、設定の個人設定（Personal preferences）か、プロジェクトの指示に貼る。
2. スキル機能が使えるプランなら、`.claude/skills/deep-mode` フォルダを zip にしてスキルとしてアップロードする。
3. 依頼のときは `docs/templates.md` の文面をコピーして使う。

## ルールを変えるとき

基本方針は `docs/system-prompt.md` だけを編集する。`CLAUDE.md` はこのファイルを読み込んでいるので自動で反映される。claude.ai や `~/.claude/CLAUDE.md` に貼った分は貼り直す。
