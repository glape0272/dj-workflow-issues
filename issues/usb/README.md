# USB

USB メモリや外部ストレージを使った DJ ワークフロー上の課題置き場

## 記録対象

- USB メモリの構成
- 音源ファイルの配置
- フォルダ構成
- バックアップ
- 複数 USB の同期
- ファイル名 / 文字コード / パス長
- 本番環境での読み込み安定性
- 紛失、破損、容量不足への対策

## ディレクトリ

```text
problems/
  personal/
    library/
    format/
    backup/
```

## 問題メモ

USB 固有の音源配置、フォーマット、バックアップ問題はこの配下に記録し、Mixxx、Serato、Spotify との対応付けや共有問題は [Cross Tool](../cross-tool/) 側にも横断課題として記録

### ライブラリ

- [USBディレクトリ管理が複雑化する](./problems/personal/library/2026-05-08-usb-directory-management-complexity.md)
- [USB内で同じ曲が複数箇所に配置される](./problems/personal/library/2026-05-08-usb-duplicate-track-placement.md)
- [DJソフトごとに扱いやすいディレクトリ構造が異なる](./problems/personal/library/2026-05-08-usb-directory-structure-cross-tool-gap.md)
- [USB内に低使用頻度曲が残り続ける](./problems/personal/library/2026-05-08-usb-low-use-tracks-accumulate.md)

### フォーマット

- [MP3とWAVなどのフォーマット混在で管理が複雑化する](./problems/personal/format/2026-05-08-usb-audio-format-mixing.md)
- [ファイル名とタグ情報が一致しない](./problems/personal/format/2026-05-08-usb-filename-tag-mismatch.md)

### バックアップ

- [USBとマスター音源フォルダの差分確認が難しい](./problems/personal/backup/2026-05-08-usb-master-library-diff.md)
