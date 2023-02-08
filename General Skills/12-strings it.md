# strings 這個命令可以查看所有可視字元，
因為不是所有字元都是可以看得見的，
如 ASCII code 的 0~31 號就是不可見的，都有特殊功能。

strings 尤其對查看執行檔內部資訊相當有用，
因為裡面大部分都是不可視的，畢竟不是文字檔案。

簡單使用方式是：
strings file
可以印出 file 的所有可視字元並以換行隔開每一個。
``` command line
wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
'跳出strings檔案下載完成'
chmod +x ./strings
./strings
strings strings '上面跳出使用strings函數，後面加上檔名'
strings strings | grep "picoCTF" '使用grep來查找關鍵字picoCTF'
```
## 得出結果
picoCTF{5tRIng5_1T_827aee91}
