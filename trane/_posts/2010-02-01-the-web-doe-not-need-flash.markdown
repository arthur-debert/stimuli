---
layout: post
title: "The Web does not need flash."
permalink: "/trane/2010/feb/01/the-web-doe-not-need-flash/"
tags: [flash ipad html5 future web ]
categories: [trane]
legacy_id: 32
date: "2010-02-01 -0300"
---
With the iPad launch, the lack of the Flash runtime has received a lot of slashback. This gave me the opportunity to gather a few thoughts on Flash, and where it is going. I've seen a lot of hate from people who don't know much about Flash, and also a very defensive and blind reaction from inside the Flash world. I wanted to give a different perspective.
A few disclaimers:

- I am not a known name in the Flash community, but I am not a Flash hater either. Actionscript is the language I've programmed the most. I've made my living primarily out of it for 5 years or so. In fact I keep two open source Actionscript projects( [BulkLoader](http://code.google.com/p/bulk-loader/) and [printf as3](http://code.google.com/p/printf-as3/)) and have contributed to [others](http://code.google.com/p/tweener/).
- Technologies come and go, but their effects  linger on for quite a while. COBOL is dead for any intended purposes, and has been dead for 20 years. But still, there is a lot of people making a living from it. Same thing with Microsoft. Microsoft is still huge and will remain so for quite some time. But neither of these are relevant for the future tech landscape. They are not dictating new directions. They're influence and usage will only decrease, not increase.
- I'll call Macrodobe initiatives for lack of better judgment. I don't know in detail (nor intend to) which were started at Macromedia, Adobe or both.
- I am not picking on the FWA itself. It's a great site, and has been invaluable to the community. I've worked on a few projects featured on the website, and I'm always proud to be there.
- I have no illusions regarding Apple's stance for blocking the flash player. It's a dog eat dog world. Adobe is not a saint either. [Alex Payne](http://al3x.net/2010/01/28/ipad.html) post hit the mark. I am not a fan of walled gardens either.

With that said, I think Flash is marked for a sharp decline in importance, and has been so for quite a few years. It's inevitable. The current situation with the iPad and HTML5's video capabilities are only the harbingers of it's decline.

## The rise of Flash:
HTML was invented to solve a very different problem than what it has been put to in the last few years. That mismatch meant that there was a large demand for capabilities it didn't possess. Flash made it's rise out of these major gaps on the web technologies of the day, namely:

- (1) Static content:  visual animation. When Flash appeared, the best you could do for animation was a GIF.
- (2) Interactivity: HTML was though of a document format. Until 2004 or so, with the raise of Ajax, web pages had zero interaction (except for forms). Flash offered an answer to that.
- (3) Design: again, HTML was never though as a presentation format. Until CSS came along, it was very messy to control HTML visually with some sophistication. Even now, with all the browser compliance differences, it's not easy to control pixel perfect the visual layout. Regarding fonts, HTML has no great solution yet.

Later on, Macrodobe was very clever to move Flash to new pastures:

- (4) Audio
- (5) Video
- (6) Advanced bitmap manipulation
- (7) Video recording
- (8) Sockets, for real time messaging.
- (9) Local storage

Until 2004 or so, Flash was the only good alternative to all of those. In that context, yes, the only way to make 'rich' applications (an ill defined term, but still), on the web was to use Flash. And then came video. Video helped spread Flash like wildfire. The prior options such as Quicktime, WMP were a mess: too many codecs and the download took forever.

If you look to the traditional web dev community, all of those issues have been, one by one, tackled. Static content, Interactivity and Design are pretty much solved with the advances in standards, the improvement in Javascript runtimes and the massive options of open source libs. Not literally. Flash can still exhibit greater visual freedom than HTML + CSS, but it's good enough for most use case. See 'worse is better'. For 95% of the web properties, standards are efficient solution to those. Have you ever seen someone says they don't user Facebook because the typography is boring?

For issues 4 through 8, HTML is catching up. These will take a while to be widespread and reliable, but it's inevitable. They are coming, all but #7. Video recording is a niche market. It won't dictate the direction the web is going by any means.

The big picture is that Flash was the only viable alternative to work around many of HTML's short comings as a document format. But webapps have become mass produced and mass consumed. The standards committees move slowly, but it has make steady progress. Each year one of Flash's unique capabilities get a reasonable alternative.

## Understanding the hate.
Flash is a strange beast, because of it's unique origin. It was it an animation tool, then a design tool, then an interactive environment than a platform. While been mostly proprietary most of the time. The net result is that the Flash community is somewhat disjointed from the general web dev community. There is some overlap on the larger web , but there is a great divide. It's hard for people to understand where all the Flash hate comes from. The main forces between Flash hate are:

- Religiousness. Yes, there is a small but very vocal group of OSS zealots. They've always criticised Flash on the basis of it been a proprietary technology alone. While this group is very loud on the blogosphere, it's not a driving force for most companies. Businesses tend to be pragmatic.
- Pragmatism. Lack of support for various platforms. Adobe has improved recently, but the fact is that many platforms (64 bits, freebsds) are or were totally neglected for a long time. Again, these were not a large number of users, but they are very loud. With the diversity of devices coming up (mobile, pads, car panels, talking toaster, whatever), this will only get worse. It will be hard for Adobe to keep stable and usable versions of Flash on the wide range of platforms yet to come. Many companies are not keen on depending on Adobe alone.
- Advertising. If you exclude video, an enormous amount of Flash work revolves around advertising. Be it the ads themselves, or campaign micro sites. Just take a look at **the** Flash showcase, The FWA, and take note of how many are marketing campaign. Folks are not very hot about ads on the web, specially the rich media, processor consuming ones. Those are precisely the ones in which Flash prevails. They've simply conflated hate for the delivery medium with the message. Oh well.
- Disregard for UI and web conventions. As a case in point, I'll take the FWA website as an example, as it's one of the most important websites in the Flash world. It's basically a data grid, with a simple filtering, and a small detail pane for content (agencies, sites). To this day, there is no way to send a direct link to a campaign or anything else but interviews. It's nuts.  
In the name of exercising more control over the visual design, the FWA makes it awfully hard to use it other sites on the web. Upon a closer inspection where is the rich application? It's basically text, lists and thumbnails. I don't mean to pick on the FWA by itself, it's just that it's really makes it easy make the point. It's a well made, high profile, commercial site within the community. It's the poster child for what was discussed above. Six years ago, Flash was the only viable way to deliver such an experience. But now, that could be achieved easily with regular web technologies.  
Yes, you can do deeplink in Flash. But the amount of work would be enormous (hint hint: if it's that easy to do, why isn't it done by now?). HTML's structure is a pretty good fit for it.  
And don't get me started on the crazy non standards UI controls, scrollbars, the lack of any sane tabbing on input elements. And that the browser cannot offer you an auto complete option for your email address. The keyboard focus is funky. Almost all of these an be done in Flash, but it's a lot of work. By the time you're done getting everything to work as people expect you've spent much more time than HTML would have taken. Just look at most Flash websites. They tend to get it wrong, precisely because it takes a lot of work to get it right. I cringe on the though of how many hours of my life I've spent coding scroll bars with quirky behaviors. The flip side of it, is that blindly following all pre-established UI conventions is not the way forward. While the experimentation is surely welcome, most UI improvements I've seen in the past years have come from games, other web apps (auto-complete boxes) and Apple. I for one am yet to see a use for 3D video or interfaces outside of gaming and simulations.
- Self centered. This one is pretty shocking to me. Of all the websites and apps I use regularly, Flash is only used for video / audio. Campaigns are a tiny niche. Just to give you an idea a, again, the FWA,  which is among the most visited Flash sites, ranks number #17,216 on Alexa. Newgrounds with its massive user base: 719th.  
Most Actionscript programmers I know show very little understanding that their niche is almost as small as Lisp, Scheme and much smaller than COBOL. To add insult to injury, most designers on the Flash space have little or no knowledge of HTML or the web. For years the flash world appeared to find plain old HTML to be ugly and boring.

That said, much of the hate geared towards Flash is either misguided (it's the ads, not the plugin!) or uninformed, or no longer valid. But still, those cultural artifacts take a while to disappear. 

## The web will be everywhere and in anything. Soon.
Macrodobe has had great success getting the Flash player to be installed in every computer. Their figures show over 96% penetration. Except now we'll witness the web coming into so many devices, in many form factors : phones, pads, car dashboards and a whole lot more. We are just at the beginning of this path. Most of those devices will be very constrained in their capabilities, namely, CPU. 

Unless Flash is utterly needed , many of those will not support it. Adobe has been working hard to get Flash running on all these platforms, but it will only get harder. If you're making a device, you can simple use Webkit. It is opensource, has a very readable code base, is actively developed  and you can tailor it to your device as you see fit. The entry price for supporting the web on your device is pretty manageable now. On the other hand, getting Flash to work requires the good will of Adobe, and might be hard to fit within  your hardware limitations. Resources are limited: manufacturers will always privilege regular HTML first. 

On the cutting edge front, the pressure to add more hardware support makes it tough on the player engineering. How can you compete with a game for the iPhone written in OpenGL? Not only the amount of platforms will increase, but allowing for greater access to the hardware makes it impossible to support them all. At this point, Unity 3D is pretty far ahead of the graphic processing you can deliver real time through a browser. Flash is second rate on CG. I remember rendering things at 30 fps in Director with a 384MB of RAM pentium 4 that I can not do at 15 fps with todays machines. This was 7 years ago.

## Strategic mistakes.
It seems that all those forces were inevitable, but in hindsight, some of Macrodobe's strategies seem harmful

- Licensing the plugin for mobile platforms. This probably withheld adoption greatly. There was a good article on the subject floating on tweeter some time ago. Too lazy to find the URL for it now. Right now it seems crazy that manufacturers would pay Adobe to have their technology running, but this is the strategy Macromedia pursued for a while.
- Batshit crazy naming. Flex? Flash? Flash MX? BlazeDS? AS3? Flex sdk? MXMLC? I still talk to people who make a living out of Flash that can't tell a difference between all of them. Every now and then there I get bug report for BulkLoader saying it doesn't work with flex. Also a very poor job communicating what the platform is like exactly, what pieces are open or open sourced and so on.
- The open source strategy was late, and was poorly executed. Till this day: how many people, outside of Adobe has contributed patches to the compiler, or asdoc (which is a mess, by the way). Why do I have to register at Adobe's Jira to search for bugs? Why most bugs have very little information, or link to issues or fixes in their internal system? It's a maze out there. 
- Using On2 codecs which hindered common tools incapable of generating content.  The enormous delay on releasing specs in a sane manner. Remember the crazy agreement people had to agree to before reading SWF's specs?).
- The awful tools. The Media Encoder that comes with Flash Professional. The code 'editor' on the IDE. The compiler written in Java that takes forever to start up. The control panel for administering FMS. FlexBuilder is buggy as hell. Would you like to compare the Flex Profiler (+500 dollars) to [Google's speed tracer](http://googleblog.blogspot.com/2009/12/faster-apps-for-faster-web-introducing.html)? Or the [Apple's intruments](http://www.apple.com/macosx/developers/#instruments)?
- Pricing. Call me crazy, but the market for expensive development environments died years ago. Remember Borland? The only large player in that space is Microsoft, which is by the way a weaker player on the web. People do not want to pay $500,00 for development tools, nevermind inferior ones.  
- What's the deal with Director? Why won't they kill it? Why split the development community? I am not convinced that there was nothing on the rendering pipeline that Flash couldn't take from Director. Director had such a great performance for it's day.
- Bugs, bugs bugs. Before player 9, I only stumbled once with a crashing bug on the player. Only once. I don't know what it is: the increasing hardware support, or the more aggressive vm, but all players since have become much more prone to ugly crashes. This has really hurt Flash's reputation. Didn't it make sense for Adobe to pay a team and get Flash running extremely well on Chrome (specially on osX), this has been, for a while their last problem to release Chrome on the Mac. All the 20 or so last projects I've been involved, we always found a bug specific to a platform under a certain player revision. Our test grid became hell.

Bottom line is that I am sympathetic to Adobe's position. It's damn hard for large companies to play the open source game. But Macrodobe hasn't handle it well at all. This contributed to putting Flash into a corner.

## Niches.
After all the iPad ordeal, Lee Brimelow has published a [witty post](http://theflashblog.com/?p=1703), showing what the web looks like without Flash. It was a smart move, but there are somethings to be said about it. Much of those do rely on video. Once HTML has that working , those will be fixed. Some are real niche websites (FWA, Aviary). Google finance could be done in Javascript (it won't take long, rest assured). Of those examples, the only one's where blue legos will be an issue are the games / gamish ones. Right now, gaming is the one space where HTML doesn't have a solution. This is **the one** niche where it will be very hard to displace Flash. That said, it's possible that some of that market will be directed to more established gaming technologies, like OpenGl, adapted for each platform. Looking at Apple's App Store catalog, there is a thriving market of games there. Gaming companies don't seem to mind using traditional gaming tech: C, C++ and OpenGl. The other thing to keep in mind, is that if those devices that lack Flash prosper, those sites will adapt their content.


Note, however, that there's nothing wrong in being a niche tech. Objective-C was a very small niche until 2 years ago (and it's still is). A lot of people hacked good software with it, and made a good living doing so. Maybe it's just natural that flash will fill a niche, since mainstream will be provided for by HTML. The truth is, most of the things Flash excels at are beyond day to day need of most people.

## Wrapping it up
Most features that set Flash apart have viable alternatives right now, or will soon enough. The final pieces are being worked on, and will, in time, be solved.

On the other hand, new devices and markets will make it harder for Adobe to keep the player with a large installed base. Once flash looses it's installed based, less content will be developed, which will in turn lower the adoption further. Just look at how hard it was for Silverlight to get mass adoption, even with Microsoft's muscles behind it. 

If you think about it, most proprietaries browser technologies are either dead or dying. Remember applets? RealVideo? Shockwave? Authorware? iPix? The 'plain' web has eaten their lunch.

Make no mistake, Flash's days are numbered.

### What the future holds (for me at least)?
The thing to keep in mind is that this movement will be slow and gradual. Will there be sites using Flash next year? Absolutely. Will you be able to work on Actionscript for years to come? Sure. But in 5 years or so it will decrease sharply. Probably earlier than that, but I don't care about predicting the right date. It doesn't matter. What I am saying is that soon the market for Flash developers will decrease, and it will do so consistently. There will be many legacy applications that will require Actionscript programmer for years to come. Also there will probably be niches where Flash will remain king. People still use Director for some things. But again and again, Flash will decline. If you haven't, go read it now [Worse is Better](http://www.jwz.org/doc/worse-is-better.html). It's required reading for any programmer, but it fits Flash's predicament like a glove. HTML is worse, Flash is better.

As developers it's a smart move to be prepared. I am not married to one platform. I want to work within the web, making tools for people to communicate, interact, discover and get things done. If it's HTML + CSS + Javascript, so be it. If it's Objective-C, python or Java, it's O.K. as well. I'd say that expect to be doing FLash work for 3 or 4 years from now.

Predicting the future is always a waste of time. Maybe Adobe will find new killer features to put into the runtime, buying the platform more time. Maybe Moore's Law will be back on track, and all those tiny devices will get insanely beefy processors next year, and Flash will be viable once again. I'll be watching closely. I am not an Adobe shareholder. I **do** have, however, vested interest in the years spent on Actionscript, but programmers should always work on more than one platform. Look into the history of our profession. Programmers have had to adapt to new technologies in the past 50 years. This isn't about to change.