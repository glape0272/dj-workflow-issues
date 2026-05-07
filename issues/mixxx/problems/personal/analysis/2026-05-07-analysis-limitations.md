# 解析が長い・精度が若干低い・外部解析しにくい

## 概要

- 対象ツール: Mixxx
- 発生日: 2026-05-07
- 優先度: 高
- 状態: 未調査

## 困っていること

曲数の多さがそのまま解析時間の長さにつながりやすい

ビートグリッド周りの精度が若干低く、変則BPMの楽曲では特に課題が出やすい

外部から解析したい場合は、Mixxx 内部の解析の仕組みと DB 保存形式を調査する必要がある

## 再現条件

- 大量の楽曲を初回解析
- 変則BPMやテンポ変化のある楽曲を解析
- 外部ツールの解析結果を Mixxx 側へ反映したい場合

## 期待する状態

- 大量楽曲でも解析時間を抑えられる状態
- BPMやビートグリッドの精度が安定している状態
- 外部解析結果を Mixxx へ取り込める状態

## 現時点の回避策

- Mixxx 内部の解析完了を待つ運用
- BPMやビートグリッドを手作業で修正
- 解析対象曲を分割して処理

## 調査メモ

- `track_analysis` に保存される解析データの内容確認が必要
- BPM、波形、ビートグリッド、Cue 情報の保存先と形式の確認が必要
- 外部解析結果を反映する場合の更新対象と整合性条件の調査が必要

## 関連する問題

- [ライブラリがローカルPCに依存](../library/2026-05-07-local-library-dependency.md)
- [ライブラリ操作と検索性に課題](../library/2026-05-07-library-operation-friction.md)
- [Spotify APIでは操作できるがDJソフト側の外部操作範囲が限られる](../../../../cross-tool/problems/personal/automation/2026-05-08-automation-scope-split-by-tool-api-limit.md)
- [BPM・ビートグリッド解析結果の確認と修正負荷](../../external/analysis/2026-05-07-bpm-beatgrid-analysis-correction.md)
- [ライブラリ再スキャン・解析待ち・未検出曲の管理負荷](../../external/library/2026-05-07-library-scan-analysis-workflow.md)

## 関連リンク

- なし
