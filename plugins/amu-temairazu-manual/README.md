# Amu TEMAIRAZU Manual Plugin

Claude / Cowork 用のTEMAIRAZU（手間いらず）操作マニュアルプラグインです。

TEMAIRAZU（手間いらず）Webマニュアルを参照し、在庫、料金、予約、部屋タイプ、プラン、予約サイト連携などの操作質問に答えます。

## 含まれるもの

- `skills/temairazu-manual/SKILL.md`
  - Claude が手間いらず操作質問を受けたときの参照ルール
- `skills/temairazu-manual/references/index.md`
  - 全377ページの目次
- `skills/temairazu-manual/references/pages/`
  - ページ別 Markdown
- `skills/temairazu-manual/references/手間いらずマニュアル_全文.md`
  - 全文検索用 Markdown
- `skills/temairazu-manual/references/images_manifest.json`
  - 画像ファイル名と元URLの対応表

画像ファイル自体は同梱していません。Markdown内の画像リンクは公開URLへ差し替え済みです。

## 使い方

Claude / Cowork にこのプラグインを入れたうえで、普通に質問してください。

例:

- `手間いらずで在庫を売止めする方法を教えて`
- `料金ランクの設定方法は？`
- `予約サイトの部屋タイプ紐付けを確認したい`
- `/temairazu 予約キャンセルの確認方法`

## 注意

- 回答時はマニュアル内の該当ページ名を示す運用にしています。
- 施設アカウントやログイン情報は含みません。
