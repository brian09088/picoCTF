# solutions
```script
## picoCTF「Undo」簡單解法

先用題目啟動後提供的連線資訊：

```bash
nc <HOST> <PORT>
```

每一關看到提示後，輸入「反向操作」的 Linux 指令：

1. **Base64 解碼**

```bash
base64 -d
```

2. **反轉字串**

```bash
rev
```

3. **將 `-` 還原成 `_`**

```bash
tr '-' '_'
```

4. **將 `()` 還原成 `{}`**

```bash
tr '()' '{}'
```

5. **還原 ROT13**

```bash
tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

題目會自動把目前字串傳入指令，所以通常只要輸入指令本身，不需要自行輸入 `echo` 或整段字串。

依公開範例，最後的 flag 格式為：

```text
picoCTF{Revers1ng_t3xt_Tr4nsf0rm@t10ns_aa00e8fb}
```

但每次 instance 產生的尾碼可能不同，請以你自己連線後得到的結果為準。
```
