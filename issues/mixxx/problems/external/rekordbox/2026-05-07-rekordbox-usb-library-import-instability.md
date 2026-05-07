# Rekordbox USB・ライブラリ連携の不安定さ

## 概要

- 対象ツール: Mixxx
- 発生日: 2026-05-07
- 優先度: 高
- 状態: 外部情報から整理

## 困っていること

Rekordbox USB や Rekordbox プレイリストを Mixxx で扱う際に、空表示、クラッシュ、UI フリーズ、キー順ソート不具合などが報告されている

本番前に USB やプレイリストが Mixxx で正しく見えるか確認しにくい状態

## 再現条件

- Rekordbox USB を Mixxx で開く
- Rekordbox プレイリストを Mixxx から参照
- キー順ソートやジョグ操作を組み合わせて利用
- macOS など特定環境で利用

## 期待する状態

- Mixxx に読み込ませる前に Rekordbox USB やライブラリの状態を検査できる状態
- Mixxx で空表示やクラッシュにつながりそうなデータを事前に検出できる状態
- Rekordbox 側のプレイリストを安全な中間形式へ変換できる状態

## 個人製作アプリで対応できそうな範囲

- Rekordbox XML や USB 内データの事前検査
- プレイリスト、曲パス、キー、BPM の一覧化
- Mixxx に渡す前の中間 CSV / M3U / JSON 生成
- 文字化け、欠損パス、重複、空プレイリストの検出
- USB 内容の検証レポート作成

## 対応が難しそうな範囲

- Mixxx 本体の Rekordbox USB 読み込み処理の修正
- Mixxx 本体クラッシュの根本修正
- Rekordbox 独自形式の完全互換再現

## 調査メモ

- 公式 GitHub issue に Rekordbox USB の空表示とクラッシュ関連の confirmed bug あり
- Reddit に Rekordbox プレイリスト利用時の UI フリーズや key sort 問題の投稿あり

## ソース

- [Mixxx 公式 GitHub Issue #13624](https://github.com/mixxxdj/mixxx/issues/13624)
- [Reddit / r/MIXXX の利用者投稿](https://www.reddit.com/r/MIXXX/comments/sxzrqh)

## 関連リンク

- https://github.com/mixxxdj/mixxx/issues/13624
- https://www.reddit.com/r/MIXXX/comments/sxzrqh
