# Linux 指令

## 常用系統指令

| 指令  | 說明             |
| ----- | ---------------- |
| cd    | 切換目錄         |
| pwd   | 顯示目前所在目錄 |
| ls    | 列出目前檔案列表 |
| mkdir | 建立新的目錄     |
| touch | 建立檔案         |
| cp    | 複製檔案         |
| rm    | 刪除檔案         |
| mv    | 移動檔案         |
| clear | 清除畫面內容     |

## ls-列出目錄下的檔案

| 指令    | 說明                 |
| ------- | -------------------- |
| ls      | 列出基本資料夾資料   |
| -l      | 列出詳細資料         |
| -a      | 列出所有包含隱藏資料 |
| ls *.py | 列出為.py的檔案      |

## 檔案處理

- 刪除目前資料夾下副檔名為.js檔案
`$ rm *.js`
- 刪除資料夾（包括在內的檔案）
`$ rm -rf /Users/folder1`
- cat:將文件印在Terminal
`$ cat README.md`
- tail:顯示檔案最後幾行內容
`$ tail README.md`
- 持續顯示更新內容（常應用於web server看lod debug使用
`tail -f README.md`

## Linux檔案系統標準

- /bin、/sbin
  - /bin放置一般使用者可操作的指令
  - /sbin放置系統管理員可操作的指令
- /etc 放置系統檔案
- /home、/root
  - /home 主要是一般帳戶的家目錄
  - /root 為系統管理者的家目錄
- /lib、/lib64 主要為系統函式庫和核心函式庫
- /proc 將記憶體內的資料做成檔案類型
- /sys 與 /proc 類似，但主要針對硬體相關參數
- /usr 全名為unix software resource，放置系統相關軟體、服務
- /media、/mnt 放置隨插即用的裝置慣用目錄， /mnt 為管理員/使用者手動掛上
（mount）的目錄
/opt - 全名為optional，通常為第三方廠商放置軟體處

## 查找檔案及其內容

- 在目前目錄下尋找檔名為README.md的檔案
`$ find . -name README.md`
- grep:文件字串搜尋工具
`$ grep '找這個字串' file_name`
- 找所有目錄（含子目錄）下檔案
`$ grep -r '字串'`

## References

<https://kim85326.github.io/2019/01/16/Terminal-指令/>

## 待整理

df -h 看硬碟容量
lsblk -p
mskf? 格式化
