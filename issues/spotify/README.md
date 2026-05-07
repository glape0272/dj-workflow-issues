# Spotify

Spotify を使った選曲、準備、参照用途での課題置き場

## 記録対象

- プレイリスト管理
- レコメンドや発見導線
- 楽曲メタデータ
- DJ ソフトへ持ち込めない情報
- ストリーミング音源とローカル音源の差分
- Serato との連携上の問題

## 主要論点

- お気に入りの曲を一時受け皿にする運用で、3000曲超になると整理負荷が高い問題
- お気に入りから用途別、ジャンル別、DJ用リストへ分ける作業の負荷
- Serato で Spotify からDJする場合、リスト整理に検索性が依存する問題
- Spotify 公式ジャンルだけではDJ用分類に使いにくい問題
- Spotify API や外部アプリでプレイリスト周りを補助できる可能性

## 課題メモ

問題メモは [problems/](./problems/) 配下に集約

既存メモは自分が感じている問題点として [personal/](./problems/personal/) 配下に配置

Spotify 固有のプレイリスト、メタデータ、API 操作はこの配下に記録し、Serato、Mixxx、USB との対応付けや準備工程の分断は [Cross Tool](../cross-tool/) 側にも横断課題として記録

### ライブラリ

- [お気に入りの曲が一時受け皿として肥大化する](./problems/personal/library/2026-05-08-spotify-liked-songs-as-intake-overload.md)

### プレイリスト

- [お気に入りから用途別リストへ分ける作業が大変](./problems/personal/playlist/2026-05-08-spotify-playlist-classification-workload.md)

### Serato連携

- [Spotifyのリスト依存でSerato上の曲探しが大変](./problems/personal/serato/2026-05-08-serato-spotify-list-dependent-search-friction.md)

### メタデータ

- [Spotify公式ジャンルだけでは分類しにくい](./problems/personal/metadata/2026-05-08-spotify-genre-metadata-accuracy-limit.md)

### 自動化

- [Spotify APIでプレイリスト操作を補助したい](./problems/personal/automation/2026-05-08-spotify-api-playlist-operation-support.md)
