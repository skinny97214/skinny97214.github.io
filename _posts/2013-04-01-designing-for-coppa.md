---
layout: post
title: Designing for COPPA
categories:
- design
- mozilla
- ux
tags: []
status: publish
type: post
published: true
meta:
  _edit_last: '1'
  _thumbnail_id: '1042'
  sgt_slide: 'on'
---
If you've never heard of COPPA, consider yourself lucky... and now, warned. Chances are, if you're finding this article via a search engine, you're already in the thick of it. For that, I offer my consolations and a few lessons learned.<!--more--> <em>Disclaimer: I am not a lawyer. None of the suggestions contained in this blog post constitute legal advice.</em>

<a href="/img/sidewalk-chalk-kid.jpg"><img class="size-large wp-image-1042" alt="sidewalk-chalk-kid" src="/img/sidewalk-chalk-kid.jpg" width="600" height="450" /></a><span style="font-size: 9px;">Some rights reserved by <a title="original photo at flickr" href="http://www.flickr.com/photos/18123948@N00/281857282">matt.forestpath</a></span>
<h3>Age Neutral Verification</h3>
This is the biggest area of impact on the interface. If you have a site which offers kid-attractive content, you'll need to know if they're above thirteen before making an account or storing personally identifiable information.

The problem is that you can't actually ask that in a way that indicates that thirteen is the break point. This is what "age-neutral verification" means. If only it was as simple as a checkbox that they tick which says "I am over 13 years of age." Nuuuh-uh, not so fast, cowboy. That's not legal. (See <a title="COPPA FAQs" href="http://www.ftc.gov/privacy/coppafaqs.shtm" target="_blank">FAQ #39 of the COPPA statute</a>.)

If the user fails the age-neutral test, <strong>you must fail in a obtuse way</strong> that doesn't indicate to them that the age check was the reason. This defies all good UX principles around writing clear error message that tell people what is actually going on. As much as this boils my cockles, it is the law. But it doesn't end there. You must prevent them from turning around trying again. Finally, your company must delete all info from any source that you have about that user.
<h3>Options</h3>
<a href="/img/coppa-birthday-facebook.png"><img class="size-full wp-image-1034 alignnone" alt="coppa birthday example from facebook" src="/img/coppa-birthday-facebook.png" width="511" height="83" /></a>

Most providers, including the screenshot from Facebook, are asking for a birth date, as that's the example solution given in the law. Facebook's popup delicately explains "Providing your birthday helps make sure you get the right Facebook experience for your age. You can choose to hide this info from your timeline later if you want. For more details, please visit our <a href="https://www.facebook.com/about/privacy/">Data Use Policy</a>."

<a href="/img/Screen-Shot-2013-04-01-at-2.05.42-PM.png"><img class="alignnone size-full wp-image-1039" alt="COPPA birth year" src="/img/Screen-Shot-2013-04-01-at-2.05.42-PM.png" width="432" height="100" /></a>

Another option is to simplify down to only asking for the birth year. The drawback to this method is that you need to toss out all of the people who turned thirteen that calendar year who would otherwise be able to use your site.

<a href="/img/age-neutral-btwf.png"><img class="size-full wp-image-1037 alignnone" alt="Age Neutral Verification BTWF" src="/img/age-neutral-btwf.png" width="299" height="116" /></a>

Lastly, my favorite option is the radio buttons with age ranges approach. This example is from the Born This Way Foundation. It's the best UX but the riskiest approach from a legal standpoint.
<h3>Tricks up our sleeve</h3>
Since Gmail, Hotmail, Yahoo all are under the same restrictions, they have already asked this question of users. A feature we've been talking about for <a title="Mozilla Persona : the official blog" href="http://identity.mozilla.com/" target="_blank">Persona</a> is to flag such users' accounts as good to go. As we roll this future feature out, this will mean that we can give sites both a verified email address and a verified age-neutral check.  Again, check with your lawyers to see what sort of documentation you'll need to keep around to prove that these third parties were indeed performing the check.
