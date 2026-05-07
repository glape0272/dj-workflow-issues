# SpotifyジャンルとMP3タグとDJソフト内メタデータの信頼度が揃わない

## 概要

- 対象ツール: Spotify / USB / Mixxx / Serato
- 発生日: 2026-05-08
- 優先度: 中
- 状態: 未調査
- 出どころ: personal

## 困っていること

Spotify公式ジャンル、MP3タグ、ファイル名、MixxxやSerato内のメタデータはそれぞれ由来と信頼度が異なる

どの情報を分類や検索の正として扱うか決めないと、リスト分類、検索、重複検出、ローカル音源との対応付けが不安定になる

## 再現条件

- Spotifyのジャンル情報を分類に使う
- MP3タグやファイル名でローカル音源を管理
- MixxxやSeratoで解析済み情報やライブラリ表示を使う
- 同じ曲に複数のメタデータ元が存在

## 期待する状態

- メタデータごとの信頼度と用途が決まっている状態
- 分類に使う情報と表示に使う情報が切り分けられている状態
- 不一致を検出して手動確認できる状態

## 現時点の回避策

- Spotifyジャンルは補助情報として扱う
- MP3タグを基本の管理情報として整備する
- ファイル名とタグ情報の不一致を手動で確認する

## 個人製作アプリで対応できそうな範囲

- Spotify情報、MP3タグ、ファイル名、DJソフト情報の突合
- 不一致項目の一覧化
- 情報元ごとの信頼度ルールの適用
- 分類候補と確認対象の生成

## 対応が難しそうな範囲

- Spotify公式ジャンルの精度改善
- 正しいジャンルや用途分類の完全自動判断
- DJソフト内部メタデータの完全な読み書き

## 調査メモ

- ジャンル、BPM、キー、曲名、アーティスト名で情報元ごとの扱いを分ける必要
- 最初は表示名と分類候補の不一致検出から始めるとよさそう
- 信頼度ルールを固定せず、手動修正できる形が必要

## 関連する問題

- [Spotify公式ジャンルだけでは分類しにくい](../../../../spotify/problems/personal/metadata/2026-05-08-spotify-genre-metadata-accuracy-limit.md)
- [ファイル名とタグ情報が一致しない](../../../../usb/problems/personal/format/2026-05-08-usb-filename-tag-mismatch.md)
- [ライブラリ操作と検索性に課題](../../../../mixxx/problems/personal/library/2026-05-07-library-operation-friction.md)
- [ローカル音源とSpotify楽曲を同一曲として対応付けにくい](./2026-05-08-local-track-and-spotify-track-matching.md)
- [Spotify APIでプレイリスト操作を補助したい](../../../../spotify/problems/personal/automation/2026-05-08-spotify-api-playlist-operation-support.md)
- [MP3とWAVなどのフォーマット混在で管理が複雑化する](../../../../usb/problems/personal/format/2026-05-08-usb-audio-format-mixing.md)

## ソース

- 自分のDJワークフロー上の懸念

## 関連リンク

- なし
