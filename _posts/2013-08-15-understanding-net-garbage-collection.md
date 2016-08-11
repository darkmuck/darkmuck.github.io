---
ID: 1959
post_title: Understanding .NET Garbage Collection
author: Shwuzzle
post_date: 2013-08-15 07:42:23
post_excerpt: ""
layout: post
published: true
---
When it comes to software and memory use there are two ways to deal with managing it, either manually or automatically. With a managed environment, such as the .NET framework, memory is generally managed automatically.

Every object is stored in memory in the managed heap. When this heap is full the garbage collector is executed and every object is looked at to see if it can be disposed of. Objects can usually be safely disposed of if they do not contain any direct or indirect references to the root of the application (global object pointers, local variables, etc.) or other objects in the application.

In .NET, objects are split into two groups: large objects (greater than 85KB or multi-dimensional arrays) and small objects. The large object heap is never really compacted, which allows for increased performance most of the time. However, this means that it also takes up quite a bit more room, thereby limiting available space in the heap for new objects (OutOfMemoryException). The small object heap is compacted and is handled a bit differently than the large heap. The garbage collector handles the small object heap in three different 'generations'. New objects are put into Generation 0 and when its full, objects not in use are disposed of and objects in use are moved to Generation 1. When Generation 1 is full then these steps are repeated and some objects are moved to Generation 2. However, when Generation 2 is full and disposable objects are removed then the garbage collector compacts everything.

For more information check the MSDN page for .NET Garbage Collection:

• <a href="http://msdn.microsoft.com/en-us/library/0xy59wtx.aspx">.NET Garbage Collection (msdn.microsoft.com)</a>
