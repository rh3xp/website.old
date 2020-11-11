---
title: old projects revisited
author: thenerdsuperuser
date: '2020-11-11'
layout: post
---

SO, I found out that my old websites are still hosted on surge.sh so, i thought, why not git them.

the following were once my blogs(lol) :

1. http://bored-hand.surge.sh   
2. http://sturdy-neck.surge.sh   
3. http://icky-grape.surge.sh/   


They are all static websites. 
I am planning to clone these, as I dont have the source code anymore.

`wget` will help me as always



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
