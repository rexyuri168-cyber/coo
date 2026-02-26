# Chloe 作品集 — 部署說明

## 📁 資料夾結構
```
chloe-site/
├── index.html        ← 作品集網站
├── netlify.toml      ← Netlify 設定
├── admin/
│   ├── index.html    ← CMS 後台入口
│   └── config.yml    ← CMS 設定
└── images/           ← 上傳的圖片會存在這裡
```

---

## 🚀 部署步驟（第一次）

### 1. 建立 GitHub 帳號
前往 https://github.com 註冊（免費）

### 2. 建立新 Repository
- 點右上角 `+` → `New repository`
- 名稱填 `chloe-portfolio`
- 選 `Public`
- 按 `Create repository`

### 3. 上傳檔案
- 在新建的 repo 頁面，點 `uploading an existing file`
- 把整個 `chloe-site` 資料夾裡的所有檔案拖曳上去
- 按 `Commit changes`

### 4. 連結 Netlify
- 前往 https://netlify.com 登入（可用 GitHub 帳號）
- 點 `Add new site` → `Import an existing project`
- 選 `GitHub` → 選你的 `chloe-portfolio` repo
- Build settings 保持預設，直接按 `Deploy site`

### 5. 開啟 Git Gateway（後台必要設定）
- 在 Netlify 後台：`Site settings` → `Identity` → `Enable Identity`
- 往下找 `Git Gateway` → `Enable Git Gateway`
- 再到 `Identity` → `Registration` → 改成 `Invite only`

### 6. 邀請自己成為管理員
- `Identity` → `Invite users` → 輸入你的 email
- 收信後點連結設定密碼

---

## 🎛️ 使用後台

部署完成後，前往：
```
https://你的網址.netlify.app/admin
```
輸入 email 和密碼就能登入後台，新增/編輯/刪除作品！

---

## ❓ 常見問題

**後台登入後看到空白？**
確認 `admin/config.yml` 已正確上傳到 GitHub。

**圖片上傳失敗？**
確認 Git Gateway 已啟用。
