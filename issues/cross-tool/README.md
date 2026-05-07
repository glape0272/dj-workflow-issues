# Cross Tool

Mixxx、Serato、Spotify にまたがる課題置き場

## 記録対象

- プレイリスト移行
- メタデータ差分
- BPM / キー情報の不一致
- キュー / ループ情報の互換性
- 音源ファイルとストリーミング情報の対応付け
- 準備作業の重複
- 本番で使う環境と準備環境の差分

## 主要論点

- Spotifyプレイリスト、Seratoクレート、Mixxxプレイリストの対応付け
- USBディレクトリ分類とDJソフト側リスト分類の二重化
- Mixxx / Serato / USB 間のライブラリ状態共有
- ローカル音源、USB音源、Spotify楽曲の参照元混在
- Spotifyジャンル、MP3タグ、DJソフト内メタデータの信頼度差
- Spotify API とDJソフト側外部操作範囲の差
- 発見からDJソフト登録までの準備工程の分断

## 課題メモ

問題メモは [problems/](./problems/) 配下に集約

既存メモは自分が感じている問題点として [personal/](./problems/personal/) 配下に配置

ツール固有の制約や操作性は各ツール側に記録し、ここでは複数ツールの対応付け、共有、差分、準備工程の分断で発生する問題を記録

### プレイリスト

- [SpotifyプレイリストとSeratoクレートとMixxxプレイリストの対応付けが難しい](./problems/personal/playlist/2026-05-08-playlist-crate-list-mapping-friction.md)
- [ディレクトリ分類とプレイリスト分類が二重化する](./problems/personal/playlist/2026-05-08-directory-and-playlist-classification-duplication.md)

### ライブラリ

- [MixxxとSeratoとUSB間でライブラリ状態を共有しにくい](./problems/personal/library/2026-05-08-library-state-sharing-across-tools-and-pcs.md)
- [PC固有パスとUSBパスとストリーミング参照が混在する](./problems/personal/library/2026-05-08-reference-paths-local-usb-streaming-mixed.md)

### メタデータ

- [SpotifyジャンルとMP3タグとDJソフト内メタデータの信頼度が揃わない](./problems/personal/metadata/2026-05-08-metadata-trust-level-differs-by-source.md)
- [ローカル音源とSpotify楽曲を同一曲として対応付けにくい](./problems/personal/metadata/2026-05-08-local-track-and-spotify-track-matching.md)

### 自動化

- [Spotify APIでは操作できるがDJソフト側の外部操作範囲が限られる](./problems/personal/automation/2026-05-08-automation-scope-split-by-tool-api-limit.md)

### ワークフロー

- [発見からDJソフト登録までの準備工程が分断される](./problems/personal/workflow/2026-05-08-discovery-to-dj-prep-workflow-fragmented.md)
- [曲数増加で全ツール横断の棚卸し対象が膨らむ](./problems/personal/workflow/2026-05-08-large-library-inventory-growth-across-tools.md)
