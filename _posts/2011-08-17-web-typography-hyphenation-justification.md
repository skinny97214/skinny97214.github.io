---
layout: post
title: ! 'Web typography: hyphenation & justification'
categories:
- design
- mozilla
- ux
tags: []
status: publish
type: post
published: true
---
<a class='hyphenation-rollover' href="/img/hyphenation-lg.jpg" style="width:410px; height:402px; display: block; text-decoration: none; border: 1px solid #ccc; background-image: url('/img/hyphenation.jpg')"></a>

<p style="font-variant:italic;"><img alt="" src="http://a2.twimg.com/profile_images/1082075935/bram-pitoyo-avatar.jpg" title="bram pitoyo, w3c-font" class="alignleft" width="50" height="50" />Post in collaboration with <a href="http://www.brampitoyo.com/" title="bram pitoyo">Bram Pitoyo</a>, Digital Design Strategist & Typographer at <a href="http://wk.com" title="wieden+kennedy">Wieden+Kennedy</a>.</p><br style="clear:both; height:0;" />

Firefox joined Safari in supporting hyphenation. Despite CSS coming out 14 years ago in 1996, we're just now getting some of the fine-grained controls necessary for beautiful typography. <a href="https://developer.mozilla.org/en/CSS/hyphens" title="MDN proposed spec for hyphenation">Details of the proposed spec</a> at Mozilla Developer Network.

<pre>
    -webkit-hyphens: auto;<br />
    -moz-hyphens: auto;<br />
    hyphens: auto;</pre>

Words need to be hyphenated because paragraphs need to be justified. But do you know why most justified texts aren’t very readable even though it looks visually pleasing at a glance? It’s not because they’re justified. It’s because they’re not justified carefully.

Mental exercise: why is the documents you’ve justified in MS Word so hard to read compared to a book? Justified text in books looks great because a lot of things have been adjusted:
<ol><li>Margin kerning. E.g. hanging punctuation.
</li><li>Character kerning. Ie. letter-spacing needs to be made tighter or looser to make the appearance more even to the eye. <a href="http://texblog.net/png/blindtext.png"><sup>[1]</sup></a>
</li><li>Additional kerning for specific characters. E.g. when typesetting French, you’d need to add a word space before (:) and after («»), and a thin space before (?), (!) and (;). <a href="http://www.microsoft.com/typography/developers/fdsspec/punc.htm"><sup>[2]</sup></a>
</li><li>Word-spacing. You can’t rely on spacing that’s mechanically widened to fit the paragraph width.
</li><li>Ligatures. Ie. when you letterspace loosely, ligatures should be turned off.</li></ol>

Justified text in a word processor doesn’t look pleasing because, well, the application doesn’t come with most of these settings.

But how far ahead (or behind) are web browsers in this department? All browsers have a setting to tweak word and letter-spacing (though not finely), and turn ligatures on and off (different browsers, different syntaxes). <a href="http://marc.baffl.co.uk/browser_bugs/css-ligatures.html"><sup>[3]</sup></a> Problem is, you’d need to adjust everything manually.

Firefox does allows for fine control of letterspacing, although it's the only browser that does. Here's a great discussion of this still frustrating topic on the <a href="http://treehouseagency.com/blog/tim-cosgrove/2011/01/22/putting-letter-spacing-under-microscope">Treehouse Agency blog</a>.

Sure, everything I’ve just described kind of returned us back at square one. But this isn’t to say that justified text isn’t appropriate to use on the web. Here’s how you can start today:

Many of us have control over words on the webpage, even as designers and developers. We can add, remove or change words around to make the word-spacing more even. If not, we have the capability to ask the copywriter sitting in the next room if this nicely-fitted wording still conveys the meaning just as well as the last version.

Since doing this to every paragraph isn’t practical, you might want to limit the use of justified spacing to shorter bodies of text that are easier to control in terms of wording. Longer subheads and introductory paragraphs are perfect.

Sources:
<ol><li><a href="http://texblog.net/png/blindtext.png">http://texblog.net/png/blindtext.png</a>
</li><li><a href="http://www.microsoft.com/typography/developers/fdsspec/punc.htm">http://www.microsoft.com/typography/developers/fdsspec/punc.htm</a>
</li><li><a href="http://marc.baffl.co.uk/browser_bugs/css-ligatures.html">http://marc.baffl.co.uk/browser_bugs/css-ligatures.html</a></li></ol>

<style type="text/css">
a.hyphenation-rollover:hover {
background-position: 0 -402px;
}
</style>
