---
layout: post
title: Ethnio + Usertesting.com for real-time unmoderated usability testing goodness
categories:
- ux
tags: []
status: publish
type: post
published: true
---
I was intrigued to use Ethnio to grab live recruits in real time. Usertesting.com has been proved itself to be a fast, cheap way to get videos of people using your site. Put them together? Magic! Like a well-executed magic trick, this combo requires finesse to make it appear effortless.

My goal was to grab users as they landed anywhere on our support site, throw them over to usertesting to watch them navigate our site to find information that solved their support issue.

The first couple tests I did failed hard. Not a single user successfully finished a video. Ouch! The conversion funnel from screener to finished video is a long and arduous one.

<a href="/img/updated_funnel.jpg"><img class="size-large wp-image-548" title="conversion funnel ethnio to usertesting.com" src="/img/updated_funnel.jpg" alt="" width="600" height="786" /></a>[/caption]

Here's what I learned in three weeks of tuning and tweaking.
<h3>Usertesting.com</h3>
Make an account and create a new task. Choose to have Ethnio pay the incentives. I still don't have 100% completion rate, so I request twice the number of users that I ultimately need. You just write to support@usertesting.com and have the extra credits refunded afterward.
<h4>URL</h4>
Usertesting requires a URL that will be shown to the participant when they start the test. This was a problem for me because I was recruiting from all over the site. There was no way to pass the participant's original URL from Ethnio. When I used our homepage as the start page, it changed the users' behavior. The hack I ultimately went with was to make a static html page that said "thanks, please close this tab."

<a href="/img/ethnio-close-tab.png"><img class="size-full wp-image-531" title="ethnio-close-tab" src="/img/ethnio-close-tab.png" alt="url that the participant will see" width="600" height="446" /></a>[/caption]
<h4>Scenario:</h4>
Today we would like to watch you as you would normally use our website to solve whatever task it was that brought you to us. Please speak aloud as we virtually peek over your shoulder so we can learn how you use our site.
<h4>Tasks:</h4>
<ol>
	<li>Please tell us what brought you to support.mozilla.com (example: I googled it and found this page.)</li>
	<li>What issue are you trying to solve?</li>
	<li>As you use our website, please keep talking and saying what you're thinking. We're especially interested in hearing if you find anything confusing or frustrating.</li>
</ol>
Take the URL it generates and move onto setting up Ethnio.
<h3>Ethnio</h3>
FYI, you may need to do start the Ethnio setup first to get the javascript you'll need to have on your production server. I had to wait an extra week waiting on the code to ship. You can these edit settings at any time, so it's no problem to use fake info at first. The setup is broken into five steps.
<h4>Setup</h4>
There's nothing tricky here. Follow their prompts.
<h4>Invite</h4>
I had to be specific that I needed them to start the task immediately. Some users were going about their task and then coming back after to fill out what they thought was a survey.

<a href="/img/screener-ethnio.png"><img class="size-full wp-image-534 " title="screener-ethnio" src="/img/screener-ethnio.png" alt="ethnio screener copy" width="590" height="486" /></a>[/caption]
<h4>Questions</h4>
Two important yes/no questions are "Does your computer have a microphone?" and "Are you okay with us watching and recording your computer screen and voice?"
<h4>Thanks</h4>
The white screener will show to users who aren't selected for the study. In the right-hand green box, turn on activate branching logic. This will bring up all the extra options you'll need to wire in usertesting.com.

<a href="/img/activate-branching-logic.png"><img class="aligncenter size-large wp-image-537" title="activate-branching-logic" src="/img/activate-branching-logic.png" alt="ethnio screener logic" width="600" height="261" /></a>

The light green box is the screener that users who've been selected will see. Users will automatically be selected and sent of to usertesting.com from there without further intervention from you. The right-hand blue box is where you put the URL that usertesting gave you.

<a href="/img/this-is-the-alternate-version.png"><img class="aligncenter size-large wp-image-538" title="this-is-the-alternate-version" src="/img/this-is-the-alternate-version.png" alt="ethnio alternate version" width="600" height="289" /></a>

At the bottom of this page is the logic that will let you filter out the users that don't match your criteria. You'll need to filter out users who said they don't have a microphone and those who don't give consent for recording their screens.

<a href="/img/filter-branching-logic.png"><img class="aligncenter size-large wp-image-541" title="filter-branching-logic" src="/img/filter-branching-logic.png" alt="ethnio set up filters for branching logic" width="600" height="423" /></a>
<h4>Activation</h4>
This is where you get the js activation code. There are other options here but js is the way to go for live recruiting. When you're ready to start your test, toggle on the test on the screener tab.
<h4>Paying incentives</h4>
After the participant has completed and uploaded their video to usertesting, you'll see their email address. You can then search the recruits page and mark them as completed by clicking on "new." This will make them appear on the incentives tab where you can then pay them.

<a href="/img/paying-incentives-ethnio.png"><img class="size-full wp-image-543" title="paying-incentives-ethnio" src="/img/paying-incentives-ethnio.png" alt="mark as completed" width="354" height="269" /></a>[/caption]
