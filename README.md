# DJ Workflow Issues

Mixxx、Serato、Spotify、USB を使った DJ ワークフロー上の課題を整理するためのリポジトリ

## 目的

- DJ 準備、選曲、解析、プレイリスト管理、当日の運用で発生する問題点の整理
- Mixxx、Serato、Spotify、USB それぞれの制約や困りごとの記録
- ツール横断で起きるデータ移行、メタデータ、BPM、キー、キュー管理の課題の整理
- 将来的な改善案、代替運用、検証結果の蓄積

## ディレクトリ

```text
docs/
  dj-workflow-issues/
    history.md
issues/
  mixxx/
    README.md
    problems/
      README.md
      personal/
        README.md
        analysis/
        controller/
        library/
        setup/
      external/
        README.md
        analysis/
        controller/
        library/
        rekordbox/
        setup/
  serato/
    README.md
    problems/
      README.md
      personal/
        README.md
        library/
  spotify/
    README.md
    problems/
      README.md
      personal/
        README.md
        automation/
        library/
        metadata/
        playlist/
        serato/
  usb/
    README.md
    problems/
      README.md
      personal/
        README.md
        backup/
        format/
        library/
  cross-tool/
    README.md
    problems/
      README.md
      personal/
        README.md
        automation/
        library/
        metadata/
        playlist/
        workflow/
templates/
  issue-note.md
agents/
  project-context.md
```

## 記録方針

- 1つの問題につき1つの Markdown ファイル
- ファイル名は `YYYY-MM-DD-short-topic.md` を基本形
- ツール固有の問題は `issues/{tool}/problems/` 配下へ配置
- 自分が感じている問題点は `issues/{tool}/problems/personal/` 配下へ配置
- 他の人が感じている問題点は `issues/{tool}/problems/external/` 配下へ配置
- 同じ出どころ内で問題メモが増えた場合は小分類ディレクトリへ配置
- `external/` では、個人製作の外部アプリで補助・変換・検証・可視化できそうな問題を優先
- 複数ツールにまたがる問題は `issues/cross-tool/problems/` 配下へ配置
- ツール固有の問題と横断問題が関連する場合は、双方の `関連する課題` に相互リンクを追加
- 再現条件、困っている影響、期待する状態、現時点の回避策を優先して記録

## 運用ルール

- 問題点は1件ごとに個別の Markdown ファイルとして記録
- 自分の体験や考えにもとづく問題点は `personal/` 配下へ配置
- 他のユーザーの意見、記事、レビュー、会話などから見つけた問題点は `external/` 配下へ配置
- `personal/` と `external/` の中で、必要に応じて `library/`、`analysis/`、`playlist/`、`metadata/` などのカテゴリに分ける運用
- ツール固有の制約や操作性は各ツール配下へ配置
- ツール間の対応付け、共有、差分、工程分断は `cross-tool/` 配下へ配置
- 他者由来の問題点を記録する場合は、出典や観測元を `ソース`、`関連リンク`、`調査メモ` に記録
- `ソース` には確認元のリンク先を Markdown リンクで記載
- 個人製作の外部アプリで解決・補助できなさそうな問題は、通常の問題メモとしては追加せず、除外リストとしても管理しない
- 1つの変更が他の箇所にも影響しそうな場合は、関連する README、運用メモ、履歴、相互リンクも同時に更新
- 正式な問題メモにする前の下書きや agent 作業メモは `agents/` 配下で管理
- カテゴリを追加した場合は、対象ツールの README と `problems/README.md`、`personal/README.md` を更新
- リンクを追加・移動した場合は、相対リンク切れを確認

## 主な観点

- 楽曲管理
- プレイリスト管理
- クレート管理
- BPM / キー / ビートグリッド
- キュー / ループ / ホットキュー
- 音源ファイルとストリーミング音源の扱い
- エクスポート / インポート
- USB メモリ / 外部ストレージ管理
- ローカル音源とストリーミング楽曲の対応付け
- 外部アプリや API で補助できる範囲
- 本番環境での安定性
- 準備時間や操作負荷

## 使い方

1. `templates/issue-note.md` をコピー
2. 対象ツールの `issues/{tool}/problems/personal/` または `issues/{tool}/problems/external/` 配下へ配置
3. `出どころ` に `personal` または `external` を記録
4. 実際に困った状況、期待する状態、検証結果を記録
5. 外部情報を根拠にする場合は `ソース` に確認元リンクを記録
6. 複数ツールにまたがる場合は `issues/cross-tool/problems/` に横断課題を作成
7. 関連するツール固有課題と横断課題を相互リンク
8. 必要に応じて `docs/dj-workflow-issues/history.md` に要約を追記
