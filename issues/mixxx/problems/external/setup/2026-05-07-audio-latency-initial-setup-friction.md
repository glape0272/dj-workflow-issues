# オーディオ設定・レイテンシ・初期導入のつまずき

## 概要

- 対象ツール: Mixxx
- 発生日: 2026-05-07
- 優先度: 中
- 状態: 外部情報から整理

## 困っていること

音割れ、Bluetooth 遅延、ヘッドホン試聴できない、Linux の PulseAudio / ALSA、Windows の ASIO など、初期導入時に確認すべき項目が多い

Mixxx を初めて使う人が、音を出すまでの設定で詰まりやすい状態

## 再現条件

- 初回起動後にオーディオ出力を設定
- Bluetooth スピーカーや一般的な PC 内蔵音源を使用
- ヘッドホン試聴を使いたい場合
- Linux、Windows、macOS で音声 API やドライバ設定が必要な場合

## 期待する状態

- 利用環境に応じた確認項目を順番に確認できる状態
- DJ 用途では避けるべき設定を事前に検出できる状態
- 本番前に音声出力、ヘッドホン、レイテンシをチェックできる状態

## 個人製作アプリで対応できそうな範囲

- 初期設定チェックリストの提供
- OS 別の推奨設定メモ生成
- 接続構成、出力先、ヘッドホン試聴可否の確認項目整理
- 本番前チェックリストの生成
- トラブル症状から公式 Troubleshooting への誘導

## 対応が難しそうな範囲

- OS のドライバ不具合修正
- ASIO、PulseAudio、ALSA、JACK など音声基盤そのものの改善
- Bluetooth 遅延の解消
- Mixxx 本体のオーディオエンジン修正

## 調査メモ

- 公式 Troubleshooting に音割れ、Bluetooth 遅延、Linux の PulseAudio、ヘッドホン試聴、Windows の ASIO などの説明あり

## ソース

- [Mixxx 公式 Wiki / Troubleshooting](https://github.com/mixxxdj/mixxx/wiki/troubleshooting)

## 関連する問題

- [音を出すまでの道のりが長め](../../personal/setup/2026-05-07-first-sound-friction.md)
- [コントローラーマッピング作成と検証の負荷](../controller/2026-05-07-controller-mapping-workflow-burden.md)
- [対応コントローラーが少ない](../../personal/controller/2026-05-07-controller-support.md)

## 関連リンク

- https://github.com/mixxxdj/mixxx/wiki/troubleshooting
