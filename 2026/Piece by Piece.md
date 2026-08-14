## Piece by Piece 簡單解法

SSH 連線：

```bash
ssh ctf-player@<HOST> -p <PORT>
```

查看提示：

```bash
cat instructions.txt
```

合併所有分割檔：

```bash
cat part_* > combined.zip
```

用密碼解壓縮：

```bash
unzip -P supersecret combined.zip
```

最後讀取 flag：

```bash
cat flag.txt
```

重點就是：**合併 `part_*` → 用 `supersecret` 解壓縮 → 讀取 `flag.txt`**。
