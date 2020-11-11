---
title: Old Projects Revisited
author: thenerdsuperuser
date: '2020-11-11'
layout: post
---

So, I found out that my old websites are still hosted on surge.sh so, i thought, why not git them.

the following were once my blogs(lol) :

1. [This is good for logging](http://bored-hand.surge.sh)   
2. [A bit nerdy](http://sturdy-neck.surge.sh)   
3. [why did i even](http://icky-grape.surge.sh)   


They are all static websites. 
I am planning to clone these, as I dont have the source code anymore.

`wget` will help me as always. Took the reference from [here](https://alvinalexander.com/linux-unix/how-to-make-offline-mirror-copy-website-with-wget/)



```bash
	wget --mirror            \
	     --convert-links     \
	     --html-extension    \
	     --wait=2            \
	     -o log              \
	     http://bored-hand.surge.sh
```

Although it only clones the homepage(index.html), luckily the surge CDN has my JS and CSS files stored online which can be found in the `link rel` tags

Anyway, gotta see what to do now.
