---
title: 'CrossFit Games Data 2012-2015'
slug: 'crossfit-games-data-2012-2015'
date: 2015-03-19 00:00:00
categories:
  - blog
tags:
  - crossfit
  - data
toc: true
---

# Mission part 1: Bring CrossFit data mainstream.  Success!

Part 1 in my mission to bring more data to the CrossFit Open is now a success. I always wondered why CrossFit HQ didn’t do more to bring the story of the Open to the fans and participants through its data.  Now they have.  The 4 x “M” team of Mike Macpherson and Megan Mitchell brought us the [first ever analytical piece from HQ breaking down performances on 15.3](http://games.crossfit.com/article/153-leaderboard-analysis).  It bears a striking resemblance to the analytical approach I’ve taken here in analyses of 2014, 15.1, and 15.2, and I’m happy to have made an impression.  This is CrossFit, you can’t get out to a lead and expect that nobody will catch up.  It’s better if they do.

# Mission part 2: Take CrossFit data to the next level.

I’m definitely not the only one playing with this data.  I’ve linked to some of the other interesting projects this year:

- Chris Simpkins’ [dynamic histograms with D3](http://csimpkinslatd.github.io/cf-open-2015/)
- Beyond the White Board’s [breakdowns of their data](http://blog.beyondthewhiteboard.com/2015/03/06/crossfit-open-15-2-is-14-2-workout-analysis-breakdown/)
- Harold Doran’s [super interactive shiny app](https://hdoran.shinyapps.io/openAnalysis/).

I think we’ve got a lot more skills out there but the overhead of scraping all the data is somewhat prohibitive, especially in the case of athlete profile data. I’d be thrilled if more people could contribute interesting analyses, so I thought I’d share everything I’ve collected and see where it takes us.  CrossFit has an appreciation for the quantitative approach in its genes.  Lets see if we can make it an example for other amateur sports of what’s possible.

Please let me know if you’re working on something interesting, and I’d be interested to collaborate if I have time. **If you use the data I’ve collected for something public, please just reference this post, thanks!**

# What are we working with
All data posted in .csv, zipped .csvs (.zip), and R binary (.RData) for your convenience.

- [Leaderboard scores](https://drive.google.com/drive/u/0/#folders/0B-JqrzitvsWSZ2NyM1NKd2EwRnc/0B-JqrzitvsWSfmVjY1BmQzVPblZ5WjEzVTktakt2b195ZEpLS1UxZmtDMU5iWERDZ0RFUVU), ranks, athlete_ids, and scaled designations.  2012, 2013, 2014, and 2015 to date.  2015 will be added as available.
  - fields refer to the URL parameters used by the games.crossfit site
      - division: 1= male, 2=female
      - stage: 0 = roster (all athletes who signed up), 1 = WoD 1 of that year, etc
      - score: expressed in reps or seconds
      - scaled: 0 = Rx, scaled = 1.  all NA before 2015
  - I refer to 15.1A as 15.1.1 so that the database field can be numeric
  - the scraping process is not 100% successful, so there may be a small number of missing records.  Not a problem if you’re summarizing trends.  Might be a problem if you’re doing reporting for individuals.
- [Athlete profiles](https://drive.google.com/drive/u/0/#folders/0B-JqrzitvsWSZ2NyM1NKd2EwRnc/0B-JqrzitvsWSfmVjY1BmQzVPblZ5WjEzVTktakt2b195ZEpLS1UxZmtDMU5iWERDZ0RFUVU): everything on the athlete profile pages (age, weight, affiliate, team, lift PRs, workout PRs, background, training and diet descriptives).
  - athlete profiles can change at any time.  73% of records have a retrieved_datetime field to make this less ambiguous.  The rest were scraped before I thought to do that, but were scraped in March 2015.
  - some of the profile fields are very sparse and are optionally self-reported. amateur statisticians beware.
  - some (~20%) user profile pages do not exist.  these are mostly athletes who only participated in the earlier years, but there’s no real rhyme or reason to it as far as I can tell.
- [Code (written in R)](https://github.com/swiftsam/CrossfitRankings) to scrape, compile, and analyze as a starting point