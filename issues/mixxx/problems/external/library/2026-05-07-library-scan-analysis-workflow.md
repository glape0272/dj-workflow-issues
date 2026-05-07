# ライブラリ再スキャン・解析待ち・未検出曲の管理負荷

## 概要

- 対象ツール: Mixxx
- 発生日: 2026-05-07
- 優先度: 中
- 状態: 外部情報から整理

## 困っていること

新しい曲が表示されない、BPM が表示されない、未対応形式の曲がライブラリに出ないなど、ライブラリ投入後の状態確認に手間がかかる

大量曲の解析では時間がかかり、どの曲が未解析・未検出・要変換なのか把握しにくい状態

## 再現条件

- 新規楽曲を大量追加
- ライブラリを再スキャン
- 未対応形式やプラグインが必要な形式の楽曲を追加
- BPM 表示前に解析が必要な曲を扱う場合

## 期待する状態

- Mixxx に入れる前に未対応形式や欠損ファイルを確認できる状態
- 未解析曲、解析済み曲、変換が必要な曲を一覧で把握できる状態
- 再スキャンや解析の前後差分を確認できる状態

## 個人製作アプリで対応できそうな範囲

- 音源フォルダの事前チェック
- Mixxx 対応形式かどうかの検査
- Mixxx DB と実ファイルの差分確認
- 未解析曲や BPM 未設定曲の一覧化
- 再スキャン前後の比較レポート作成

## 対応が難しそうな範囲

- Mixxx 本体のライブラリスキャン速度改善
- Mixxx 本体の解析処理速度改善
- Mixxx の内部表示更新やフォーカス制御の修正

## 調査メモ

- 公式 Troubleshooting に BPM 未表示、新曲未表示、未対応音源形式の説明あり
- GitHub issue 一覧には再スキャンや再解析、波形生成に関する open issue が見られる

## ソース

- [Mixxx 公式 Wiki / Troubleshooting](https://github.com/mixxxdj/mixxx/wiki/troubleshooting)
- [Mixxx 公式 GitHub Issues](https://github.com/mixxxdj/mixxx/issues)

## 関連リンク

- https://github.com/mixxxdj/mixxx/wiki/troubleshooting
- https://github.com/mixxxdj/mixxx/issues
