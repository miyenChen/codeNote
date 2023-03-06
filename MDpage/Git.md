# Git 筆記
[新建版本庫](#新建版本庫)
[提交版本&更新](#提交版本&更新)
[新增&刪除檔案(資料夾)](#新增刪除檔案資料夾)
[分支](#分支)
[remote遠端](#remote遠端)
[使用者設定](#使用者設定)
[gitignore](#gitignore )
[Reset切到某版本](#Reset切到某版本)

## 新建版本庫
| Command  | note          |
| -------- | ------------- |
| git init | 初始化本地git |
| git clone |   克隆遠端儲存庫            |

## 提交版本&更新
| Command             | note                 |
| ------------------- | -------------------- |
| git status          | 查看狀態             |
| git add .           | 添加所有檔案到暫存區 |
| git add <檔案名>    | 添加指定檔案到暫存區 |
| git commit -m 'xxx' | 提交 + "備註"        |



## 新增&刪除檔案(資料夾)
| Command          | note       |
| ---------------- | ---------- |
| git rm <檔案名> | 刪除檔案   |
| git rm <資料夾> | 刪除資料夾 |
| rm -rf .git      | 移除 Git   |
| touch <檔案名>   | 建立檔案   |
| mkdir <資料夾>   | 建立資料夾           |

## 分支
| Command              | note               |
| -------------------- | ------------------ |
| git branch           | 顯示本地分支       |
| git merge <分支名稱> | 合併分支到當前分支 |

## remote遠端
| Command                         | note          |
| ------------------------------- | ------------- |
| git remote add origin git@~.git | 連結遠端      |
| git push -u origin <遠端分支>   | 上傳+綁定遠端 |
| git push                        | 推上遠端      |
- origin 默認遠端版本庫
- 遠端指 github

## 使用者設定
| Command                                      | note       | remark |
| -------------------------------------------- | ---------- | ------ |
| git config --global user.name "xxx"          | 設定用户名 | 所有   |
| git config --global user.email "xxx@xxx.com" | 設定信箱   | 所有   |

## Reset 切到某版本
| Command  | note         |
| -------- | ------------ |
|   |  |

## 其他
| Command  | note         |
| -------- | ------------ |
| git log  | 查看提交歷史 |
| git diff | 顯示未添加到暫存區的變更 |

## gitignore
當有檔案不想被版本追蹤時，可以用 gitignore 這個文件控管
常見忽略類型：密碼紀錄、套件、次數計費工具

### gitignore 忽略格式
- 檔案
**example.html**
- 整個資料夾
**/example/**
- apple 資料夾底下的檔案
**apple/example.html**
- 所有副檔名為 .ai 檔案
***.ai**
- apple 資料夾底下的所有副檔名為 .ai 檔案
**/apple/*.ai**

當檔案已經被追蹤後，即便在 .gitignore 內加入新的規則，也無法被忽略。
首先要先將追蹤解除，再寫gitignore：
```
$ git rm --cached filename    
$ git rm -r --cached foldername  
$ git rm -r --cached .
```
↑ 看情況選用