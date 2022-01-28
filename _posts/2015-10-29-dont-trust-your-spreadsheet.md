---
title: 'Modern Data Analysis: Don’t Trust Your Spreadsheet'
slug: 'dont-trust-your-speadsheet'
date: 2015-10-29 00:00:00
categories:
  - blog
tags:
  - data
---

_This post was originally published [on the Betterment blog](https://www.betterment.com/resources/modern-data-analysis-dont-trust-your-spreadsheet/)_

- Companies are innovating and improving the craft of using data to do business.
- Companies like Betterment are hiring data scientists and analysts who use software development techniques to reliably answer business questions which have quickly expanded in scale and complexity.
- To do good data work today, you need to use a system that is reproducible, versionable, scalable, and open.

Just as the Ford Motor Company created efficiency with assembly line production and Pixar opened up new worlds by computerizing animation, companies now are innovating and improving the craft of using data to do business. Betterment is one of them. We are built from the ground up on a foundation of data.

It’s only been about three decades since companies started using any kind of computer-assisted data analysis. The introduction of the spreadsheet defined the beginning of the business analytics era, but the scale and complexity of today’s data has outgrown that origin. To avoid time-consuming manual processes, and the human error typical of that approach, analytics has become a programming discipline.

Companies like Betterment are hiring data scientists and analysts who use software development techniques to reliably answer business questions which have quickly expanded in scale and complexity. To do good data work today, you need to use a system that is reproducible, versionable, scalable, and open. Our analytics and data science team at Betterment uses these data best practices to quickly produce reliable and sophisticated insights to drive product and business decisions.

### A Short History of Data in Business
First, a step back in the business time machine. With VisiCalc, the first-ever spreadsheet program, in 1979 and Excel in 1987, the business world stepped into [two new eras](http://www.businessinsider.com/how-microsoft-excel-changed-the-world-2010-12) in which any employee could manage [large amounts of data](http://www.npr.org/blogs/money/2015/02/25/389027988/episode-606-spreadsheets). The bottlenecks in business analytics had been the speed of human arithmetic or the hours available on corporate mainframes operated by only a few specialists. With spreadsheet software in every cubicle, analytical horsepower was commoditized and Excel jockeys were crowned as the arbiters of truth in business.

But the era of the spreadsheet is over. The data is too large, the analyses are too complex, and mistakes are too dangerous to trust to our dear old friend the spreadsheet.

Ask [Carmen Reinhart and Kenneth Rogoff](http://www.nytimes.com/2013/04/19/opinion/krugman-the-excel-depression.html), two Harvard economists who published an influential paper on sovereign debt and economic growth, only to find out that the results rested in part on the accidental omission of five cells from an average. Or ask the execs at JPMorgan who lost $6 billion in the ‘London Whale’ trading debacle, also due in part of poor data practices in Excel.

More broadly, a 2015 survey of large businesses in the UK reported that 17% had experienced direct financial losses because of spreadsheet errors. It’s a new era with a new scale of data, and it’s time to define new norms around management of and inferences from business data.

## Requirements for Modern Data Analysis
Spreadsheets fundamentally lack these properties essential to modern data work. To do good data work today, you need to use a system that is:

### Reproducible
It’s not personal, but I don’t trust any number that comes without supporting code. That code should take me from the raw data to the conclusions. Most analyses contain too many important detailed steps to plausibly communicate in an email or during a meeting. Worse yet, it’s impossible to remember exactly what you’ve done in a point and click environment, so doing it the same way again next time is a crap shoot. Reproducible also means efficient. When an input or an assumption changes, it should be as easy as re-running the whole thing.

### Versionable
Code versioning frameworks, such as git, are now a staple in the workflow of most technical teams. Teams without versioning are constantly asking questions like, “Did Jim send the latest file?”, “Can I be sure that my teammate selected all columns when he re-sorted?”, or “The bottom line numbers are different in this report; what exactly changed since the first draft?”

These inefficiencies in collaboration and uncertainties about the calculations can be deadly to a data team. Sharing code in a common environment also enables the reuse of modular analysis components. Instead of four analysts all inventing their own method for loading and cleaning a table of users, you can share as a group the utils/LoadUsers() function and ensure you are talking about the same people at every meeting.

### Scalable
There are hard technical limits to how large an analysis you can do in a spreadsheet. Excel 2013 is capped at just more than 1 million rows. It doesn’t take a very large business these days to collect more than 1 million observations of customer interactions or transactions. There are also feasibility limits. How long does it take your computer to open a million row spreadsheet?  How likely is it that you’ll spot a copy-paste error at row 403,658? Ideally, the same tools you build to understand your data when you’re at 10 employees should scale and evolve through your IPO.

### Open
Many analyses meet the above ideals but have been produced with expensive, proprietary statistical software that inhibits sharing and reproducibility. If I do an analysis with open-source tools like R or Python, I can post full end-to-end instructions that anyone in the world can reproduce, check, and expand upon. If I do the same in SAS, only people willing to spend $10,000 (or more if particular modules are required) can review or extend the project. Platforms that introduce compatibility problems between versions and save their data in proprietary formats may limit access to your own work even if you are paying for the privilege. This may seem less important inside a corporate bubble where everyone has access to the same proprietary platform, but it is at the very least a turnoff to most new talent in the field. I don’t hear anyone saying that expensive proprietary data solutions are the future.

## What to Use, and How
Short answer: R or Python.

Longer answer: Here at Betterment, we use both. We use Python more for data pipeline processes and R more for modeling, analyses, and reporting. But this article is not about the relative merits of these popular modern solutions. It is about the merits of using one of them (or any of the smaller alternatives). To get the most out of a programmatic data analysis workflow, it should be truly end-to-end, or as close as you can get in your environment.

If you are new to one or both of these environments, it can be daunting to sort through all of the tools and figure out what does what. These are some of the most popular tools in each language organized by their layer in your full-stack analysis workflow:

|Full Stack Analysis|R|Python|
|--- |--- |--- |
|Environment|RStudio|iPython / Jupyter, PyCharm|
|Sourcing Data|RMySQL, rpostgresql, rvest, RCurl, httr|MySQLdb, requests, bs4|
|Cleaning, Reshaping and Summarizing|data.table, dplyr|pandas|
|Analysis, Model Building, Learning|see CRAN Task Views|NumPy, SciPy, Statsmodels, Scikit-learn|
|Visualization|ggplot2, ggvis, rCharts|matplotlib, d3py, Bokeh|
|Reporting|RMarkdown, knitr, shiny, rpubs|IPython notebook|

### Sourcing Data
If there is any ambiguity in this step, the whole analysis stack can collapse on the foundation. It must be precise and clear where you got your data, and I don’t mean conversationally clear. Whether it’s a database query, a Web-scraping function, a MapReduce job, or a PDF extraction, script it and include it in your reproducible process. You’ll thank yourself when you need to update the input data, and your successors and colleagues will be thankful they know what you’re basing your conclusions on.

### Cleaning, Reshaping, Summarizing
Every dataset includes some amount of errant, corrupted, or outlying observations. A good analysis excludes them based on objective rules from the beginning and then tests for sensitivity to these exclusions later. Dropping observations is also one of the easiest ways for two people doing similar analyses to reach different conclusions. Putting this process in code keeps everyone accountable and removes ambiguity about how the final analysis set was reached.

### Analysis, Model Building, Learning
You’ll probably only present one or two of the scores of models and variants you build and test. Develop a process where your code organizes and saves these variants rather than discarding the ones that didn’t work. You never know when you’ll want to circle back. Try to organize analyses in a structure similar to how you present them so that the connection from claims to details is easy to make.

### Visualization, Reporting
Careful, a trap is looming. So many times, the chain of reproducibility is broken right before the finish line when plots and statistical summaries are copied onto PowerPoint slides. Doing so introduces errors, breaks the link between claims and process, and generates huge amounts of work in the inevitable event of revisions. R and Python both have great tools to produce finished reports as static HTML or PDF documents, or even interactive reporting and visualization products. It might take some time to convince the rest of your organization to receive reports in these more modern formats.

Moving your organization towards these ideals is likely to be an imperfect and gradual process. If you’re the first convert, absolutism is probably not the right approach. If you have influence in the hiring process, try to push for candidates who understand and respect these principles of data science.

In the near term, look for smaller pieces of the analytical workflow which would benefit especially from the efficiencies of reproducible, programmatic analysis and reporting. Good candidates are reports that are updated frequently, require extensive collaboration, or are constantly hung up on discussions over details of implementation or interpretation.

Changing workflows and acquiring new skills is always an investment, but the dividends here are better collaboration, efficient iteration, transparency in process and confidence in the claims and recommendations you make.  It’s worth it.
