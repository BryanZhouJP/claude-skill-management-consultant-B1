# インストールガイド — MBB経営コンサルタントスキル

このガイドでは、Claudeを中心に本スキルを導入する方法を説明します。
最短導入は **Claude Codeプラグイン方式** です。

> 英語原文: [INSTALL.md](./INSTALL.md)

---

## 方法0: Claude Codeプラグイン（最短）

```bash
/plugin marketplace add DogInfantry/claude-skill-management-consultant-B1
/plugin install management-consultant
```

アップデート時:

```bash
/plugin marketplace update
```

---

## 方法1: Claude Cowork（デスクトップ）推奨

1. このリポジトリをZIPでダウンロードして展開  
2. ワークスペース配下に `.claude/skills/management-consultant/` を作成  
3. `skill/` の中身を上記フォルダへコピー  
4. Claude Coworkを再起動  

期待ディレクトリ:

```text
Your Workspace/
└── .claude/
    └── skills/
        └── management-consultant/
            ├── SKILL.md
            └── references/
```

---

## 方法2: Claude Code（CLI）

```bash
git clone https://github.com/DogInfantry/claude-skill-management-consultant-B1.git
mkdir -p ~/.claude/skills/
cp -r claude-skill-management-consultant-B1/skill/ ~/.claude/skills/management-consultant/
```

確認:

```bash
ls ~/.claude/skills/management-consultant/
# SKILL.md と references/ が見えること
```

---

## 方法3: 手動貼り付け（お試し）

`skill/SKILL.md` の内容を会話の最初に貼り付けて利用できます。  
ただし深掘り分析には `skill/references/` の関連ファイルも併用してください。

---

## 方法4: 他エージェント（Codex/Gemini/Copilot/Cursor/Ollama）

- **Codex/Cursor/Windsurf/Amp/Cline**: `AGENTS.md` 経由で読み込み
- **Gemini CLI**: `GEMINI.md` 経由で読み込み
- **GitHub Copilot**: `.github/copilot-instructions.md` 経由で読み込み
- **Ollama**: `Modelfile` を利用

```bash
ollama create management-consultant -f Modelfile
ollama run management-consultant
```

---

## 動作確認チェック

以下を満たせば概ね正常です:

- 結論先出し（Pyramid Principle）
- MECE構造での分解
- 仮説主導の言い回し
- 数字・レンジを用いた定量化
- 追加質問の質（文脈・制約・目的の確認）

---

## 関連ドキュメント

- 概要: [README_JP.md](./README_JP.md)
- フレームワーク: [FRAMEWORKS_JP.md](./FRAMEWORKS_JP.md)
- ケース集: [CASE-STUDIES_JP.md](./CASE-STUDIES_JP.md)
- 評価: [EVALS_JP.md](./EVALS_JP.md)
- 貢献: [CONTRIBUTING_JP.md](./CONTRIBUTING_JP.md)
