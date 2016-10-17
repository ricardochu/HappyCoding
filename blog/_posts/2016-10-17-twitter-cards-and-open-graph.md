---
layout: blog-post
title: Twitter Cards and Open Graph
slug: twitter-cards-and-open-graph
meta-title: Twitter Cards and Open Graph
meta-description: Ever wonder how Twitter and Facebook figure out what to show when you share a link?
meta-image: /examples/processing/using-objects/images/eyes-5.png
published: false
---
 
When you share a link to Twitter or Facebook, do you ever wonder how it knows what thumbnail and description to use? How does it know whether the page contains a video? Have you ever noticed that some websites seem to have better-looking links when you share them?
 
For example, this is what it looked like when I shared last week's blog:
 
And this is what it looks like when I share this blog:
 
Where are those images coming from? How does it know the title and description?
 
## Hmm, I wonder how this works...
 
I had a vague idea that Twitter and Facebook must be doing some kind of scraping, where they send out bots to read the page and report back this information. But how do those bots choose the thumbnail and description?
 
One of the coolest things about programming is that you can start pulling on the "hmm, I wonder how this works..." thread and discover all kinds of interesting stuff going on behind the scenes. So after a little bit of Googling, I found out the basics: both Twitter and Facebook send out bots that look for specific [meta tags](http://www.w3schools.com/tags/tag_meta.asp) in a webpage's html.
 
Human beings never see these meta tags. But they allow me as a webpage author to let Twitter and Facebook know more about how links should behave when people share them.
 
For example, Twitter uses [Twitter Cards](https://dev.twitter.com/cards/overview), and here is what the meta tags for this blog page look like:
 
```html
 
```
 
Which generates this when you share this page on Twitter:
 
Similarly, Facebook uses [Open Graph](https://developers.facebook.com/docs/sharing/webmasters), which looks like this:
 
```html
 
```
 
Which generates this when you share this page on Facebook:
 
## Too Much Freedom
 
These tags allow you to do all kinds of cool things, like embedding parts of your website into other websites. This is how YouTube links are automatically shown as videos, for example. So I spent a little too much time trying to figure out exactly what our links should look like. Maybe they should show small thumbnails instead of big thumbnails?
 
![small thumbnail]()
 
I also spent a little too much time reading the recommended best practices for these tags.
 
But in the end I just decided to go with a standard 600x300 thumbnail for each page. Then it was "just" a matter of going back and creating thumbnails and descriptions for every tutorial and example. This was pretty tedious, but now that it's done.. it's done! Now the site has nifty thumbnails!
 
## Nobody Notices but Everybody Cares
 
If you think this sounds like a lot of rigmarole for a tiny feature, then I mostly agree with you. A big part of me has trouble caring about this sort of thing. I got the site working, so who cares what it looks like? Who is even going to notice whether the links have thumbnails or not? And the answer is that even though nobody will really notice little things like this, people do care (even if just on a subconscious level).
 
By that I mean, the little stuff adds up. Even if you don't **notice** which font a website uses, you'll **care** if the font isn't quite right. You might not even know that you care, you'll just "feel" like you don't really like the website. That can be frustrating for programmers like me who aren't artists and have to rely on [programmer art](https://en.wikipedia.org/wiki/Programmer_art) for everything, because we'd rather spend our time on the interesting bits instead of making it look nice.
 
The problem is that if you don't make it look nice, people assume that the interesting bits are crappy too. A smarter guy than me (hi Mr. B) described this as "signalling low quality" which is probably a better way to say it. The funny thing is that I'm not sure there's a way to signal high quality: people don't notice when everything looks good, they just notice when it looks bad. So you end up spending a lot of time on stuff that, hopefully, nobody will even notice!
 
Anyway, the point is that even though this is a very small feature that I don't *really* care about, I think little things like this add up to make a website "feel" like a "real website" so I'm trying to be more intentional about things like this.
 
Oh, and this happened:
 
![CodePen sharing HappyCoding.io]()
 
If only I had finished the meta tags before!