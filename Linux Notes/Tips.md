
>[!tip] Search web from terminal 
>ddgr duck duck go

``` bash
mkdir duckduckgo
cd duckduckgo/
git clone https://github.com/jarun/ddgr.git
cd ddgr
sudo make install
```
>[!example] ddgr waterloo university

---
>[!tip] Move only files to sub dir set2
``` bash
find . -maxdepth 1 -type f ! -name ".*" -exec mv -t set2/ -- {} +
```
*move hidden files too*
``` bash
find . -maxdepth 1 -type f -exec mv -t set2/ -- {} +
```

---
>[!tip] Double width colon
>echo -e '\uFF1A'

``` bash
echo -e '\uFF1A'
```