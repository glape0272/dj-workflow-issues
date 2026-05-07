# ライブラリ操作と検索性に課題

## 概要

- 対象ツール: Mixxx
- 発生日: 2026-05-07
- 優先度: 中
- 状態: 未調査

## 困っていること

楽曲数が増えた場合に目的の曲を即座に見つけにくく、ライブラリ整理や Cue 打ちの運用負荷が高くなりやすい

Cue 情報やプレイリストの整理結果を別環境や他ユーザーと共有しにくい状態

## 再現条件

- 楽曲数が多いライブラリを利用
- 別PCでも同じ Cue 情報やプレイリストを利用したい場合
- 他ユーザーや別環境と Cue 情報を共有したい場合

## 期待する状態

- Cue 情報を別環境や他ユーザーと共有できる状態
- プレイリストやクレートを整理しやすい状態
- 探している曲を即座に見つけられる状態

## 現時点の回避策

- PCごとに解析とCue打ちを行う運用
- プレイリストやクレートを手動で整理する運用

## 調査メモ

- `library`、`track_locations`、`cues`、`track_analysis` 周辺の関係整理が重要
- Cueや解析情報を外部化・同期する場合の抽出単位の検討が必要
- 検索性に関係するカラムやインデックスの確認が必要

## 関連する問題

- [ライブラリがローカルPCに依存](./2026-05-07-local-library-dependency.md)
- [動作が若干重い](./2026-05-07-library-performance.md)
- [SpotifyプレイリストとSeratoクレートとMixxxプレイリストの対応付けが難しい](../../../../cross-tool/problems/personal/playlist/2026-05-08-playlist-crate-list-mapping-friction.md)
- [曲数増加で全ツール横断の棚卸し対象が膨らむ](../../../../cross-tool/problems/personal/workflow/2026-05-08-large-library-inventory-growth-across-tools.md)
- [ライブラリ再スキャン・解析待ち・未検出曲の管理負荷](../../external/library/2026-05-07-library-scan-analysis-workflow.md)
- [SpotifyジャンルとMP3タグとDJソフト内メタデータの信頼度が揃わない](../../../../cross-tool/problems/personal/metadata/2026-05-08-metadata-trust-level-differs-by-source.md)

## 関連リンク

- なし
