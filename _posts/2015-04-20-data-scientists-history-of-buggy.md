---
title: A Data Scientist's History of Buggy
slug: 'a-data-scientists-history-of-buggy'
date: 2015-04-20 00:00:00
categories:
  - blog
tags:
  - buggy
  - data
header: 
    image: /assets/images/buggy_course.jpg
---

I was very kindly invited to give a talk at Carnegie Mellon during the _Buggy Showcase_ (aka Design Comp) portion of Spring Carnival. For the uninitiated, ‘Buggy’ is a race held annually among CMU students since 1920. It’s part soap box derby or street luge, and part relay race. It involved finding the smallest girl you can on campus, building an unpowered carbon fiber vehicle for her, and then pushing her as quickly as possible around a park. Sometimes a video helps explain.

It’s probably 2 orders of magnitude more niche than the stuff I’ve done with Cross fit, so I’m mostly just posting it here for posterity. Here are the slides

And here are a selection of plots from the presentation.

The total number of teams participating peaked in 1990 once women’s teams were fully introduced and before the decline of fraternities on campus.

![](/assets/images/posts/participation.year_-1024x768.png)

The men’s race has been similarly competitive over the last 45 years. The top 5 finishers averaged a 5 second deficit to the winner quite regularly. The women’s field got deeper from 1985 until the mid-2000s, but has been reversing for the last 10 years.

![](/assets/images/posts/perf.margin.year_-1024x768.png)

New course records happen when the engineering, athletic, and environment come together exceptionally well. Sequences of new records or long stretches between them probably reveal periods of systematic change in the race across teams. I was particularly interested to see the 3 different kinds of record setting periods in the men’s race:

*   Constant post-war improvement in the 1950’s
*   20 years of occasional record setting from ’67 – ’87
*   big new records in both genders after a 20 year drought in 2008 and 2009

![](/assets/images/posts/comp.record.year_-1024x768.png)

Data and code available [here on github](https://github.com/swiftsam/cmubuggy-data), a front end which makes it easier to explore historic times [here on cmubuggy.org](http://cmubuggy.org/history)
