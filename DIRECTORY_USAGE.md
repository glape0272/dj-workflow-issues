# ディレクトリ運用メモ

このプロジェクトで使用する各ディレクトリの役割と記録方針

## `docs/`

作業管理と履歴の置き場

- プロジェクト全体の履歴
- 作業単位の進捗メモ
- 後から見返すための変更要約
- 実際の問題メモではなく、整理作業そのものの記録

## `issues/`

DJ ワークフロー上の問題点を分類して記録する置き場

- `mixxx/`: Mixxx 固有の問題
- `serato/`: Serato 固有の問題
- `spotify/`: Spotify 固有の問題
- `usb/`: USB メモリや外部ストレージ管理の問題
- `cross-tool/`: 複数ツールにまたがる連携、共有、対応付け、工程分断の問題

1つの問題につき1つの Markdown ファイルを作成する方針

各ツール配下では `problems/` に問題メモを集約する方針

`problems/` 配下は、出どころ別に `personal/` と `external/` を分け、その下で `library/` や `analysis/` などの小分類ディレクトリを作成して整理する方針

ツール固有の制約や操作性は各ツール配下へ配置する方針

ツール間の対応付け、ライブラリ共有、メタデータ差分、ワークフロー分断は `cross-tool/problems/` 配下へ配置する方針

### 問題メモの運用

- 問題点は1件ごとに個別の Markdown ファイルとして記録
- 自分の体験や考えにもとづく問題点は `personal/` 配下へ配置
- 他のユーザーの意見、記事、レビュー、会話などから見つけた問題点は `external/` 配下へ配置
- 他者由来の問題点を記録する場合は、出典や観測元を `ソース`、`関連リンク`、`調査メモ` に記録
- `ソース` には確認元のリンク先を Markdown リンクで記載
- 個人製作の外部アプリで解決・補助できなさそうな問題は、問題メモとして追加せず、除外リストとしても管理しない
- `personal/` と `external/` の中で、必要に応じて `library/`、`analysis/` などのカテゴリに分ける運用
- 1つの変更が他の箇所にも影響しそうな場合は、関連する README、運用メモ、履歴、相互リンクも同時に更新
- ツール固有問題と横断問題が関連する場合は、双方の `関連する問題` に他の Markdown への相対リンクを追加
- `関連する問題` はリポジトリ内の問題メモ同士のリンク用
- `関連リンク` は外部URLや参考資料用
- カテゴリを追加した場合は、対象ツールの README、`problems/README.md`、`personal/README.md` を更新
- リンクを追加・移動した場合は、相対リンク切れを確認

現在の主な構成:

```text
issues/
  mixxx/
    problems/
      personal/
        analysis/
        controller/
        library/
        setup/
      external/
        analysis/
        controller/
        library/
        rekordbox/
        setup/
  serato/
    problems/
      personal/
        library/
  spotify/
    problems/
      personal/
        automation/
        library/
        metadata/
        playlist/
        serato/
  usb/
    problems/
      personal/
        backup/
        format/
        library/
  cross-tool/
    problems/
      personal/
        automation/
        library/
        metadata/
        playlist/
        workflow/
```

## `templates/`

問題メモのひな形を置く場所

- 新しい問題メモを作るときのコピー元
- 記録項目の統一
- 書き漏れ防止のための補助
- `出どころ`、`ソース`、外部アプリで対応できそうな範囲を記録するための基準

## `agents/`

AI agent やローカル作業用の一時ファイル置き場

- Codex などの agent 作業メモ
- 一時的な調査結果
- まだ正式な issue として整理していない下書き
- Git 管理しないローカル専用領域

正式に残す内容は `issues/` または `docs/` へ移動する方針

## トップ階層

プロジェクト全体の入口となるファイルを置く場所

- `README.md`: プロジェクト概要と基本的な使い方
- `DIRECTORY_USAGE.md`: ディレクトリごとの運用メモ
- `.gitignore`: Git 管理しないファイルやディレクトリの指定

個別の問題メモはトップ階層に置かず、原則 `issues/` 配下へ配置
