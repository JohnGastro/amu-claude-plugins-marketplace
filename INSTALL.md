# 社員向けインストール手順

AmuのClaude / Coworkで、TEMAIRAZU（手間いらず）操作マニュアルを使えるようにする手順です。

## 前提

- Claude Code または Cowork が使えること
- Amu社内GitHub上のこのprivate repoにアクセスできること
- Claudeのアカウントが社内利用アカウントであること

## 1. Marketplaceを追加する

ターミナルで以下を実行します。

```sh
claude plugin marketplace add <このリポジトリのURL>
```

例:

```sh
claude plugin marketplace add https://github.com/<org-or-user>/amu-claude-plugins-marketplace
```

## 2. プラグインをインストールする

```sh
claude plugin install amu-temairazu-manual@amu-claude-plugins
```

## 3. Claude / Coworkを再起動する

インストール後、Claude Code / Coworkを一度再起動してください。

## 4. 動作確認する

以下のように質問します。

```text
手間いらずで在庫を売止めする方法を教えて
```

または:

```text
/temairazu 予約キャンセルの確認方法
```

マニュアルの該当ページを根拠にした手順が返ってくれば完了です。

## うまくいかない場合

### marketplace addで失敗する

- GitHub repoへのアクセス権があるか確認してください。
- GitHubにログインしているか確認してください。
- repo URLがprivate repoのURLになっているか確認してください。

### plugin installで見つからない

Marketplace名は `amu-claude-plugins` です。

```sh
claude plugin marketplace list
```

で追加済みか確認してください。

### 反映されない

Claude Code / Coworkを再起動してください。
