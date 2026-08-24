# picoCTF — Password Profiler

## 題目概念

題目提供：

- `userinfo.txt`：目標人物的個人資訊
- `hash.txt`：密碼的 SHA-1 hash
- `check_password.py`：驗證密碼並取得 flag 的程式

解題流程是：

1. 讀取個人資訊
2. 使用 CUPP 根據個人資訊產生客製化密碼字典
3. 將產生的字典命名為 `passwords.txt`
4. 執行 `check_password.py` 找出正確密碼

影片中也是使用 CUPP 的 interactive mode 產生密碼字典，再交由 `check_password.py` 驗證。

---

## 1. 建立工作目錄

```bash
mkdir profiler
cd profiler
```

---

## 2. 下載題目檔案

將下列 `<URL>` 替換成 picoCTF 題目頁面提供的實際下載連結：

```bash
wget "<USERINFO_URL>" -O userinfo.txt
wget "<HASH_URL>" -O hash.txt
wget "<CHECK_PASSWORD_URL>" -O check_password.py
```

確認檔案內容：

```bash
cat userinfo.txt
cat hash.txt
```

`check_password.py` 不需要查看，直接執行即可。

---

## 3. 取得 CUPP

如果環境尚未安裝 CUPP，可以使用 Git 下載：

```bash
git clone https://github.com/Mebus/cupp.git
```

進入 CUPP 目錄：

```bash
cd cupp
```

## 3.1 也可直接編輯存檔cupp.py / cupp.cfg
``` bash
nano cupp.py
nano cupp.cfg
貼上github source file
ctrl + o (Save), ctrl + x(exit)
```
---

## 4. 使用個人資訊產生密碼字典

執行 CUPP 的互動模式：

```bash
python3 cupp.py -i
```

根據 `userinfo.txt` 的內容填寫資訊，例如：

- Name
- Nickname
- Birthdate
- Partner's name
- Child's name
- Pet's name
- Company name
- Other personal information

不確定的欄位可以直接按 Enter 略過。

CUPP 完成後，通常會產生：

```text
alice.txt
```

檔名可能會依照目標人物名稱而不同。CUPP 會根據姓名、生日、暱稱等個人資訊建立密碼字典。

回到上一層目錄：

```bash
cd ..
```

---

## 5. 將密碼字典重新命名

`check_password.py` 預期讀取的檔案名稱是 `passwords.txt`，因此將 CUPP 產生的字典重新命名：

```bash
mv cupp/alice.txt passwords.txt
```

---

## 6. 執行密碼檢查程式 get flag!

```bash
python3 check_password.py
```

程式會逐一測試 `passwords.txt` 中的密碼，找到符合 `hash.txt` 的密碼後，輸出正確密碼與 flag。
