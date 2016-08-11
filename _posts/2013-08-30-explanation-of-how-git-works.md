---
ID: 2037
post_title: Explanation of How Git Works
author: Shwuzzle
post_date: 2013-08-30 15:06:37
post_excerpt: ""
layout: post
permalink: >
  http://localhost:8080/2013/08/30/explanation-of-how-git-works/
published: true
---
Git is a distributed version control and source code management system. It was created originally by Linus Torvalds, who also had developed the original Linux kernel. Git is one of the most popular version control systems in use today.

How does git really work behind the scenes?

Each git directory is a full repository that includes the entire history and versioning with no external dependencies (e.g. no central server). All of this git metadata is stored in a .git directory in the base of each repository directory.

Every git repository essentially consists of a simple key-value store in which all of the objects are indexed by SHA-1 hash values. These objects consist of all types of git data, including: tags, files, commits, etc. This storage unit is the object database. There are essentially 4 specific types of objects: blob (files), tree (directories), commit (links trees together to form a history), and tag (container that contains references to other objects and meta data).

In addition to the object database, git has another data structure. The other data structure is a mutable index that is used to cache information about the repository directory and the current revision that has yet to be committed.

When objects are added they are hashed and then referred to by the SHA-1 hash value. Git first computes this hash (used for object's name), next it stores the object in a directory that's name matches the first 2 characters of its hash, and finally names the remaining hash as the filename of the object. However, if a file(s) has the same hash then it won't store the same file twice. This helps to reduce the amount of space used along with the default use of the zlib library for compression. Another thing that helps to reduce the amount of space used is the use of packs. Packs contain multiple objects, using delta compression for saving space. Below are 2 examples of how objects are stored in the .git directory:
.git/objects/02/b365d4af3ef6f74b0b1f18c41507c82b3ee571
.git/objects/37/ce98f6635fa1192d85243bcaa4622537b2eb87

Git also stores some metadata in the objects. This includes the files' Unix permissions, every file revision (which are linked together to form a history), commit data (author, committer detail, timestamp, commit message, etc.), etc.

Git is primarily intended for use on Linux/Unix systems, however there are versions available for other operating systems, such as: BSD, OS X, Windows, and more. To find out more about git check out some of the links below.

External Resources:
• <a href="http://gitscm.com/">Gitscm.org - Official Website</a>
• <a href="http://gitscm.com/book">Pro Git Book - Official book (free)</a>
• <a href="http://jonas.nitro.dk/git/quick-reference.html">Git Quick Reference</a>
• <a href="http://eagain.net/articles/git-for-computer-scientists/">Git for Computer Scientists</a>