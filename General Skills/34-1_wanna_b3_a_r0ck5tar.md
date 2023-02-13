本系列General Skills最後一題
2023/02/13 全部解完
======

- 將連結song下載得到lyrics.txt文字檔
- 打開後需要透過前面提到的rockstars去做編譯
- 這裡透過rockstars的網址[https://github.com/yanorestes/rockstar-py] 提供的github裡面有.py套件
``` command
pip install rockstar-py #在cmd輸入後運行
```
- 在VS-code 打開txt檔案後，終端機輸入
```
rockstar-py -i lyrics.txt
```
- 得到output.py
- 打開後發現中間有許多數字變量，將他使用ASCII轉換網址 [https://www.rapidtables.com/convert/number/ascii-hex-bin-dec-converter.html] 去得到BONJVI
- 但是中間有一行They are dazzled audiences沒有翻譯到
- 因此這邊推斷出知名搖滾樂團-BONJOVI就是flag
- 加入後picoCTF{BONJOVI}就是答案
