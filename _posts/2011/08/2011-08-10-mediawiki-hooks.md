---
title: "MediaWiki Hooks"
date: 2011-08-10 22:55:28 +0000
external-url: http://www.mediawiki.org/wiki/Manual:Hooks
hash: c8878ebd1829ef1fb57436285ad53d01
annum:
    year: 2011
    month: 08
hostname: www.mediawiki.org
---

MediaWiki provides many hooks that can be used to extend the functionality of the MediaWiki software. Assigning a function (known as an event handler) to a hook will cause that function to be called at the appropriate point in the main MediaWiki code, to perform whatever additional task(s) the developer thinks would be useful at that point. Each hook can have multiple handlers assigned to it, in which case it will call the functions in the order that they are assigned, with any modifications made by one function passed on to subsequent functions in the chain.