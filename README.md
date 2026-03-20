# TVBox GitHub Pages 配置

## 文件說明

- `tvbox.json` - TVBox 主配置文件
- `api.json` - 分類接口數據
- `list.json` - 影片列表數據

## 快速開始

### 1. 創建 GitHub 倉庫

1. 訪問 https://github.com/new
2. 倉庫名稱：`tvbox-config`（或你喜歡的名字）
3. 選擇 **Public**（公開）
4. 點擊 **Create repository**

### 2. 上傳文件

#### 方法 A：網頁上傳（簡單）

1. 打開你的 GitHub 倉庫頁面
2. 點擊 **Add file** → **Upload files**
3. 將這個文件夾中的 3 個 JSON 文件拖放到網頁
4. 點擊 **Commit changes**

#### 方法 B：命令行上傳

```bash
# 進入這個文件夾
cd /Users/andyau/Documents/trae_projects/miss/api-system/tvbox-server/github-pages

# 初始化 git
git init
git add .
git commit -m "Initial TVBox config"

# 連接到你的 GitHub 倉庫（替換 你的用戶名）
git remote add origin https://github.com/你的用戶名/tvbox-config.git
git branch -M main
git push -u origin main
```

### 3. 啟用 GitHub Pages

1. 在 GitHub 倉庫頁面，點擊 **Settings**
2. 左側選擇 **Pages**
3. **Source** 選擇 **Deploy from a branch**
4. **Branch** 選擇 **main**，文件夾選擇 **/(root)**
5. 點擊 **Save**

等待 1-2 分鐘，你的網站就會上線。

### 4. 獲取配置 URL

你的 TVBox 配置 URL 將是：
```
https://你的用戶名.github.io/tvbox-config/tvbox.json
```

例如：
```
https://john.github.io/tvbox-config/tvbox.json
```

### 5. 在 TVBox 中使用

1. 打開 TVBox 應用
2. 進入 **設置** → **配置地址**
3. 輸入你的配置 URL
4. 點擊 **確認**
5. 返回主頁，選擇 **MissAV影視** 數據源

## 更新影片

當你想更新影片時：

1. 更新 `list.json` 文件
2. 重新上傳到 GitHub
3. GitHub Pages 會自動更新（可能需要幾分鐘）

## 注意事項

- 倉庫必須是 **Public** 才能使用 GitHub Pages
- 首次部署可能需要 1-2 分鐘
- 如果配置無法加載，檢查 URL 是否正確
- 確保文件名沒有拼寫錯誤

## 故障排除

**問題：無法訪問配置**
- 檢查 GitHub Pages 是否已啟用（Settings → Pages）
- 確認 URL 格式正確
- 等待 1-2 分鐘後重試

**問題：影片無法播放**
- 檢查 m3u8 鏈接是否有效
- 確認電視有網絡連接
