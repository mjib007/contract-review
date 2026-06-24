# 📋 AI 契約條款自動審查教學

![Profile views](https://komarev.com/ghpvc/?username=mjib007&label=Profile%20views&color=4c8eda&style=flat)
[![Stars](https://img.shields.io/github/stars/mjib007/contract-review?style=flat&color=yellow)](https://github.com/mjib007/contract-review/stargazers)
[![Forks](https://img.shields.io/github/forks/mjib007/contract-review?style=flat&color=blue)](https://github.com/mjib007/contract-review/network/members)
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-orange)
![AI](https://img.shields.io/badge/AI-Gemini%20%7C%20GPT%20%7C%20Claude-green)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)
![Status](https://img.shields.io/badge/status-active-success)

> 用大語言模型（Gemini / GPT / Claude）幫 B 公司法務部門自動審查契約條款，產出分析報告。

![AI契約審查五步驟](https://github.com/mjib007/contract-review/blob/main/contract.png?raw=true)

---

## 🚀 快速開始（點一下，直接執行）

**不需要安裝任何軟體，不需要下載任何檔案。** 點下方按鈕，瀏覽器直接開啟，就可以執行。

| 版本 | 說明 | 開啟 |
|------|------|------|
| 📘 教材版 | 有完整步驟說明，支援 Gemini / GPT / Claude 三選一 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjib007/contract-review/blob/main/contract_review_colab.ipynb) |

---

## ❓ Open in Colab 是什麼？

點擊按鈕後，程式碼會在**你自己的 Google 帳號**下開啟並執行：

- 程式在你自己的 Colab 環境跑，不影響任何人
- 執行結果只有你看得到
- 關閉視窗後，執行結果不會保留（但你可以下載報告）

> ⚠️ 需要登入 Google 帳號才能使用 Colab（免費）

---

## 🤖 支援的 AI 模型（三選一）

| 模型 | 費用 | 推薦對象 | 申請網址 |
|------|------|---------|---------|
| 🟢 **Gemini**（Google） | ✅ 有免費額度，每天1,500次 | ⭐ 學生首選 | https://aistudio.google.com/ |
| 🟡 **GPT**（OpenAI） | 新帳號有試用金 | 一般使用者 | https://platform.openai.com/ |
| 🔵 **Claude**（Anthropic） | 需付費 | 進階使用者 | https://console.anthropic.com/ |

> 💡 **學生推薦使用 Gemini**，用 Google 帳號登入即可，完全免費！

---

## 📂 教學情境說明

| 角色 | 說明 |
|------|------|
| **A 公司**（甲方） | 提供契約範本的委託方 |
| **B 公司**（乙方） | 法務部門需要審查契約的受託方 |

**B 公司法務部門的 5 條審查規則：**

| 編號 | 審查重點 | 說明 |
|------|---------|------|
| 規則1 | 付款條件公平性 | 頭期款比例是否超過30%？付款期限是否合理？ |
| 規則2 | 違約金是否過重 | 逾期違約金比例是否超過千分之5？ |
| 規則3 | 保密期間合理性 | 保密義務期間是否超過5年？ |
| 規則4 | 智慧財產權歸屬 | 是否有一方完全壟斷所有IP權利？ |
| 規則5 | 終止條款平衡性 | 是否只有單方（甲方）才能終止契約？ |

---

## 🔄 執行流程

```
Step 2：下拉選單選擇 AI 模型 → 輸入框貼上金鑰（輸入內容隱藏）
                      ↓
Step 3：自動偵測目前開啟的 GitHub repo → 產生正確的資料來源網址
                      ↓
Step 4：自動下載 party_data.json + contract_template.txt
                      ↓
Step 5：自動填充 → 產生完整契約文字
                      ↓
Step 7：呼叫選定的 AI，依照 5 條規則逐一審查
                      ↓
Step 8：輸出審查分析報告（可下載）
```

---

## 🍴 Fork 說明

想要**修改資料做練習**的同學，可以 fork 這個 repo：

### Fork 步驟
1. 點右上角「**Fork**」按鈕，複製一份到你自己的 GitHub 帳號
2. 在你自己的 repo 中，點選 `party_data.json` → 點鉛筆圖示編輯
3. 修改裡面的資料（例如把違約金比例改成 `"8"`）→「Commit changes」
4. 回到你自己的 repo 首頁，點選 `contract_review_colab.ipynb` 檔案
5. 點右上角的「**Open in Colab**」開啟

### ✅ 資料來源自動切換
程式內建**自動偵測功能**：
- 從**老師的 repo** 開啟 → 自動抓老師的資料
- 從**你 fork 的 repo** 開啟 → 自動抓你修改後的資料

**不需要改任何程式碼**，Colab 開啟時會自動判斷。

> ⚠️ 注意：fork 後請從你自己 repo 裡的 `.ipynb` 檔案點「Open in Colab」，  
> 不要點 README 上的按鈕（那個會連到老師的版本）。

---

## 📁 本 Repo 的檔案說明

| 檔案 | 用途 |
|------|------|
| `contract_review_colab.ipynb` | 主教材（支援三個 AI 模型，含自動偵測 repo） |
| `contract_template.txt` | 技術服務契約範本（含佔位符） |
| `party_data.json` | 當事人資料（**fork 後可直接修改此檔做練習**） |
| `README.md` | 本說明文件 |

---

## 🎓 延伸練習

| 練習 | 建議方式 | 內容 |
|------|---------|------|
| 練習一 | 直接在 Colab 操作 | 分別用三個 AI 模型審查同一份契約，比較結果差異 |
| 練習二 | 直接在 Colab 操作 | 在 Step 6 新增第六條審查規則（爭議解決機制） |
| 練習三 | **Fork 後修改 JSON** | 修改 `party_data.json` 的違約金比例，觀察審查結果變化 |

---

## 📜 授權

本教材供教學使用，歡迎自由修改與分享。
