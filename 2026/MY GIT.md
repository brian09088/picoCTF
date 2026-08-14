**My GIT 快速解法：**

```bash
git clone ssh://git@<HOST>:<PORT>/git/challenge.git
cd challenge
cat README.md
```

依 README 設定 Git 身分：

```bash
git config user.name "root"
git config user.email "root@picoctf"
```

建立並推送 `flag.txt`：

```bash
touch flag.txt
git add flag.txt
git commit -m "add flag"
git push origin master
```

輸入題目提供的 SSH password，成功 push 後，伺服器會回傳 flag。
