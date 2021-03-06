---
layout: post
title: "AS3 Sad bits #1: Deep copying or cloning"
permalink: "/trane/2007/may/09/as3-sad-bits-1-deep-copying-or-cloning/"
tags: [as2 actionscript flash-annoyances]
categories: [trane]
legacy_id: 10
date: "2007-05-09 -0300"
---
UPDATE: This post is outdated, see:

- [original idea to use a ByteArray](http://www.kirupa.com/forum/showpost.php?p=1897368&postcount=77)
- [how to not loose type information](http://niko.informatif.org/blog/2007_07_20_clone_an_object_in_as3)
- [Darron Schall explains throughly how the [TRANSIENT] directive works and it's effects on cloning](http://www.darronschall.com/weblog/archives/000271.cfm#more)

Along with many great improvements in AS3 there are a few things that are frustrating.

While for some, a great programming language is on that has a very concise, elegant core and for others a more capable standard, some facilities really should be included in the language itself. Complex objects in AS3 are passed by reference, and it works almost all the time. At another times though, you must make a fresh new, deep copy of an object. An object where all of it's properties are unique new objects, recursively. That's why it makes sense to give developers a way to make deep copies. That's why python has the [copy module](http://docs.python.org/lib/module-copy.html). 

AS3 can make copies of objects with the ObjectUtil module. But as it's documentation says, it will work for some objects, but not for others. The documentation doesn't go into much detail of what constitutes a good clonable object. It tells us that it won't work for UIComponent objects. Why not? it will later go on and recommend the "clone" method on these objects. But the clone method is a mystery in itself: it's not defined in a root object in the display list. Some objects implement it , some don't.

In a current project I stumbled upon the need to clone NetStream instances. No dice. No clone method. Ok, so I will implement it my self. Following [this thread](http://www.richapps.de/?p=34), it seems more people have ran into this issue. The work around is to copy ByteArray.writeObject. Great! Except that you'll loose typing information, making it somewhat useless. Now you must traverse the prototype hierarchy and copy that as well.

Sure, deep copying poses some questions: circular references and large data structures, but the first one can be resolved pretty easily and the second one, just let developers decide what's too large to copy.

This came as a shock because the new display list, with it's real node tree, where you can move objects freely along the tree would benefit a lot from a powerful clone method. It's useful to really duplicate a MovieClip (with all state preserved): current frame, transforms, filters, callbacks and all. 

I'll just have to stop whining and code a well rounded class. Any finished implementations on this?