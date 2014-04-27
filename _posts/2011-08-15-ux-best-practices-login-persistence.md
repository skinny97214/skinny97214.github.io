---
layout: post
title: ! 'UX Best Practices: login persistence'
categories:
- ux
tags: []
status: publish
type: post
published: true
---
<a href="/img/amazon-comic.jpg"><img src="/img/amazon-comic.jpg" alt="persistent login from amazon ux" title="amazon-login-ux" width="600" height="261" class="alignleft size-large wp-image-472" /></a>

Login persistence has to be one of my top three UX annoyances. I see it everywhere, on tons of sites, big and small. Login friction is a huge problem and yet so many get it wrong.

I have a couple of theories about why this is. Login persistence seems like a minor issue and it's never URGENT so it never makes it up to the top of the list to get fixed. Also, there's no real upside for a developer in reducing security. Setting the login cookie to expire in a year or never means someone *could* impersonate a user on a shared and/or public computer. OH NOES! They could add tons of comments to your TPR report generator site in someone else's name! OH THE HORROR!

<img src="/img/remember-me.jpg" alt="checkbox login openid" title="remember-me" width="410" height="180" class="aligncenter size-medium wp-image-456" />

To add insult to injury is that damnable little "remember me" checkbox. Does it ever do anything? I'd like it if when I checked the box it would make the developer rip a really big windy at that moment. I digress... People are sad when you forget them. ALWAYS REMEMBER PEOPLE.

Amazon has sorted this out. They have millions of people's credit card numbers. They are a giant retailer. Their risk is much higher than yours and yet, they let you put stuff in your cart, show you recommendations based on your personal information, and see the contents of your cart. It's when you checkout that it triggers you to login. At that point, you have a very clear task to accomplish and are motivated.

How motivated are your users? I hope you're providing a richer experience to users who are logged in. Yet users are only motivated to login when they have a specific task to accomplish that requires it.

Proposal for best practice is this: have users logins persist forever. If you have sensitive info such as ecommerce, reauth right before they access that info. To keep your pretty databases from filling up with random sessions, delete the cookie if a user hasn't logged in after two or three months. That way even infrequent users will never have to reauthenticate.

We made this change on <a href="http://support.mozilla.com">support.mozilla.com</a> and it has been very well received.

What complexities do you think this would introduce?
