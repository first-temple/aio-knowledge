# aio-knowledge

Google公式の「生成AI検索向け最適化ガイド」をはじめとするAI検索・SEO関連の一次情報を日本語ナレッジに整理したリポジトリ。

サイト構築・コンテンツ制作・SEO/AIO施策の判断軸として、First Temple 社内および関連プロジェクトで参照する。

> **このリポジトリは公開ミラーです**。一次編集はObsidian Vault（`obsi/ClaudeCode/knowledge/SEO/`）で行い、本リポジトリには公開可能な確定版を同期する運用。グローバル `~/.claude/CLAUDE.md` の「ドメインナレッジ参照表」からも辿れるようにしている。

## 収録ドキュメント

| ファイル | 概要 | 出典 |
|---|---|---|
| [Google公式-AI検索最適化ガイド.md](./Google公式-AI検索最適化ガイド.md) | AI Overviews / AI Mode 向けの公式最適化指針。やるべきこと/避けるべきこと、E-E-A-T、Who/How/Why、スパムポリシー、技術要件を網羅 | [developers.google.com/search/docs/fundamentals/ai-optimization-guide](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide) ほか公式ドキュメント群 |

## 使い方

- 新規サイト立ち上げ時：「サイト構築時のチェックリスト」セクションを上から潰す
- コンテンツ制作時：「Helpful, Reliable, People-First」の自己診断質問にYES/NOで答える
- AIO/GEOの新しい施策提案を見たとき：「やってはいけないこと（Mythbusting）」表と「スパムポリシー」表で照合

## 重要な前提

Google公式の結論：

> **AI検索向けの「特別な最適化」は存在しない。AI機能はコアランキングシステムの上に乗っているため、従来のSEOがそのままAI最適化になる。**

llms.txt・AI専用Markdown・コンテンツのチャンキング・特定文体での執筆・人工的なメンション獲得などはいずれも公式に否定されている。

## 更新運用

- 公式ドキュメントは継続的に更新されるため、四半期に一度程度差分確認を行う
- 大きな仕様変更（新AI機能・新スパムポリシー類型など）があれば該当セクションを追記
- 改訂はファイル末尾の「改訂履歴」に追記

## ライセンス・帰属

- 本リポジトリの整理・解説部分は First Temple 社内利用を主眼とする
- 引用している公式ドキュメントは Google LLC の Creative Commons Attribution 4.0 License および Apache 2.0 License（コード例）に従う
- 出典：[Google Developers Site Policies](https://developers.google.com/site-policies)
