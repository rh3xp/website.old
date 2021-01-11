---
title: Github Changes Authentication Policy
author: thenerdsuperuser
date: '2021-01-11'
layout: post
---

WTF Github, I ended up writing this whole blog post again. ugh.

It all started with an email github sent titled "Deprecation Notice".
![Deprecation Notice](https://thenerdsuperuser.xyz/assets/images/deprecation_mail.png "Scary, isn't it?")

Apparently, last month Github thought of [deprecating the password based authentication](https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/) for it's repositories. They switched to either of the two methods instead:   
1. [Personal Authentication Token](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/creating-a-personal-access-token)   
2. [SSH Authentication](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/connecting-to-github-with-ssh)   

Now this came as a shocker, even though the deadline is [August 13, 2021](https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/#:~:text=Beginning,2021). Although they have published it on their blog, not many people have come to know about it, atleast none of my friends. So more the need to bring it out to notice.

Now, why are we using an SSH/PAT based approach exactly? I mean, it was fine while we were using the usual password based authentication. Well, as we know, tokens have been used everywhere. Be it a django app, or a password reset form which I am pretty sure everyone reading this has filled, atleast twice.
> > and if not, then wow, you have either a very good memory, or you need to update your passwords!

Coming back to PAT. The reasons it is preffered are:   
1. **Unique** – tokens are specific to GitHub and can be generated per use or per device.   
2. **Revocable** – tokens can can be individually revoked at any time without needing to update unaffected credentials.   
3. **Limited** – tokens can be narrowly scoped to allow only the access necessary for the use case.   
4. **Random** – tokens are not subject to the types of dictionary or brute force attempts that simpler passwords that you need to remember or enter regularly might be.   

This is a 3 part blog, where I will be showing you what the changes are, and how to enable SSH based auth and create Personal Authentication Tokens. 

Feel free to contact me over [twitter](https://twitter.com/vimoveremacs)
