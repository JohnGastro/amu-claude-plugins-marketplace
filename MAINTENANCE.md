# 運用・更新手順

TEMAIRAZUマニュアルを再取得した場合の更新手順です。

## ディレクトリ構成

```text
amu-claude-plugins-marketplace/
├── .claude-plugin/
│   └── marketplace.json
├── plugins/
│   └── amu-temairazu-manual/
│       ├── .claude-plugin/
│       │   └── plugin.json
│       ├── README.md
│       └── skills/
│           ├── temairazu/
│           │   └── SKILL.md
│           └── temairazu-manual/
│               ├── SKILL.md
│               └── references/
│                   ├── index.md
│                   ├── 手間いらずマニュアル_全文.md
│                   ├── images_manifest.json
│                   └── pages/
└── README.md
```

## 更新対象

通常更新するのは以下だけです。

- `plugins/amu-temairazu-manual/skills/temairazu-manual/references/index.md`
- `plugins/amu-temairazu-manual/skills/temairazu-manual/references/手間いらずマニュアル_全文.md`
- `plugins/amu-temairazu-manual/skills/temairazu-manual/references/images_manifest.json`
- `plugins/amu-temairazu-manual/skills/temairazu-manual/references/pages/`

## バージョンを上げる

マニュアル本文を更新したら、以下の両方の `version` を上げます。

- `plugins/amu-temairazu-manual/.claude-plugin/plugin.json`
- `plugins/amu-temairazu-manual/skills/temairazu-manual/SKILL.md`

例:

```text
0.1.0 -> 0.1.1
```

## 検証

更新後に以下を実行します。

```sh
claude plugin validate .
```

インストール済み環境で確認する場合:

```sh
claude plugin update amu-temairazu-manual
```

反映されない場合は Claude Code / Cowork を再起動してください。

## GitHubへ反映

```sh
git status
git add .
git commit -m "Update TEMAIRAZU manual plugin"
git push
```
