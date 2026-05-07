# Mixxx

Mixxx を使った DJ ワークフロー上の課題置き場

## 記録対象

- ライブラリ管理
- 解析結果
- BPM / キー / ビートグリッド
- キュー / ループ
- コントローラー設定
- 本番運用時の安定性
- Serato との連携上の問題

## 主要論点

- ライブラリや解析情報がローカルPCに依存しやすい問題
- 楽曲数が増えた場合の検索性、操作性、動作負荷の問題
- BPM、キー、ビートグリッド、Cue 情報を外部化・共有しにくい問題
- 初回セットアップから音を出すまでの導線がわかりにくい問題
- コントローラー対応やマッピング作成の負荷

## 課題メモ

問題メモは [problems/](./problems/) 配下に集約

既存メモは自分が感じている問題点として [personal/](./problems/personal/) 配下に配置

外部情報から見つけた問題点は [external/](./problems/external/) 配下に配置

外部情報由来の問題点は、個人製作の外部アプリで補助・変換・検証・可視化できそうなものを優先

Mixxx 固有の制約や操作性はこの配下に記録し、Serato、Spotify、USB との対応付けや共有問題は [Cross Tool](../cross-tool/) 側にも横断課題として記録

### ライブラリ

- [ライブラリがローカルPCに依存](./problems/personal/library/2026-05-07-local-library-dependency.md)
- [ライブラリ操作と検索性に課題](./problems/personal/library/2026-05-07-library-operation-friction.md)
- [動作が若干重い](./problems/personal/library/2026-05-07-library-performance.md)

### 解析

- [解析が長い・精度が若干低い・外部解析しにくい](./problems/personal/analysis/2026-05-07-analysis-limitations.md)

### コントローラー

- [対応コントローラーが少ない](./problems/personal/controller/2026-05-07-controller-support.md)

### 初期導入

- [音を出すまでの道のりが長め](./problems/personal/setup/2026-05-07-first-sound-friction.md)

## 外部情報由来の課題メモ

- [BPM・ビートグリッド解析結果の確認と修正負荷](./problems/external/analysis/2026-05-07-bpm-beatgrid-analysis-correction.md)
- [ライブラリ再スキャン・解析待ち・未検出曲の管理負荷](./problems/external/library/2026-05-07-library-scan-analysis-workflow.md)
- [Rekordbox USB・ライブラリ連携の不安定さ](./problems/external/rekordbox/2026-05-07-rekordbox-usb-library-import-instability.md)
- [オーディオ設定・レイテンシ・初期導入のつまずき](./problems/external/setup/2026-05-07-audio-latency-initial-setup-friction.md)
- [コントローラーマッピング作成と検証の負荷](./problems/external/controller/2026-05-07-controller-mapping-workflow-burden.md)
