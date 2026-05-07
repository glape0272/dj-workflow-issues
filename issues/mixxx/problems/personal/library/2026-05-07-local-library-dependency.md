# ライブラリがローカルPCに依存

## 概要

- 対象ツール: Mixxx
- 発生日: 2026-05-07
- 優先度: 中
- 状態: 未調査

## 困っていること

Mixxx のライブラリDBがローカルPCに保存されるため、別PCへ環境を持ち出してそのまま使うことが難しい

外部ストレージを接続すればすぐ使える形でライブラリを共有できず、解析済み情報や管理情報も環境ごとに分断される状態

## 再現条件

- Mixxx を複数PCで利用
- 同じ楽曲ファイルを別PCや外部ストレージから利用
- ローカルPC側のDBに依存したライブラリ状態を再利用しようとする場合

## 期待する状態

- 別PCでも同じライブラリ状態を利用できる状態
- 外部ストレージ接続だけで解析済み情報や Cue 情報を参照できる状態
- PC固有パスへの依存が少ない状態

## 現時点の回避策

- PCごとにライブラリ登録と解析を行う運用
- DBファイルや設定ファイルを手動で移行する運用

## 調査メモ

- 楽曲パス、解析情報、Cue 情報、プレイリストの保存先確認が必要
- 別PCで再利用する場合のパス依存・環境依存情報の特定が必要
- `library`、`track_locations`、`cues`、`track_analysis` 周辺の関係確認が必要

## 関連する問題

- [ライブラリ操作と検索性に課題](./2026-05-07-library-operation-friction.md)
- [解析が長い・精度が若干低い・外部解析しにくい](../analysis/2026-05-07-analysis-limitations.md)
- [MixxxとSeratoとUSB間でライブラリ状態を共有しにくい](../../../../cross-tool/problems/personal/library/2026-05-08-library-state-sharing-across-tools-and-pcs.md)
- [PC固有パスとUSBパスとストリーミング参照が混在する](../../../../cross-tool/problems/personal/library/2026-05-08-reference-paths-local-usb-streaming-mixed.md)
- [Seratoライブラリを他PCと共有しにくい](../../../../serato/problems/personal/library/2026-05-08-serato-library-sharing-between-pcs.md)

## 関連リンク

- なし
