# PERMALINK-for-Gist
to create permanent link that will forever include all the changes, and uptodate.  

### solution
this is done by creating <ins>Github Repo with GitHub Pages activated</ins>.  
here the permanent url is github-pages url of content in repo.  
which can be updated at any time.  

## Primary Step
create repository with GitHub Pages turned on
###### example : [https://github.com/nkpro2000sr/man-manjaro](https://nkpro2000sr.github.io/man-manjaro/ "man-manjaro `blog by manjaro user`")

## * For Dynamic Embedded Gist  
create a reverse_proxy_script.md which has url of gist you want to show.    
###### example : [sample-script.md](https://gist.github.com/nkpro2000sr/af9f3eb1346c1dc6a1a8ce78ec78cca1 "script.md")
```js
var url = "gist_url"
document.write('<script src="'.concat(url,'"></script>'))
```

now `<script src="https://UserName.github.io/reverse-proxy-repo/reverse-proxy-script.md"></script>`
is the permanent url. :wink:  

## * For Dynamic File Link  
Upload a file you want to create link for in your github pages activated repo.  

now `url_to_your_github_pages/Filename` is the link to then file.  
you can also place file in directories inside repo, for this just replace Filename by File path in url.  
