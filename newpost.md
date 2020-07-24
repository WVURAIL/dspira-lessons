---
layout: page
title: New Post
permalink: /newpost/
---

These are instructions and a simple template to start creating a new post!

## Syntax hints for post formatting

All post files must begin with *front matter* which is typically used to set a layout or other meta data. For a simple example this can just be empty:


```
---
layout:     post
date:       2020-07-09 21:21:29
title:      Title of your Lesson
summary:    Summary of your Lesson
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Lessson Category']
---
```

- Make sure you do not have special characters like `:` in your title and/or summary quote any special characters, such as `:` like `title: "my awesome site: an adventure".`
- Every *post* can have one `tag` or multiple `tags`. It will automatically split a string entry if it contains whitespace. The website software  Jekyll expects multiple items mapped to the key tags For example, while front matter `tag: classic hollywood` will be processed into a singular entity `"classic hollywood"`, front matter `tags: classic hollywood` will be processed into an array of entries `["classic", "hollywood"]`. 
- `categories` or `category` work the same way as tags.

- After the front matter make your lesson post formatting it in `markdown` refer to this cheat sheet [https://github.com/WVURAIL/dspira-lessons/wiki/Markdown-Cheatsheet](https://github.com/WVURAIL/dspira-lessons/wiki/Markdown-Cheatsheet)

- Add buttons to link to a pdf of your document using this syntax

```
[Google](http://www.google.com){: .button}
```

In Google Drive:
- open document
- click share button (upper right corner)
- in dialogue box, change the get link attribute to Anyone with link with viewer priveleges. see screenshot below

![screen shot of changing permissions of google document](/images/SharedScreenshot.jpg)

EXAMPLE:
- To add a Google doc lesson:
```
[Name of your lesson](https://link/to/your/document/dotcom){: button}
```

- Add YouTube link:
Add an embedded window of the youtube video to the page by simply paste the youtube link on the markdown page on its own. Please add a couple of lines describing the contents of the video at minimum. 

```
https://www.youtube.com/watch?v=jS5fTzMP_mg

The above video is a video of Kermit the frog singing the rainbow connention
```
##### Addding images to the posts

To add images to your post first upload your image to github by going to the link below  upload and commit an image to the the images directory: 

[Upload image](https://github.com/WVURAIL/dspira-lessons/upload/master/images){: .button}

Then add the following to the post you are editing
```
![write-a-brief-alt-text-describing-your-image]({{ site.baseurl }}/images/name-of-you-image-file.FORMAT)
```
### View the live webpage: [wvurail.org/dspira-lessons](http://wvurail.org/dspira-lessons/)


##  Edit your post in the text area below 

<html>
<body>
<div>
    <p>Date:</p><h2 id="date"></h2>
    <div>
    <textarea id="inputTextToSave" cols="80" rows="25">
---
layout: post
date:   copy date from above
title: edit this title
summary:  edit this a ~10 word summary
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['category', 'Subcategory'] 
---

Enter the Lesson posts here
    </textarea></div>
    <div>
    Filename to Save As: &nbsp; <input id="inputFileNameToSaveAs">&nbsp;.md
    <button onclick="saveTextAsFile()">Save</button>
    </div>
</div>

<div> Upload your saved file to the website by uploading and commiting on github.com: &nbsp;
 <a href="https://github.com/WVURAIL/dspira-lessons/upload/master/_posts" class = "button">Upload to Website</a>
</div>

<script type="text/javascript">
 
n =  new Date();
y = n.getFullYear();
m = n.getMonth() + 1;
d = n.getDate();

if (d < 10) {
  d = '0' + d;
}
if (m < 10) {
  m = '0' + m;
}

datetoday = y + "-" + m + "-" + d;
document.getElementById("date").innerHTML = datetoday

function saveTextAsFile()
{
    var textToSave = document.getElementById("inputTextToSave").value;
    var textToSaveAsBlob = new Blob([textToSave], {type:"text/plain"});
    var textToSaveAsURL = window.URL.createObjectURL(textToSaveAsBlob);
    var fileNameToSaveAs = datetoday + "-" + document.getElementById("inputFileNameToSaveAs").value + ".md";
 
    var downloadLink = document.createElement("a");
    downloadLink.download = fileNameToSaveAs;
    downloadLink.innerHTML = "Download File";
    downloadLink.href = textToSaveAsURL;
    downloadLink.onclick = destroyClickedElement;
    downloadLink.style.display = "none";
    document.body.appendChild(downloadLink);
 
    downloadLink.click();
}
 
function destroyClickedElement(event)
{
    document.body.removeChild(event.target);
}

</script>
 
</body>
</html>
