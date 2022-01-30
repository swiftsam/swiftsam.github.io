---
title: 'What’s normal (or top 5%) for a CrossFit athlete?'
slug: 'whats-normal-or-top-5-for-a-crossfit-athlete'
date: 2015-03-10 00:00:00
categories:
  - blog
tags:
  - crossfit
  - data
toc: true
---

Ever see a 32 year old 5’10” 185lb guy walking down the street with a 32 year old 5’5″ 135lb lady and say, “Now those are some CrossFit people!”?  Well you should, because those are the most typical ages and proportions for athletes registered for the 2015 Crossfit Open.

I pulled together the data from the profiles of 245,000 CrossFit athletes participating in the 2015 Open.  Having all of these stats in one place is valuable as a reference for comparison, and interesting to see how Open athletes fill out their profiles.

One important thing to remember is that these stats are all optional and self-reported.  We’ll see some places where that results in curious patterns, but the big issue is that people likely don’t report numbers they’re not proud of.  For example, only 7% of women reported their max pull-ups, but among those who did, the average was 19.  That’s nowhere near representative, so check the number of profiles included in each stat and consider what that means about the distribution.

You’ll probably also be interested in my other CrossFit posts.

# Age

![](/assets/images/posts/crossfit_dists_age.png)

Men are a hair older, but its remarkably even actually. 54% of athletes registered for the Open are between 25 and 35. These data do not include the Masters > 55 or Teen < 16 athletes.  That’s not because I hate kids or old people, they’re just on their own leaderboard, so I need to pull them next.  This is the only required field in user profiles, so this is our only complete observation of the population.

|  Age   | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th |
| ------ | ----------- | ------- | -------------- | ---- | ---- | ---- | ---- |
| Female | 102538| 32| 21| 26| 31| 37| 47|
| Male| 142485| 32| 21| 27| 31| 37| 46|

# Height

![](/assets/images/posts/crossfit_dists_height.png)

Here’s where it gets fun. So guys, how many of you are actually 5’11” but thought it wouldn’t hurt anybody if you rounded up to 6’0″?  My estimate … somewhere around 7,000 or 5% of all men.  See that big blue spike at 6′ which sticks out of the normal distribution?  Any time you see a single value sticking out way above the shaded distribution, that’s evidence of something interesting going on.  In this case, I think it’s that being 6 feet tall is an All-American-Man’s right and sometimes he’ll take it even if the tape measure says 5’11”.  Reminds me of [this article from OKCupid](http://blog.okcupid.com/index.php/the-biggest-lies-in-online-dating/) about dating profiles.

Women actually have a curious spot too: at 5′.  That seems harder to explain as it looks like it pulls from 4’11” and 5’1″. Everybody likes a round number I guess?

| Height | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th       |
| ------ | ----------- | ------- | -------------- | ---- | ---- | ---- | ---------- |
| Female | 38694       | 65      | 60             | 63   | 65   | 67   | 69         |
| Male   | 77343       | 70      | 66             | 69   | 70   | 72   | 75|

# Weight

![](/assets/images/posts/crossfit_dists_weight.png)

The ladies like to hit 135#, and the men are happy to say 185#, both exceeding their expected frequency in the distribution.  This could be because of rounding in the self-reports or because people actually try to maintain those target weights.  Interesting that in weights, people like the numbers that end in 5s: 135, 165, 175, 185, 195, and 205 are all more popular than their round number neighbors.

|  Weight | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th        |
| ------- | ----------- | ------- | -------------- | ---- | ---- | ---- | ----------- |
| Female  | 69075       | 142     | 114            | 128  | 138  | 151  | 180         |
| Male    | 118332      | 188     | 150            | 170  | 185  | 201  | 235 |

# Clean & Jerk

![](/assets/images/posts/crossfit_dists_candj.png)

| Clean & Jerk | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th        |
| ------------ | ----------- | ------- | -------------- | ---- | ---- | ---- | ----------- |
| Female       | 24990       | 134     | 85             | 115  | 135  | 155  | 185         |
| Male         | 51568       | 224     | 154            | 195  | 225  | 255  | 300|

# Deadlift

![](/assets/images/posts/crossfit_dists_deadlift1.png)

The 400lb deadlift is the biggest statistical aberration on this page. It’s extremely motivating as most people’s biggest PR, but it’s in reach for a substantial number of Open athletes.  Women are more split amongst 200, 225, and 300.

| Deadlift | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th        |
| -------- | ----------- | ------- | -------------- | ---- | ---- | ---- | ----------- |
| Female   | 26960       | 241     | 155            | 205  | 240  | 275  | 325         |
| Male     | 55979       | 394     | 275            | 345  | 400  | 441  | 515 |

# Snatch

![](/assets/images/posts/crossfit_dists_snatch.png)

| Snatch | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th        |
| ------ | ----------- | ------- | -------------- | ---- | ---- | ---- | ----------- |
| Female | 22212       | 102     | 65             | 85   | 100  | 118  | 150         |
| Male   | 47772       | 172     | 115            | 145  | 170  | 200  | 242 |

# Back Squat

![](/assets/images/posts/crossfit_dists_backsq.png)

| Back Squat | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th        |
| ---------- | ----------- | ------- | -------------- | ---- | ---- | ---- | ----------- |
| Female     | 25945       | 194     | 125            | 165  | 195  | 225  | 270         |
| Male       | 54347       | 321     | 215            | 275  | 315  | 365  | 435 |

# Fran

![](/assets/images/posts/crossfit_dists_fran.png)

How do you crazy people do Fran so fast? It’s interesting there that we see clusters just under the salient minutes (e.g. the sub-4:00 club) but that it’s not all in one of the 10 second bins.  People strive for being sub-X minute, but then often end up with a 3:35 instead of the 3:59 we might expect after seeing the other WoDs.

Remember with Fran and the other time-based WoDs below, lower scores are better, so the 5th percentile is better than the 95th.

| Fran   | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th     |
| ------ | ----------- | ------- | -------------- | ---- | ---- | ---- | -------- |
| Female | 9543        | 6:13    | 3:03           | 4:30 | 5:52 | 7:32 | 10:22    |
| Male   | 31566       | 4:56    | 2:28           | 3:18 | 4:26 | 6:00 | 9:12 |

# Helen

![](/assets/images/posts/crossfit_dists_helen.png)

| Helen | \# profiles | Average | 5th percentile | 25th | 50th  | 75th  | 95th  |
| ------ | ----------- | ------- | -------------- | ---- | ----- | ----- | ----- |
| Female | 5320        | 11:33   | 8:26           | 9:52 | 11:12 | 12:50 | 15:49 |
| Male   | 16883       | 9:59    | 7:27           | 8:30 | 9:33  | 11:00 | 14:00 |

# Grace

![](/assets/images/posts/crossfit_dists_grace.png)

| Grace  | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th         |
| ------ | ----------- | ------- | -------------- | ---- | ---- | ---- | ------------ |
| Female | 7786        | 4:02    | 2:00           | 2:51 | 3:40 | 4:48 | 7:23         |
| Male   | 23051       | 3:26    | 1:42           | 2:19 | 3:00 | 4:01 | 6:32 |

# Filthy Fifty

![](/assets/images/posts/crossfit_dists_filthy50.png)

| Filthy 50 | \# profiles | Average | 5th percentile | 25th  | 50th  | 75th  | 95th  |
| ---------- | ----------- | ------- | -------------- | ----- | ----- | ----- | ----- |
| Female     | 3661        | 28:08   | 19:15          | 23:40 | 27:33 | 31:45 | 39:25 |
| Male       | 10546       | 25:57   | 17:20          | 21:10 | 25:00 | 29:27 | 37:53 |

# Fight Gone Bad

![](/assets/images/posts/crossfit_dists_fgonebad.png)

Cool to see in FGB that 300 is a huge goal that works for men and women.  We also saw men and women congregating at the same score in Grace (sub 3:00), but here it’s a much bigger stretch for the ladies.

| FGB   | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th        |
| ------ | ----------- | ------- | -------------- | ---- | ---- | ---- | ----------- |
| Female | 6132        | 240     | 0              | 214  | 263  | 306  | 371         |
| Male   | 15597       | 2038    | 0              | 256  | 306  | 350  | 421 |

# Pull-ups

![](/assets/images/posts/crossfit_dists_pullups.png)

This graph makes me think that pull ups aren’t entirely about strength, they’re about will and caring enough to try to set new PRs. There are no plates to load here so there’s reason people only attempt multiples of 5. If 5% of men can do 50 pullups, I bet 4.9% can do 51, but only 1% bothered to notch the extra rep.  Why not? Are you the kind of person who would push to 51 once you finally hit 50?

Women (and actually guys too), remember, pull-ups are not an exotic movement.  Everyone knows what their PR is.  More than 4 out of 5 athletes chose to leave it blank, so you’re doing better than all those … chickens.

| Pull Ups | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th |
| -------- | ----------- | ------- | -------------- | ---- | ---- | ---- | ---- |
| Female   | 7819        | 19      | 3              | 10   | 18   | 26   | 40   |
| Male     | 25416       | 33      | 10             | 22   | 32   | 42   | 60   |

# 400m  Run

![](/assets/images/posts/crossfit_dists_run400.png)

94% of people were like, “We say at our gym that it’s 400m if you run out the door, past the dumpster and turn around at 3rd street light. That’s probably not legit.  I better leave that blank.”

| 400m   | \# profiles | Average | 5th percentile | 25th | 50th | 75th | 95th         |
| ------ | ----------- | ------- | -------------- | ---- | ---- | ---- | ------------ |
| Female | 3516        | 1:28    | 1:01           | 1:15 | 1:24 | 1:37 | 2:03         |
| Male   | 12282       | 1:12    | 0:53           | 1:00 | 1:08 | 1:18 | 1:43 |

# 5k Run

![](/assets/images/posts/crossfit_dists_run5k.png)

“But my Turkey Trot 2011 time, yeah, I’ll put that in there.”

| 5k    | \# profiles | Average | 5th percentile | 25th  | 50th  | 75th  | 95th          |
| ------ | ----------- | ------- | -------------- | ----- | ----- | ----- | ------------- |
| Female | 6939        | 26:19   | 20:15          | 23:07 | 25:37 | 28:33 | 35:00         |
| Male   | 19476       | 22:54   | 18:04          | 20:10 | 22:06 | 24:42 | 30:00 |
