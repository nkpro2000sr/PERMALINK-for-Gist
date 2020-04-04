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

now `<script src="url_to_your_github_pages/reverse-proxy-script.md"></script>`
is the permanent url. :wink:  
> 'url_to_your_github_pages' is like 'https://UserName.github.io/github-pages-activated-repo-name'.  

#### Sample:
see this [demo.html](https://nkpro2000sr.github.io/Updatable-PermaLink/demo.html "https://nkpro2000sr.github.io/Updatable-PermaLink/demo").  

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

In these examples, 1,3,5 have extension and 2,4,6 don't have extension.  
GitHub Pages serves these with different header based on extension.
If no extension provided it is considered same as only downloadable file.  
In above example:
1. SampleImage1 is shown in page. since it has image file extension.
> GitHub Pages don't shows images > 5MB. it simply asks to downloads it. (see [this](https://stackoverflow.com/questions/56724914/github-images-links-downloaded-instead-of-showing "Someone contacted GitHub") for reason)
2. SampleImage2 is simply asks to download. since it don't has extension.  
3. SamplePDF1 is shown in browser. since it has pdf extension.  
4. SamplePDF2 is simply asks to download. since it don't has extension.  
5. SampleFile1 is also asks to download. since zip file format is not viewed in browser.  
6. SampleFile2 is simply asks to download. since it don't has extension.  

\> We can also force url with showable extension to simply asks to download by a simple trick.  
1. Create an html file. For example 'SampleImage.png.html'
```html
<a id="Download" href="SampleImage.png" download></a>
<script type="text/javascript">
    (function () {
      document.getElementById("Download").click();
    })();
</script>
```
2. now [https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage.png.html](https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage.png.html "Only Download Image") will only download image instead of [showing like example_1](https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage.png "https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage.png").  

\> We can also force url without showable extension to show.  
1. Create an html file. For example 'SampleImage.html'  
```html
<img src="SampleImage" style="max-width:100%;height:auto;">
```
2. now [https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage.html](https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage.html "Only Shows Image") will only shows image instead of [downloading like example_2](https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage "https://nkpro2000sr.github.io/Updatable-PermaLink/SampleImage").  

> we can also make PDF shown in browser instead of downloading by [this](https://github.com/MrRio/jsPDF/issues/1969 "Solution Available Here") method.  

### Note:
The files whose filename begins with underscore '\_' will not be accessed via url.  
Example '\_nk.png' will not be viewed using [https://nkpro2000sr.github.io/Updatable-PermaLink/\_nk.png](https://nkpro2000sr.github.io/Updatable-PermaLink/_nk.png "Using Github Pages").  
But can be viewed through:  
1. Github [https://github.com/nkpro2000sr/Updatable-PermaLink/blob/master/\_nk.png](https://github.com/nkpro2000sr/Updatable-PermaLink/blob/master/_nk.png "Github")  
2. Raw Github Content [https://raw.githubusercontent.com/nkpro2000sr/Updatable-PermaLink/master/\_nk.png](https://raw.githubusercontent.com/nkpro2000sr/Updatable-PermaLink/master/_nk.png "RawGitHubUserContent").  

*only if it is a public repo.*  
