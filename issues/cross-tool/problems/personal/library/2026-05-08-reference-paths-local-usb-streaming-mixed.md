# PC固有パスとUSBパスとストリーミング参照が混在する

## 概要

- 対象ツール: Mixxx / Serato / Spotify / USB
- 発生日: 2026-05-08
- 優先度: 中
- 状態: 未調査
- 出どころ: personal

## 困っていること

ローカルPC上の音源、USB上の音源、Spotify上のストリーミング楽曲が混在すると、曲をどこから参照しているのか分かりにくい

同じ曲でも、ローカルファイル、USBコピー、Spotify上の楽曲として別々に存在し、参照切れや重複管理の原因になる状態

## 再現条件

- ローカルPC、USB、Spotifyを併用
- 同じ曲が複数の参照元に存在
- SeratoやMixxxでローカル / USB音源を扱う
- Spotifyを選曲やSerato連携の参照元として使う

## 期待する状態

- 各曲の参照元が分かる状態
- ローカル音源、USB音源、Spotify楽曲の対応関係が見える状態
- 参照切れや重複登録を確認できる状態

## 現時点の回避策

- PC側マスター音源フォルダを正として扱う
- USBは投入先として扱い、直接編集を避ける
- Spotifyは選曲元として扱い、ローカル音源との対応は手動確認する

## 個人製作アプリで対応できそうな範囲

- ローカル音源、USB音源、Spotify候補の対応表作成
- DJソフト側参照パスの棚卸し
- 参照切れ、重複参照、USB側のみ存在する曲の検出
- Spotify候補とローカル音源の照合補助

## 対応が難しそうな範囲

- Spotify楽曲とローカル音源の完全な同一曲判定
- 各DJソフトの参照仕様差の解消
- ストリーミング音源をローカル音源と同じように扱うこと

## 調査メモ

- 音源の実体、DJソフト内参照、Spotify上の候補を分けて管理する必要
- ISRCやアーティスト、曲名、アルバム名が照合に使える可能性
- USB運用ではパス固定が重要

## 関連する問題

- [USBとマスター音源フォルダの差分確認が難しい](../../../../usb/problems/personal/backup/2026-05-08-usb-master-library-diff.md)
- [Spotifyのリスト依存でSerato上の曲探しが大変](../../../../spotify/problems/personal/serato/2026-05-08-serato-spotify-list-dependent-search-friction.md)
- [ファイル名とタグ情報が一致しない](../../../../usb/problems/personal/format/2026-05-08-usb-filename-tag-mismatch.md)
- [MixxxとSeratoとUSB間でライブラリ状態を共有しにくい](./2026-05-08-library-state-sharing-across-tools-and-pcs.md)
- [ローカル音源とSpotify楽曲を同一曲として対応付けにくい](../metadata/2026-05-08-local-track-and-spotify-track-matching.md)
- [ライブラリがローカルPCに依存](../../../../mixxx/problems/personal/library/2026-05-07-local-library-dependency.md)

## ソース

- 自分のDJワークフロー上の懸念

## 関連リンク

- なし
