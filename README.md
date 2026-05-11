# DJ Workflow Issues

Mixxx、Serato、Spotify、USB を使った DJ ワークフロー上の課題を整理するためのリポジトリ

## 目的

- DJ 準備、選曲、解析、プレイリスト管理、当日の運用で発生する問題点の整理
- Mixxx、Serato、Spotify、USB それぞれの制約や困りごとの記録
- ツール横断で起きるデータ移行、メタデータ、BPM、キー、キュー管理の課題の整理
- 将来的な改善案、代替運用、検証結果の蓄積

## 何を記録するか

- 実際に困ったこと
- 期待する状態
- 再現条件や発生条件
- 現時点の回避策
- 検証した結果
- 関連する外部情報や参考リンク

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

## ディレクトリ

```text
issues/
  mixxx/
  serato/
  spotify/
  usb/
  cross-tool/
templates/
  issue-note.md
docs/
  dj-workflow-issues/
    history.md
```

- `issues/`: DJ ワークフロー上の問題点
- `issues/mixxx/`: Mixxx 固有の問題
- `issues/serato/`: Serato 固有の問題
- `issues/spotify/`: Spotify 固有の問題
- `issues/usb/`: USB メモリや外部ストレージ管理の問題
- `issues/cross-tool/`: 複数ツールにまたがる問題
- `templates/`: 問題メモのひな形
- `docs/`: 作業履歴や整理作業の記録

詳しいディレクトリ運用は [DIRECTORY_USAGE.md](DIRECTORY_USAGE.md) を参照

## 使い方

1. [templates/issue-note.md](templates/issue-note.md) をもとに問題メモを作成
2. 対象ツールの `issues/{tool}/problems/` 配下へ配置
3. 自分の体験にもとづく内容は `personal/` へ配置
4. 他者の意見、記事、レビュー、会話などから見つけた内容は `external/` へ配置
5. 複数ツールにまたがる内容は `issues/cross-tool/problems/` へ配置

## 関連ファイル

- [DIRECTORY_USAGE.md](DIRECTORY_USAGE.md): ディレクトリごとの運用メモ
- [templates/issue-note.md](templates/issue-note.md): 問題メモのひな形
