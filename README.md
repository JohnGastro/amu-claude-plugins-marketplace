# Amu Claude Plugins Marketplace

Amu社内向け Claude / Cowork プラグイン配布用ディレクトリです。

## 重要

このリポジトリは **private repo として運用**してください。

`amu-temairazu-manual` はTEMAIRAZU（手間いらず）のログイン後マニュアル本文を参照資料として含みます。社内利用のための配布物であり、public repo、社外共有、外部公開ページには置かないでください。

## 含まれるプラグイン

- `amu-temairazu-manual`
  - TEMAIRAZU（手間いらず）Webマニュアルを根拠に、在庫・料金・予約・予約サイト設定などの操作質問へ回答します。

## インストール

```sh
claude plugin marketplace add <このリポジトリのURL>
claude plugin install amu-temairazu-manual@amu-claude-plugins
```

Claude Code / Cowork を再起動後、以下のように質問できます。

```text
手間いらずで在庫を売止めする方法を教えて
/temairazu 予約キャンセルの確認方法
```

## ローカルで試す場合

```sh
claude plugin marketplace add /path/to/amu-claude-plugins-marketplace
claude plugin install amu-temairazu-manual@amu-claude-plugins
```

## ドキュメント

- [社員向けインストール手順](./INSTALL.md)
- [使い方マニュアル](./USAGE.md)
- [運用・更新手順](./MAINTENANCE.md)
- [取り扱い注意](./SECURITY.md)

## 検証

```sh
claude plugin validate .
```
