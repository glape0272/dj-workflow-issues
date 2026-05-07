# Serato

Serato を使った DJ ワークフロー上の課題置き場

## 記録対象

- クレート / プレイリスト管理
- 解析結果
- BPM / キー / ビートグリッド
- キュー / ループ
- 音源ファイルの配置と参照切れ
- Mixxx / Spotify との連携上の問題

## 主要論点

- Mixxx と Serato でディレクトリ、プレイリスト、クレートの設計思想が異なる問題
- Serato ライブラリを他PCと共有しにくい可能性
- Serato ライブラリを外部アプリから操作しにくい可能性
- 曲数が増えた場合の検索性、整理、参照切れ確認の負荷

## 課題メモ

問題メモは [problems/](./problems/) 配下に集約

既存メモは自分が感じている問題点として [personal/](./problems/personal/) 配下に配置

Serato 固有のクレート、ライブラリ、外部操作制約はこの配下に記録し、Mixxx、Spotify、USB との対応付けや共有問題は [Cross Tool](../cross-tool/) 側にも横断課題として記録

### ライブラリ

- [ディレクトリとクレートの設計思想がMixxxと異なる](./problems/personal/library/2026-05-08-serato-directory-playlist-crate-concept-gap.md)
- [Seratoライブラリを他PCと共有しにくい](./problems/personal/library/2026-05-08-serato-library-sharing-between-pcs.md)
- [Seratoライブラリを外部アプリから操作しにくい](./problems/personal/library/2026-05-08-serato-library-external-app-operation-limit.md)
- [曲数が増えるとSeratoライブラリ管理が難しくなる](./problems/personal/library/2026-05-08-serato-large-library-management-difficulty.md)
