這題比較特別
======
- 下載三個檔案
  - 1. 打開.py檔案
       - 查看最後第44行所有密碼的那列
       - 每跑一次就編譯一次，一個一個慢慢試，試到密碼正確為止，就會得到flag
  - 2. 用power shell 下載.bin檔案
  ``` command line
  bvi level3.hash.bin
  ```
       - 得到16進位的一串數字
       - 將數字一連串複製貼上，記得把空白忽略掉
       - 拿去 [https://crackstation.net/] 進行爆破，解出密碼4b17(也會在剛剛的set中)

![image](https://user-images.githubusercontent.com/72643996/218401846-3605d951-e5ab-48aa-bfb7-41e5c5b754cb.png)
