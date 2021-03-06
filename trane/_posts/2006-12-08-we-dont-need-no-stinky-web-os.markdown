---
layout: post
title: "We don't need no stinky web oS"
permalink: "/trane/2006/dec/08/we-dont-need-no-stinky-web-os/"
tags: [webdev python]
categories: [trane]
legacy_id: 1
date: "2006-12-08 -0300"
---
An operating system that you can run from your browser: launch applications and work on your files. The idea seemed straight forward.
So I've tried youos and wasn't impressed. I played with it a little and lost interest. I figured I just didn't spend enough time on it, maybe another time I'll come back to it and "get it".

Fast forward a couple of months and I was involved in a project that had a small team, 5 or 6 people, that had to exchange (and share) quite a few documents: email, calendars, spreadsheets, textfiles - the usual stuff for non techies. We shared everything with google's apps to manage our workflow. Then it hit me: we don't need a web os. 

##What good is an operating system for?
I am going to use a lax definition of an operation system: kernel + drivers + user land general utilities. In a general way what would be called a stripped down Linux distro or a Microsoft Windows install. A X window system and a window manager would be included inside this definition.

Generally speaking an os is useful for:

1. Interfacing with hardware: IO operations: This means that every developer doesn't have to worry how track move positions for every mouse maker model, or keys pressed on a keyboards, or how to display graphics for each kind of video card.
2. Storing data: though the file system, an os allows user to store , manage and retrieve their data (and launch applications too)
3. Providing facilities for applications developers to build upon, like Cocoa on OSX. 

But the more you look carefully to the way web applications work, to how users use them (and will use them), the less an idea of a web os makes sense.
Point 1 is the easier to dismiss: if you can log into an web os on a browser, all that stuff is already taken care of for you (reading from the keyboard, mouse, showing graphics on screen, and so forth).
There are quite a few ways to dismiss point 2 such as WEBDAV. But actually the focus on file storage is probably mostly an artifact of not having a good server / client architecture. Your documents, your data only make sense if you use it with an application (or a few of them), so let each application take care of keeping it's data for you. This is how many applications work: let iTunes organize you music files, let Thunderbird keep track of your emails without you even knowing where / how they are stored, let the browser keep track of cookies or browsing history. It doesn't (and shouldn't) matter if the browser stores cookies on files or in a database, if they are in plain text or binary. 
As long as it works it's not the user's problem. Users shouldn't have to think about files, it's a convenient abstraction for system developer's  but it's lame for users, users need data, not files. How and where those are stored are irrelevant as long as applications provide practical ways to process and exchange information.

Point 3 will be solved by the combination of two things: frameworks and webservices. Frameworks can be linked to server and client code. You might provide RSS feeds by using a common library for parsing and generating rss, such as the excellent feedparser. You may also use framework for common gui widgets such as calendars and checkboxes, like [yui](http://developer.yahoo.com/yui/). Through webservices apis you can exchange, import and consume data coming from different places. I keep bookmarks on my del.icio.us account, but consume them from the provided api to replicate them on this website. I also use my [flicker account](http://www.flickr.com/photos/bananal/) to store all my relevant photos, and send the to [tabloo](http://www.tabblo.com/studio) to make posters. 

##Are we arguing about names?
I am not sure about this one. Each year more and more applications become web based. And each year it becomes easier to make our data go from one place to the other and back, it's not about the applications, it's about the data. 
When Sun says "the network is the computer" (and it has been saying that for over 20 years now) it is referring exactly to this. Maybe we can call the whole ecosystem of web applications as the web-os, but that would be just for the sake of using a familiar term, the convergence and communication of apps through the web is very different from a desktop OS both from the user perspective and from the developer, we could use a new name just as well.

##This sounds good in theory but in practice...
We are pretty much in a transitory stage right now. The transition from the desktop world to the web world has begun only a few years ago and it will take some time until we have a more established way of doing things. It's still early and there are many questions unanswered: we'll we use REST, atom, SOAP or some combination of these ? How do all these apps exchange data? What about user's privacy and security? We'll we be just replacing vendors lock-in: from Microsoft to Google? 
There are many open questions, but little by little we are drawing the landscape that will make possible for people to forget (mostly) about local applications, platforms and files , soon enough all you'll see is your data.

I might be wrong, maybe youos and other web based operating systems will prosper and I will have to eat my words. But from all I can tell, we are moving towards a much less decentralized, much more distributed scenery: many applications running on many different places and all you care about is that is keeps your data safe and accessible.