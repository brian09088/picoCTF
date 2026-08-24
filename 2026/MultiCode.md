## MultiCode

```bash
\\ given input
NjM3NjcwNjI1MDQ3NTMyNTM3NDI2MTcyNjY2NzcyNzE1ZjcyNjE3MDMwNzE3NjYxNzQ1ZjM4NzE3MTMwMzM3MjczNzIyNTM3NDQ

\\ Base64 Decode
echo "NjM3NjcwNjI1MDQ3NTMyNTM3NDI2MTcyNjY2NzcyNzE1ZjcyNjE3MDMwNzE3NjYxNzQ1ZjM4NzE3MTMwMzM3MjczNzIyNTM3NDQ=" | base64 -d
637670625047532537426172666772715f72617030717661745f3871713033727372253744

\\ Hex Decode
echo "637670625047532537426172666772715f72617030717661745f3871713033727372253744" | xxd -r -p
cvpbPGS%7Barfgrq_rap0qvat_8qq03rsr%7D

\\ URL decode
echo "cvpbPGS%7Barfgrq_rap0qvat_8qq03rsr%7D" | python3 -c "import sys,urllib.parse;print(urllib.parse.unquote(sys.stdin.read().strip()))"
cvpbPGS{arfgrq_rap0qvat_8qq03rsr}

\\ ROT13 Decode
echo "cvpbPGS{arfgrq_rap0qvat_8qq03rsr}" | tr 'A-Za-z' 'N-ZA-Mn-za-m'

\\ get flag
picoCTF{}
```
------
## lesson learns
```
Why Base64?
Ends with =
Common encoding pattern
```
```
Why Hex?
Only characters: 0-9 a-f
```
```
Why URL Encoding?
%7B → {
%7D → }
```

## Python Automation Script
```python
import base64
import codecs
import urllib.parse
data = "NjM3NjcwNjI1MDQ3NTMyNTM3NDI2MTcyNjY2NzcyNzE1ZjcyNjE3MDMwNzE3NjYxNzQ1ZjM4NzE3MTMwMzM3MjczNzIyNTM3NDQ="
step1 = base64.b64decode(data).decode()
step2 = bytes.fromhex(step1).decode()
step3 = urllib.parse.unquote(step2)
step4 = codecs.decode(step3, 'rot_13')
print(step4)
```
<img width="1148" height="444" alt="image" src="https://github.com/user-attachments/assets/a740c1e3-4a0e-4417-afa6-fd3865b12f29" />


