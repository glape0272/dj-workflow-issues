# BPM・ビートグリッド解析結果の確認と修正負荷

## 概要

- 対象ツール: Mixxx
- 発生日: 2026-05-07
- 優先度: 高
- 状態: 外部情報から整理

## 困っていること

Mixxx の BPM 検出やビートグリッドが、楽曲ジャンルやテンポ変化によってずれる場合がある

DnB、disco、rock、生演奏、テンポ変化のある楽曲では、手動修正や再解析が必要になりやすい状態

## 再現条件

- 変則 BPM やテンポ変化のある楽曲を解析
- キックが曖昧な楽曲を解析
- 大量楽曲を解析したあと、誤検出曲を探す場合

## 期待する状態

- 誤検出の可能性が高い楽曲を事前に見つけられる状態
- BPM 倍半分、ビートグリッドずれ、変則 BPM を一覧で確認できる状態
- Mixxx 側で手修正すべき曲を優先順位づけできる状態

## 個人製作アプリで対応できそうな範囲

- Mixxx DB から BPM、解析日時、Cue、ファイルパスを読み出す補助
- 外部 BPM 解析結果との比較レポート作成
- BPM が倍半分になっていそうな曲の検出
- 手修正候補リストの生成
- Mixxx に取り込む前の事前解析ワークフロー作成

## 対応が難しそうな範囲

- Mixxx 本体の解析アルゴリズム改善
- Mixxx 本体 UI 上のビートグリッド編集機能改善
- 可変テンポ楽曲の完全自動補正

## 調査メモ

- 公式 Troubleshooting に BPM 誤検出とビートグリッドずれの対処項目あり
- 公式 Wiki に beatgrid の制約としてテンポ変化や生演奏の揺れが記載
- Reddit でも DnB、disco、rock などで手修正が必要という利用者投稿あり

## ソース

- [Mixxx 公式 Wiki / Troubleshooting](https://github.com/mixxxdj/mixxx/wiki/troubleshooting)
- [Mixxx 公式 Wiki / Beat and Bar Edit Workflow](https://github.com/mixxxdj/mixxx/wiki/Beat-and-Bar-Edit-Workflow)
- [Reddit / r/MIXXX の利用者投稿](https://www.reddit.com/r/MIXXX/comments/1reb08m/beatmatching_on_mixxx_linux_os_fedora_kde/)

## 関連する問題

- [解析が長い・精度が若干低い・外部解析しにくい](../../personal/analysis/2026-05-07-analysis-limitations.md)
- [ライブラリ再スキャン・解析待ち・未検出曲の管理負荷](../library/2026-05-07-library-scan-analysis-workflow.md)
- [Spotify APIでは操作できるがDJソフト側の外部操作範囲が限られる](../../../../cross-tool/problems/personal/automation/2026-05-08-automation-scope-split-by-tool-api-limit.md)

## 関連リンク

- https://github.com/mixxxdj/mixxx/wiki/troubleshooting
- https://github.com/mixxxdj/mixxx/wiki/Beat-and-Bar-Edit-Workflow
- https://www.reddit.com/r/MIXXX/comments/1reb08m/beatmatching_on_mixxx_linux_os_fedora_kde/
