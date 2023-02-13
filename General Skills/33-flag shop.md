- 1. 這題需要先打開看c檔案
- 2. 之後根據程式碼37~39行
- 3. 我們需要讓number_flags超過int limit使其overflow 變成負數
- 4. 之後便能將 total_cost 最大化，因為a-(-b) = a+b
- 5. int limit  -2147483648 ~ 2147483647
- 6. 2147483647/900 = 2386092
- 7. 2386092 -> 2386192
**所以最後要輸入2386192**

``` C
if(number_flags > 0){
   int total_cost = 0;
   total_cost = 900*number_flags;
```

![image](https://user-images.githubusercontent.com/72643996/218490367-70555928-1e41-4db6-a03b-97629c3518bb.png)
![image](https://user-images.githubusercontent.com/72643996/218490415-a467cecb-5e56-4b02-8c08-d11b9cb7326f.png)
