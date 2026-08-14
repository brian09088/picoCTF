# hints:
knowing how SMB protocol works would be helpful!
smbclient and smbutil are good tools
------
# solutions
``` script
nc -vz mysterious-sea.picoctf.net 16888
使用指令提示-L 網址 -p port
smbclient -L //mysterious-sea.picoctf.net -p 16888
<img width="1056" height="255" alt="image" src="https://github.com/user-attachments/assets/555db439-86a9-4125-b2b8-211f675671ad" />

找出檔案內有shares
smbclient //mysterious-sea.picoctf.net/shares -p 16888
<img width="628" height="189" alt="image" src="https://github.com/user-attachments/assets/8c7321a9-3a0b-4b64-9550-b0848d150e27" />
進入smb 指令集
ls 找出flag.txt
get flag.txt
exit跳出smb
cat flag.txt
get flag
```

