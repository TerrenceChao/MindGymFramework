# MindGymFramework

這個資料夾現在是純靜態網站，可以直接用 GitHub Pages 發布，不需要本地 server、npm、build step。

入口頁：

- 本機瀏覽：打開 `index.html`
- GitHub Pages：發布後打開 GitHub Pages 顯示的網址

## 目前保留的內容

```text
index.html        網站首頁
assets/site.css   共用樣式
v1/               既有 MindGym 專案的架構、流程圖、wireframe
v2/               未來重構設計，現在本機留空
.nojekyll         讓 GitHub Pages 原樣提供靜態檔
README.md         這份發布與分享說明
```

V1 的資料結構入口：

- `v1/data/index.html`：資料結構總覽
- `v1/data/database-schema.html`：34 張 public 資料表的 schema 字典
- `v1/data/cache-structure.html`：瀏覽器、本機與 process 暫存資料

注意：Git 不會追蹤空資料夾，所以 `v2/` 如果完全空白，推到 GitHub 後不會出現在 repository。等要開始設計 v2 時，放入第一個 `index.html` 或文件即可。

## 推到 GitHub

在這個資料夾執行：

```bash
cd /Users/chaoalbert/Projects/playground/local-storage/MindGymFramework
git status
git add .
git commit -m "Publish MindGym framework static site"
git branch -M main
git remote add origin https://github.com/<你的帳號>/<你的 repo>.git
git push -u origin main
```

如果你已經設定過 remote，就不要再跑 `git remote add origin ...`，改用：

```bash
git remote -v
git push -u origin main
```

## 開啟 GitHub Pages

到 GitHub repository 頁面：

1. 進入 `Settings`
2. 左側選 `Pages`
3. `Build and deployment` 選 `Deploy from a branch`
4. `Branch` 選 `main`
5. Folder 選 `/ (root)`
6. 按 `Save`

GitHub 會顯示一個網址，通常長這樣：

```text
https://<你的帳號>.github.io/<你的 repo>/
```

部署完成後，把這個網址傳給朋友即可。他們用瀏覽器打開就能看，不需要你另外傳 `.md` 或啟動任何 server。
