---
layout: post
title: ! 'Log-in that doesn''t suck: Can single sign-on finally deliver?'
categories:
- mozilla
- ux
tags: []
status: draft
type: post
published: false
---
<a href="/img/Screen-shot-2011-11-16-at-4.49.05-PM.png"><img class="alignleft size-large wp-image-677" title="Screen shot 2011-11-16 at 4.49.05 PM" src="/img/Screen-shot-2011-11-16-at-4.49.05-PM.png" alt="" width="600" height="204" /></a>

I've recently taken the baton from <a href="http://twitter.com/clarkbw">Bryan Clark</a> to pick up Mozilla's effort at fixing login, currently titled <a href="https://browserid.org/" title="Browser ID - single sign-on">BrowserID</a>. My challenge is the massive inertia of our current, kinda crappy solution where everyone uses pretty much the same password for everything. Good enough is good enough? Right? I realize we're going to have to do something massively better to overcome that inertia.

Tasked with the challenge of reinventing a core paradigm of the internet, I take a deep sigh. Let's start with a light competitive analysis, shall we?

<h3>Facebook Connect</h3>
<a href="/img/kickstarter-facebook-connect.jpg"><img src="/img/kickstarter-facebook-connect.jpg" alt="" title="kickstarter-facebook-connect" width="600" height="426" class="alignleft size-large wp-image-687" /></a>
The leader, the heavyweight, the big mamma jamma identity provider is Facebook. In 2009 when I worked at a boutique developer of Facebook-dependent microsites and apps, Stepchange, using them as the only login was a scary proposition. By 2010 it was old hat. Most mainstream sites now support legacy (password-based) login as well as Facebook Connect. It's confusing though, because in instances you're attaching the Facebook capabilities to an existing account AND/OR it's a secondary way to make an account. It's not all 100% clear in my head and I've been looking at this stuff like it's my job (it is) for years.

<h3>OpenID</h3>
<a href="/img/Screen-shot-2011-11-16-at-5.22.43-PM.png"><img class="alignleft size-large wp-image-682" title="livejournal openid nascar box of shame" src="/img/Screen-shot-2011-11-16-at-5.22.43-PM.png" alt="" width="600" height="267" /></a>Oh Livejournal, look at that Nascar box of all the different ways to log-in. It's just shameful. There's OpenID with that damn url that I CAN NEVER REMEMBER.

<h3>Google Account Chooser</h3>
<a href="/img/Screen-shot-2011-11-16-at-5.14.22-PM.png"><img class="size-full wp-image-679 alignnone" title="Screen shot 2011-11-16 at 5.14.22 PM" src="/img/Screen-shot-2011-11-16-at-5.14.22-PM.png" alt="" width="508" height="339" /></a>

This isn't a sign-on provider. It's a meta chooser that supports OpenID,SAML, OAuth2 and a whole bowlful of alphabet soup, PLUS legacy (password-based) auth. I can't figure out what the next screen would look like. I'm guessing it hands off to the sign-in provider for that.

<h3>What's the score?</h3>
<a href="/img/analysis-identity-providers.jpg"><img src="/img/analysis-identity-providers.jpg" alt="existing userbase versus UI problems with remembering which signup method" title="analysis-identity-providers" width="600" height="400" class="alignleft size-full wp-image-689" /></a>
Facebook has the massive userbase but concerns about a profit-driven company owning your access to accounts and problems when users go to a site of knowing how they signed up. OpenID has neither users nor convenient UI. BrowserID will automate keeping track of which email you used to sign up for which sites, but it doesn't have the userbase. It's a problem I'm happy to be digging my teeth into.

Further reading:

Ben Adida's <a href="http://blog.webfwd.org/post/12829575514/id-log-in-but-i-lost-my-post-it-with-all-my-password" title="    I’d log in, but I lost my post-it with all my password info…">I’d log in, but I lost my post-it with all my password info…</a>

Luke Wroblewski's <a href="http://uxdesign.smashingmagazine.com/2011/08/22/new-approaches-to-designing-login-forms/">New Approaches to Designing Log-in Forms</a>
