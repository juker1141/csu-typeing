# 基本目錄操作指令

## 查看目錄內容
```bash
# 顯示目錄內的檔案
ls

# 顯示目錄下的詳細內容
ls -l
# 或
ll

# 顯示目錄下隱藏的檔案
ls -a

# 顯示目錄下的隱藏檔案與詳細內容
ls -al
# 或
ls -la
```

## 建立目錄
```bash
# 建立新目錄
mkdir <目錄名稱>

# 範例
mkdir 81311126
```

## 修改檔案或目錄的最後修改時間 或 當檔案不存在的時候建立空檔案
```bash
# 建立新檔案 or 修改最後的時間
touch <檔案名稱>

# 範例
touch 81311126.txt
```

## 刪除檔案 / 目錄
```bash
# 刪除檔案
rm <檔案名稱>

# 範例
rm 81311126.txt

# 刪除目錄
rmdir <目錄名稱>
rm -d <目錄名稱>

# 強制刪除檔案或目錄
rm -rf <檔案/目錄名稱>

```

## 移動使用者的位置
```bash
cd <目錄名稱>

# 範例
cd 81311126

# 移動至家目錄
cd ~

# 移動至根目錄
cd /

```

## 查看目錄或檔案是什麼類型
```bash
file <檔案/目錄名稱>

```

## 輸出文字
```bash
# 輸出純文字
echo text

# 輸出帶參數，使用 `` 包起來
echo `date`
# 輸出結果:
西元2025年03月15日 (週六) 19時52分43秒 CST

```

# 下載檔案
```bash
wget <檔案位置>

# 範例
wget https://www.csu.edu.tw/var/file/0/1000/img/1/mlogoH.png

```

## 清空畫面
```bash
clear
```

## 移動現在位置
```bash
# 相對路徑
cd ..

# 絕對路徑
cd /home
```

## 觀看檔案內容
```bash
# 相對路徑
cat ../../etc/passwd

# 絕對路徑
cat etc/passwd

# more 一頁一頁瀏覽
# | 串接指令
cat passwd | more
```


## 更改擁有者/群組
```bash

# 擁有者
chown mis shadow

# 擁有者：群組
chown mis:mis shadow

# 群組
chgrp mis shadow

```


```bash

# Read 讀 4
# Write 寫 2
# Write 執行 1

chmod 741 shadow

```

## vim 指令

R / I replace/insert

### 退出指令
```bash

esc + ":q"

# 如果編輯過後不想存檔要使用
esc + ":q!"

# 如果編輯後想存檔要使用
esc + ":wq"


```

# 使用者
```bash

# 新增 user
## -M 可以不建立 home 目錄
sudo useradd mis81311126

# 查詢是否有該user 的帳號被建立
# grep 是一個文本搜索工具
cat /etc/passwd | grep mis

# 更改密碼
sudo passwd mis8131126

# 登入使用者（確認密碼已更新, switch user
su mis8131126

# 更改使用者名稱（不會改home 的名稱
# 改成 csumis81311126 對 csu81311126 這位user
sudo usermod -l csumis81311126 csu81311126

# 刪除使用者
sudo userdel del1234 # 不會刪除使用者目錄

sudo userdel -r del1234 #會把使用者目錄刪除
```
