---
title: "git"
date: 2025-10-11
draft: false
categories: ["版本控制", "技術", "程式設計"]
tags: ["git", "github", "branch", "版本控制", "指令"]
---
# Git

### 使用者資料
```
git config --global user.name "name"
git config --global user.email "name@email.com"
```
***

文件狀態 :
 `git status` (檢查)
 `git add .` (追蹤)
 `git commit -m "備註"` (暫存)
***
GITHUB:
 `git push` (上傳github)
 `git clone  URL` (install the url file)
 `git pull` (同步)
 `git pull --rebase`（把遠端的檔案拉到自己的本地，把本地最新的資料放到最前面）
***
 `git checkout -b name` (add 分支) 
 `git push Name` 分支name
***
`git log` (日誌)
`git log  --oneline`(日誌line)
`git diff ID` (比較)
`git checkout ID -- file_name` （應用）
***
***
***
(覆盖main分支)
checkout main
git reset --hard origin/${branchName}
git push -f

重點整理
分支（branch）以個人開發來看，是為了解決開發新功能途中遇上緊急修正的情況，我們透過分支可以將「開發新功能」、「修正」分開成兩條線，在開發新功能的同時，可以修正穩定版本的 bug。

開啟新的分支： `git branch ${branchName}`
確認目前所在分支： `git branch -v`
切換分支： `git checkout ${branchName}`
刪除分支： 
```
git branch -d ${branchName}
git push origin --d ${branchName} 
```

合併分支： $ git merge ${被合併分支 branchName}
假設在合併時發生衝突，必須開啟檔案手動解決衝突，重新 $ git add 並 $ git commit ，git 會新增一個版本。
***
這個指令會把目前的 HEAD 移到指定的 commit 上，並且把目前的狀態變成當時 commit 的樣子，但是不會移動任何分支（也就是分支都停在原來的地方，只有 HEAD 移動而已）。
因此，整個歷史紀錄看起來並沒有什麼變化，只是 HEAD 暫時移到某個地方而已。

$ git checkout HEAD~1 # 數字表示移動到 HEAD後面第幾個

如果想在這個版本修改資料，可以建立新的分支，修改完後再 merge 回主線。

`git checkout -b ${新分支名稱}`
