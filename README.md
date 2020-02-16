# PERMALINK-for-Gist
to create permanent link that will forever include all the changes, not just the revision

### solution
this is done by creating <ins>reverse proxy repo</ins>.  
here the permanent url is github-pages url of script.md in repo  
which contains the url of gist (which we can change at anytime).

## step 1
create repositorie with GitHub Pages turned on
###### example : [https://github.com/nkpro2000sr/man-manjaro](https://nkpro2000sr.github.io/man-manjaro/ "man-manjaro `blog by manjaro user`")

## step 2
create a reverse_proxy_script.md which has url of latest revision gist  
###### example : [sample-script.md](https://gist.github.com/nkpro2000sr/af9f3eb1346c1dc6a1a8ce78ec78cca1 "script.md")
```js
var url = "latest_gist_url"
document.write('<script src="'.concat(url,'"></script>'))
```

## step 3
now `<script src="https://UserName.github.io/reverse-proxy-repo/reverse-proxy-script.md"></script>`
is the permanent url. :wink:

### note
* you can create many reverse_proxy_scriptn.md for each gists in same repositorie
* if gist is revised, altering the reverse_proxy_script.md with new url will make permanent url redirecting to latest revision
