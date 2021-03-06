---
layout: post
title: "Loading Reloaded"
permalink: "/trane/2007/nov/25/loading-reloaded/"
tags: [actionscript bulk-loader opensource]
categories: [trane]
legacy_id: 19
date: "2007-11-25 -0300"
---
Controlling loading is tedious, error prone, and each projects has such specific requirements that you end up rewriting loading code. A lot. In my last project I spent 4 hours debugging download code and promised my self I would solve this annoyance once and for all. So in the best \"let me be lazy\" fashion, I decided to write my final loading code.

Everybody has been there, and there are many classes around to manage loading, but I\'ve never found one that was complete, flexible and easy enough to use. AS3 has created some kind of loading hell: so many classes to import and understand, a plethora of listeners, the need for error handling and the new API objects (Bitmap, DisplayObject) have added more corner cases to remember. Worse still, videos are still left in some twisted logic maze.

[BulkLoader](http://github.com/arthur-debert/BulkLoader/) is my shot at trying to unify the most common cases for loading management into a reusable library for AS3. 

It is licensed under an open source MIT license. Features: 

   - Unified interface for different loading types.
   - Unified progress notification.
   - Events for individual items and as a group.
   - Priority.
   - Stop,resuming and removing individually as well as in bulk.
   - Configurable number of maximum connections.
   - Cache managing.
   - Statistics about loading (latency, speed, average speed).
   - Multiple kinds on progress indication: ratio (items loaded / items to load), bytes, and weighted percentage.
   - Multiple number of retries.
   - Configurable logging. 
   - Video: meta data storage, streaming as soon as connection is open, sane progress handling.
   - Helpers for different kinds of contents
   - Easy memory management (releasing objects)
   - Connection pooling.

Design goals:

   - Minimal imports.
   - Few method to learn.
   - Dynamic nature: items can be added by specifying a url as a String or a URLRequest .
   - Items can be assigned an identifier key to be used on retrieval.
    
At a glance:

    var loader : BulkLoader = new BulkLoader("main");
    loader.add("bg.jpg");
    loader.add("config.xml");
    loader.add("soundtrack.mp3");
    loader.add("intro.flv");
    loader.addEventListener(BulkLoader.PROGRESS, onProgress);
    loader.addEventListener(BulkLoader.COMPLETE, onComplete);
    loader.start();

    function onProgress(evt : BulkProgressEvent) : void{
        trace(evt.percentLoaded);
    }

    function onComplete(evt : Event) : void{
        var bgBitmap = loader.getBitmap("bg.jpg");
        addChild(bgBitmap);
        var video : Video = new Video();
        video.attachNetStream(loader.getNetStream("intro.flv"));
        parseConfig(loader.getXML("config.xml"));
    }

The above code in 8 lines:

- adds 4 items with different typed to be loaded: xml, mp3, flv, jpg.
- created listeners for progress notification and when all items are done.

I needed a class that:

- Would wrap up errors elegantly: retries and no errors on browser tabs closed.
- Progress that works with many simultaneous items and many simultaneous items of very different sizes
- Would let me use (and let me know) as each item was ready, and would allow items that can be streamed (video, sound) to be consumed as soon as possible.
- Would treat video as any kind of asset.

I am pretty happy with the results. I feel BulkLoader strikes a good balance between ease of use, flexibility and power. At [work](http://www.gringo.nu/) we\'ve used it in a few projects, and users like it. 

The thought of managing multiple loadings by hand again makes me shiver. It\'s the same feeling I got when I started to use a tweening library.

The project is hosted at github. Right now, I believe it\'s very close the final API. Mostly bug fixes and other enhancements. 
## Links:

- project home at [github](http://github.com/arthur-debert/BulkLoader/)
- [the issue tracker](http://github.com/arthur-debert/BulkLoader/issues): if you find a bug, please let me know and I\'ll get it fixed asap.
- An [online doc](http://media.stimuli.com.br/projects/bulk-loader/docs/). 
- The WIKI [developer guide](http://github.com/arthur-debert/BulkLoader/wiki/). 
- The [discussion list](http://groups.google.com/group/bulkloader-users).

## Thanks to:

- Igor Almeida: my coworker who has been a thorough beta tester. A couple of months ago he wrote a loading manager class that, while has little resemblance to BulkLoader, provided many insights and a good road map of what  works (and what doesn\'t). Igor reported bugs and gave a lot of feedback on features and ideais.
- [Zeh](http://www.zeh.com.br/): in long emails Zeh has given valuable ideas and discussed a few key issues. Having Zeh give you design ideas is (to steal a phrase from [Paul Graham](http://www.paulgraham.com/)) like having Mick Jagger playing on your son\'s Bar Mitzvah.'