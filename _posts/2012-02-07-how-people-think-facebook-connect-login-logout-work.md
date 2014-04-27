---
layout: post
title: How People *Think* Facebook Connect Log‑in and Log‑out Work
categories:
- ux
tags: []
status: publish
type: post
published: true
---
<a href="/img/facebook-connect1.png"><img class="alignnone size-large wp-image-888" title="facebook-connect-login" src="/img/facebook-connect1.png" alt="" width="600" height="113" /></a>

&nbsp;

As part of my work on the <a href="http://identity.mozilla.com/">Identity project</a> at Mozilla, I've been taking a look into how the average person thinks about single sign-on. It's a complex system, so not surprisingly, it's most often misunderstood at a fundamental level.

I ran an unmoderated user test with <a href="http://usertesting.com">usertesting.com</a> with five users. Their task was to go to <a href="http://Buyosphere.com">Buyosphere</a>, a site that implements Facebook Connect, create an account, then log out. Then I asked them a series of questions. All five indicated they had used Facebook to log into sites before.

"When you log out of Buyosphere, do you think it logs you out of Facebook also? Why or why not and how would you tell for sure?" Incorrect answers are red and bold.
<ul>
	<li><span style="color: #800000;"><strong>User 1)</strong></span> "i believe that once i log out of buyosphere, i am also logged out of facebook. once i am logged out i cannot see any more information regarding my account after logging out."</li>
	<li><span style="color: #800000;"><strong>User 2)</strong></span> "I think it does log me out because it gave me connect with Facebook, thus it mean it is not recognizing that I have a Facebook account. I'd tell if I am or not by opening up Facebook in a new tab and seeing if it is automatically logged in or not."</li>
	<li>User 3) "No, I told facebook to remember me. I would open my facebook page in a different browser window? I don't normally tell it to log me out, so that is only a guess."</li>
	<li><span style="color: #800000;"><strong>User 4)</strong></span> "Yes. I do not see a separate window for my facebook site so I would assume that Buyosphere would have set it up to log me out when I'm done on their site. I think I can check to see if I'm logged out by opening facebook and seeing if the login boxes come up or if it takes me straight to my FB page. I will try it right now....I was wrong it didn't log me out. I am surprised by that. That makes the process of logging off take longer if I have to log out of this site and then go to FB to log out of that site separately."</li>
	<li>User 5) "I don't think it would log me out. I have used other sites through facebook and usually the log in and log outs are separate. I can tell for sure by checking my facebook page which I just did and I am logged in."</li>
</ul>
The goal of this research was to determine if users had a mental model that would allow them to correctly log out of a single sign-on system in places where there are security concerns like a shared computer or public terminal. The answer is no. <em>Disclaimer: Do not be tempted to extrapolate that this means 60% of people would get this question wrong. This is qualitative research, not quantitative and should not be regarded as having statistical significance.</em>

The last little gut-wrenching nugget comes from the last 20 seconds of one test. Watch and weep.

<object id="_player" width="610" height="399" classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowfullscreen" value="true" /><param name="allowscriptaccess" value="always" /><param name="flashvars" value="config={'key':'#$a7865b80ef02a600b6d','screen':{'width':'610','height':'375','top':'0','left':'0'},'clip':{'url':'http://dc2.usertesting.com/videos/255685-1.mp4', 'autoPlay':false},'plugins':{'controls':{'url':'http://www.usabilitytestresults.com/fp/flowplayer.controls-3.2.5.swf','autohide':'never'}}}" /><param name="src" value="http://www.usabilitytestresults.com/fp/flowplayer.commercial-3.2.6.swf" /><embed id="_player" width="610" height="399" type="application/x-shockwave-flash" src="http://www.usabilitytestresults.com/fp/flowplayer.commercial-3.2.6.swf" allowfullscreen="true" allowscriptaccess="always" flashvars="config={'key':'#$a7865b80ef02a600b6d','screen':{'width':'610','height':'375','top':'0','left':'0'},'clip':{'url':'http://dc2.usertesting.com/videos/255685-1.mp4', 'autoPlay': false, 'autoBuffering': true},'plugins':{'controls':{'url':'http://www.usabilitytestresults.com/fp/flowplayer.controls-3.2.5.swf','autohide':'never'}}}" /></object>

You caught it, right? She believes she could use her Facebook user and password to log into this site. *sigh* It's horrifying how easily a bad actor could build a honeypot to collect Facebook credentials.

In addition to confusion over when/where/how to log-in and log-out, we know that sites have big percentages of users with multiple accounts. This video clearly illustrates how that can happen.

What are sites to do? I don't think there is a good answer. As much as your business case allows, use only one identity provider. If you're using Facebook Connect, don't have a standard log-in. Too often, two log-in systems are less than the sum of their parts. <a href="http://uxdesign.smashingmagazine.com/2011/08/22/new-approaches-to-designing-login-forms/">LukeW's article</a> details experiments to mitigate these problems. Some of them have security concerns that wouldn't fly with many sites. I'm not confident any of them work massively better than only supporting one way of logging in. However, many site will feel it necessary to have a standard log-in plus Facebook Connect. Clearly more thinking and testing needs to be done in this direction.

Of course, my biased view is that we can build <a href="http://identity.mozilla.com/">better solutions for single sign-on</a>.
