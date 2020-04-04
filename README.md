# solution
this is done by creating <ins>Github Repo with GitHub Pages activated</ins>.  
here the permanent url is github-pages url of content in repo.  
which can be updated at any time.  

## Primary Step
create repository with GitHub Pages turned on
###### example : [https://github.com/nkpro2000sr/man-manjaro](https://nkpro2000sr.github.io/man-manjaro/ "man-manjaro `blog by manjaro user`")

## #] For Dynamic Embedded Gist  
create a reverse_proxy_script.md which has url of gist you want to show.    
###### example : [sample-script.md](https://gist.github.com/nkpro2000sr/af9f3eb1346c1dc6a1a8ce78ec78cca1 "script.md")
```js
var url = "gist_url"
document.write('<script src="'.concat(url,'"></script>'))
```

now `<script src="https://UserName.github.io/reverse-proxy-repo/reverse-proxy-script.md"></script>`
is the permanent url. :wink:  

## #] For Dynamic File Link  
Upload a file you want to create link for in your github pages activated repo.  

now `url_to_your_github_pages/Filename.ext` is the link to the file.  
you can also place file in directories inside repo, for this just replace Filename by File path in url.  

##### Exapmple:
1. Sample Image 1: [https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage.png](https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage.png "Only Shows Image")  
2. Sample Image 2: [https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage](https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage "Only Downloads Image")  
3. Sample PDF 1: [https://nkpro2000sr.github.io/Updatable-PermaLink/SamplePdf.pdf](https://nkpro2000sr.github.io/Updatable-PermaLink/SamplePdf.pdf "Only Shows PDF")  
4. Sample PDF 2: [https://nkpro2000sr.github.io/Updatable-PermaLink/SamplePdf](https://nkpro2000sr.github.io/Updatable-PermaLink/SamplePdf "Only Downloads PDF")  
5. Sample File 1: [https://nkpro2000sr.github.io/Updatable-PermaLink/Sample.zip](https://nkpro2000sr.github.io/Updatable-PermaLink/Sample.zip "Only Downloads File")  
6. Sample File 2: [https://nkpro2000sr.github.io/Updatable-PermaLink/SampleFile](https://nkpro2000sr.github.io/Updatable-PermaLink/SampleFile "Only Downloads File")  


### Note:
The files with filename presiding underscore '\_' will not be accessed via url.  
Example '\_nk.png' will not be viewed using [https://nkpro2000sr.github.io/Updatable-PermaLink/\_nk.png](https://nkpro2000sr.github.io/Updatable-PermaLink/_nk.png "Using Github Pages").  
But can be viewed through:  
1. Github [https://github.com/nkpro2000sr/Updatable-PermaLink/blob/master/\_nk.png](https://github.com/nkpro2000sr/Updatable-PermaLink/blob/master/_nk.png "Github")  
2. Raw Github Content [https://raw.githubusercontent.com/nkpro2000sr/Updatable-PermaLink/master/\_nk.png](https://raw.githubusercontent.com/nkpro2000sr/Updatable-PermaLink/master/_nk.png "RawGitHubUserContent")  
