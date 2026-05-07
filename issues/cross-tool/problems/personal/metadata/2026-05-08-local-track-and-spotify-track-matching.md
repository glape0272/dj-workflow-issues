# ローカル音源とSpotify楽曲を同一曲として対応付けにくい

## 概要

- 対象ツール: Spotify / USB / Mixxx / Serato
- 発生日: 2026-05-08
- 優先度: 中
- 状態: 未調査
- 出どころ: personal

## 困っていること

Spotifyで見つけた曲と、ローカルPCやUSBにある音源ファイルが同じ曲かどうかを対応付けにくい

曲名、アーティスト名、アルバム名、バージョン違い、表記ゆれがあると、Spotify上のリスト分類をローカル音源やDJソフト側へ持ち込みにくい

## 再現条件

- Spotifyで選曲や分類を行う
- ローカル音源やUSB音源として同じ曲を管理する
- 曲名、アーティスト名、リミックス名、エディット名に表記ゆれがある
- MP3版、WAV版、Spotify版が混在する

## 期待する状態

- Spotify楽曲とローカル音源の対応候補を確認できる状態
- 同一曲、別バージョン、未所持曲を分けて扱える状態
- Spotifyで作った分類をローカル音源管理へ反映しやすい状態

## 現時点の回避策

- 曲名とアーティスト名で手動確認する
- Spotifyのリストを見ながらローカル音源を検索する
- 表記ゆれがある曲は手動でタグを整える

## 個人製作アプリで対応できそうな範囲

- Spotify楽曲とローカル音源の候補マッチング
- ISRC、曲名、アーティスト名、アルバム名による照合
- 未所持候補、重複候補、別バージョン候補の抽出
- 手動確認用の対応表生成

## 対応が難しそうな範囲

- リミックス、エディット、リマスター違いの完全自動判定
- Spotify上にないローカル音源の正確な補完
- 音声内容にもとづく完全な同一判定

## 調査メモ

- ISRCが使える場合は強いが、全曲で使えるとは限らない
- Spotify版と手元音源が別マスターの可能性もある
- 最終判断は候補提示と手動確認の形が安全

## 関連する問題

- [お気に入りの曲が一時受け皿として肥大化する](../../../../spotify/problems/personal/library/2026-05-08-spotify-liked-songs-as-intake-overload.md)
- [ファイル名とタグ情報が一致しない](../../../../usb/problems/personal/format/2026-05-08-usb-filename-tag-mismatch.md)
- [MP3とWAVなどのフォーマット混在で管理が複雑化する](../../../../usb/problems/personal/format/2026-05-08-usb-audio-format-mixing.md)
- [SpotifyジャンルとMP3タグとDJソフト内メタデータの信頼度が揃わない](./2026-05-08-metadata-trust-level-differs-by-source.md)
- [PC固有パスとUSBパスとストリーミング参照が混在する](../library/2026-05-08-reference-paths-local-usb-streaming-mixed.md)
- [発見からDJソフト登録までの準備工程が分断される](../workflow/2026-05-08-discovery-to-dj-prep-workflow-fragmented.md)

## ソース

- 自分のDJワークフロー上の懸念

## 関連リンク

- なし
