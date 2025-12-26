---
title: "Git & Github"
---

## Git

1. 使用者資料(只需在下載 git 後運行一次)
   ```
   git config --global user.name "name"
   git config --global user.email "name@email.com"
   ```

---

2. 文件狀態 :  
   `git status` (檢查)  
   `git add .` (追蹤)  
   `git commit -m "備註"` (暫存)

---

3. Branch:  
    `git checkout -b { branchName }` (add 分支)  
    `git push { branchName }`(推送 branch)  
   ` git merge { 被合併分支 branchName }`(merge branch)

---

4. other:  
   `git log` (日誌)  
   `git log  --oneline`(日誌 line)  
   `git diff ID` (比較)  
   `git checkout ID -- file_name` （應用）

---

## GITHUB

`git push` (上傳 github)  
 `git clone  URL` (fork the repo)  
 `git pull` (同步)  
 `git pull --rebase`（把遠端的檔案拉到自己的本地，把本地最新的資料放到最前面）

---
