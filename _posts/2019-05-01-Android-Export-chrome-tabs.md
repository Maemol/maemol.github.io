---
layout: post
title: How to Export Android Chrome tabs
subtitle: Export all open tabs from Android Chrome via chrome dev tools
tags: [Android]
comments: true
---

I read a lot during transit, often I start an article and don't have time to finish it so I just keep the tab open and wait to find the time to finish it. After a while, I find myself with more than 100 open tabs and no way to easily find what's important and what's not.

That's why I need to export them in a list to review them on my computer.

After some research, I found this thread on [stackexchange](https://android.stackexchange.com/questions/56635/how-can-i-export-the-list-of-open-chrome-tabs) and it's the only way I manage to export all my tabs without losing tabs or character in their url.


- So first, connect your Android phone via USB and activate the USB debugging.

- On your computer, open chrome dev tools (ctrl + shift + J).

- Undock into separate window.

- Go to More tools then Remote devices.

![Remote devices](https://maemol.github.io/img/devtools_remote.jpg)

- Select your device and check that you see your tabs.

- Open a new dev tools window (ctrl + shift + J) then select the element with your tabs.

![Element](https://maemol.github.io/img/devtools_element.jpg)

- Find <div class="vbox"> under <div class=device-page-list vbox device-viw-more-toggled> and check that you see your tabs.

- Go to the console and run this script :

```javascript
tabs = Array.from(document.querySelector('div /deep/ div /deep/ div /deep/ div /deep/ div /deep/ div /deep/ div.vbox.flex-auto').shadowRoot.querySelectorAll('.devices-view .device-page-list .vbox'), s => ({name: s.querySelector('.device-page-title').textContent, url: s.querySelector('.device-page-url .devtools-link').getAttribute('href')})) 
str = '';
for (i=0;i<tabs.length;i++){
	str += tabs[i]['name'] + '~' + tabs[i]['url'] + '\n'
	}
copy(str)
```

![Console](https://maemol.github.io/img/devtools.jpg)

- Now you can paste the list somewhere. I used ~ as a separateur between the name and the URL to split them easily.


