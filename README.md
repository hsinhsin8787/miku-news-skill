# Miku News Skill

台灣繁體中文新聞稿撰寫 Skill，適用於 ChatGPT 與 Codex 團隊工作流程。

## 功能

- 新聞稿撰寫、改寫與結構分析
- 專家觀點、課程／書籍／品牌發布
- 活動預熱與活動回顧
- 公益、ESG 與季節型實用指南
- 固定提供 3 個新聞標題選項
- 對數據、人物、引言與高風險主張進行查核提醒

## 團隊安裝

### 使用 GitHub CLI（建議）

先確認團隊成員已取得此 private repository 的讀取權限，並安裝及登入 GitHub CLI。

```bash
gh auth login
gh skill install hsinhsin8787/miku-news-skill miku-news --agent codex --scope user
```

安裝完成後，重新啟動 Codex。使用時輸入：

```text
$miku-news 請根據這份資料撰寫一篇新聞稿
```

### 手動安裝

將 `skills/miku-news` 整個資料夾複製到：

```text
~/.agents/skills/miku-news
```

不可只複製 `SKILL.md`；必須保留 `references/` 與 `agents/`。

## 更新

若使用 GitHub CLI 安裝：

```bash
gh skill update --all
```

## Repository 結構

```text
skills/
└── miku-news/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    └── references/
        └── structures.md
```

## 使用提醒

- 缺少重要事實時，Skill 會使用 `[待確認]`，不會自行虛構。
- 法律、醫療、金融、投資、政策與績效主張仍需人工複核。
- 個案、照片與引言須確認已取得公開使用授權。

## 權限

Internal use only. 僅供已獲 repository 存取權的團隊成員使用。
