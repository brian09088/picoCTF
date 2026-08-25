## Log hunt

``` bash
wget https://challenge-files.picoctf.net/c_amiable_citadel/49cec6157142f24a599f4164d5b63322c2494f801390d6f22eb91b3aa592bc66/server.log
grep "picoCTF" server.log
grep "INFO FLAGPART" server.log
```
<img width="566" height="588" alt="image" src="https://github.com/user-attachments/assets/b5620a22-efaf-42a6-8e63-0197fbf4f6db" />

combine string segments of the flag info
```
picoCTF{us3_y0urlinux_sk1lls_cedfa5fb}
```

