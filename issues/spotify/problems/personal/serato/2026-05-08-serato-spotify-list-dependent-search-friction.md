# Spotifyのリスト依存でSerato上の曲探しが大変

## 概要

- 対象ツール: Spotify / Serato
- 発生日: 2026-05-08
- 優先度: 中
- 状態: 未調査
- 出どころ: personal

## 困っていること

Serato で Spotify からDJをする場合、曲探しがリスト整理に依存しやすい

Spotify側のリストが未整理だと、Serato上で目的の曲を探すのも大変になり、DJ中の選曲や準備に影響する可能性

## 再現条件

- Serato で Spotify の曲やリストを参照してDJする
- Spotifyのお気に入りの曲やプレイリストが大量にある
- リスト分類が未整理または粗い状態
- DJ中に目的の曲を素早く探したい場合

## 期待する状態

- Serato上で参照しやすいSpotifyリスト構成
- DJ用途に合うプレイリストが事前に整理されている状態
- 曲数が増えても目的の曲を探しやすい状態

## 現時点の回避策

- Spotify側でDJ用リストを手動作成する
- お気に入りの曲を直接探すのではなく、用途別リストから選ぶ
- Seratoで使う前にSpotify側のリストを整理する

## 個人製作アプリで対応できそうな範囲

- Seratoで使いやすいSpotifyリスト案の生成
- 未分類曲やリスト未所属曲の抽出
- DJ用途別のプレイリスト作成補助
- Spotifyリストの棚卸し結果の一覧化

## 対応が難しそうな範囲

- Serato側のSpotify参照UIそのものの改善
- DJ中の文脈に応じた最適曲の完全自動提示
- SpotifyとSeratoの連携仕様差の解消

## 調査メモ

- Serato側で扱いやすい単位に合わせてSpotifyリストを作る必要がありそう
- Spotifyの整理不足がSerato側の検索性へ直接影響する
- Seratoのライブラリ管理問題とも関連

## 関連する課題

- [お気に入りの曲が一時受け皿として肥大化する](../library/2026-05-08-spotify-liked-songs-as-intake-overload.md)
- [お気に入りから用途別リストへ分ける作業が大変](../playlist/2026-05-08-spotify-playlist-classification-workload.md)
- [曲数が増えるとSeratoライブラリ管理が難しくなる](../../../../serato/problems/personal/library/2026-05-08-serato-large-library-management-difficulty.md)
- [SpotifyプレイリストとSeratoクレートとMixxxプレイリストの対応付けが難しい](../../../../cross-tool/problems/personal/playlist/2026-05-08-playlist-crate-list-mapping-friction.md)
- [PC固有パスとUSBパスとストリーミング参照が混在する](../../../../cross-tool/problems/personal/library/2026-05-08-reference-paths-local-usb-streaming-mixed.md)

## ソース

- 自分のSpotify / Serato運用上の懸念

## 関連リンク

- なし
