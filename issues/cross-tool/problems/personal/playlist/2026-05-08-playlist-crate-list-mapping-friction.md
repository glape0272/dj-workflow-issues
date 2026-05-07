# SpotifyプレイリストとSeratoクレートとMixxxプレイリストの対応付けが難しい

## 概要

- 対象ツール: Spotify / Serato / Mixxx
- 発生日: 2026-05-08
- 優先度: 中
- 状態: 未調査
- 出どころ: personal

## 困っていること

Spotify ではプレイリスト、Serato ではクレート、Mixxx ではプレイリストやクレート相当の管理単位を使うため、同じ分類意図をそのまま横断利用しにくい

準備段階で作ったリストが、別ツールでは別の概念として扱われ、どれを正とするか迷いやすい状態

## 再現条件

- Spotifyで選曲や分類を行う
- Seratoでクレートを使ってDJ準備を行う
- Mixxxでも同じ分類を使いたい
- 1曲が複数の用途別リストに所属する

## 期待する状態

- Spotifyプレイリスト、Seratoクレート、Mixxxプレイリストの対応関係が分かる状態
- どのツールの分類を正とするか決まっている状態
- ツール間で分類を再作成する負荷が低い状態

## 現時点の回避策

- 各ツールで手動でリストやクレートを作る
- Spotify側でDJ用途別リストを先に整理する
- SeratoやMixxxで必要な分類だけを作り直す

## 個人製作アプリで対応できそうな範囲

- 各ツールの分類単位の対応表作成
- Spotifyプレイリストを基準にしたSerato / Mixxx向け分類案の生成
- リスト所属の差分確認
- 横断分類用の中間リスト生成

## 対応が難しそうな範囲

- 各DJソフト内部の分類仕様差そのものの解消
- DJ中の文脈に応じた最適分類の完全自動判断
- 非公開形式への安全な書き込み

## 調査メモ

- まずはSpotifyを選曲元、Serato / Mixxxを利用先として整理すると扱いやすそう
- 1曲1分類ではなく、複数リスト所属を前提にする必要
- クレートとプレイリストの意味差を整理する必要

## 関連する問題

- [お気に入りから用途別リストへ分ける作業が大変](../../../../spotify/problems/personal/playlist/2026-05-08-spotify-playlist-classification-workload.md)
- [ディレクトリとクレートの設計思想がMixxxと異なる](../../../../serato/problems/personal/library/2026-05-08-serato-directory-playlist-crate-concept-gap.md)
- [ライブラリ操作と検索性に課題](../../../../mixxx/problems/personal/library/2026-05-07-library-operation-friction.md)
- [ディレクトリ分類とプレイリスト分類が二重化する](./2026-05-08-directory-and-playlist-classification-duplication.md)
- [Spotifyのリスト依存でSerato上の曲探しが大変](../../../../spotify/problems/personal/serato/2026-05-08-serato-spotify-list-dependent-search-friction.md)
- [発見からDJソフト登録までの準備工程が分断される](../workflow/2026-05-08-discovery-to-dj-prep-workflow-fragmented.md)

## ソース

- 自分のDJワークフロー上の懸念

## 関連リンク

- なし
