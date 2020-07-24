---
layout: page
title: New Post
permalink: /newpost/
---

# Syntax hints for post formatting

All post files must begin with *front matter* which is typically used to set a layout or other meta data. For a simple example this can just be empty:


```
---
layout:     post
date:       2020-07-09 21:21:29
title:      Title of your Lesson
summary:    Summary of your Lesson
tags: ['School Teachers', 'Students', 'Hobbyists' ]
---
```

- Every *post* can have one `tag` or multiple `tags`. It will automatically split a string entry if it contains whitespace. The website software  Jekyll expects multiple items mapped to the key tags For example, while front matter `tag: classic hollywood` will be processed into a singular entity `"classic hollywood"`, front matter `tags: classic hollywood` will be processed into an array of entries `["classic", "hollywood"]`. 

- After the front matter make your lesson post formatting it in `markdown` refer to this cheat sheet [https://github.com/WVURAIL/dspira-lessons/wiki/Markdown-Cheatsheet](https://github.com/WVURAIL/dspira-lessons/wiki/Markdown-Cheatsheet)

- Add buttons to link to a pdf of your document using this syntax

```
[Google](http://www.google.com){: .button}
```
In Google Drive:
- open document
- click share button (upper right corner)
- in dialogue box, change the get link attribute to Anyone with link with viewer priveleges. see screenshot below

![screen shot of changing permissions of google document](/image/SharedScreenshit.jpg)

EXAMPLE:
- To add a Google doc lesson:
```
[Name of your lesson](https://link/to/your/document/dotcom){: .button}
```

- Add YouTube link:
Add an embedded window of the youtube video to the page by simply paste the youtube link on the markdown page on its own. Please add a couple of lines describing the contents of the video at minimum. 

```
https://www.youtube.com/watch?v=jS5fTzMP_mg

The above video is a video of Kermit the frog singing the rainbow connention
```


### View the live webpage: [wvurail.org/dspira-lessons](http://wvurail.org/dspira-lessons/)


# Add Edit yout post here following the above intructions to properly  

- Make sure to enter your lesson filename.
- Click save to save the file
- Upload the file appropraitely on the github repostory in the appropraite directory to post to the website

<html>
<body>
<div>
    <p>Date:</p><h2 id="date"></h2>
    New Post:

    <textarea id="inputTextToSave" cols="80" rows="25">
---
layout: post
date:   copy date from above
title: add title
summary:  add a one summary (~10 word summary) 
tags: ['School Teachers', 'Students', 'Hobbyists' ]
---

Enter the Lesson posts here
    </textarea>
    Filename to Save As:
    <input id="inputFileNameToSaveAs"></input>&nbsp;&nbsp;<button onclick="saveTextAsFile()">Save</button>

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