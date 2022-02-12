---
title: 'AI farming: 100x the yield with a data team of 1 @ Data Council NYC'
slug: '100x-yield-data-team-of-1-data-council'
date: 2018-11-09 00:00:00
categories:
  - talks
tags:
  - dbt
  - ml engineering
  - Bowery
excerpt: At Data Council's NYC conference, I described how I built data ingestion, warehousing, analytics, and productionized machine learning with a team of 1 using all the best new tools. 
---

In November 2018, I spoke at the DataEngConf NYC (now called Data Council) about my work building the initial data infrastructure at Bowery Farming.  

My main points were

- The challenge in standing up a data ecosystem from scratch is "completing the loop". You've got to
    - collect the data
    - organize it all nicely
    - get it back out into the business to do something useful
- I accomplished this quickly and cheaply with 
    - AWS SNS, SQS, and Kinesis Firehose to collect messages from our application and IoT fleet
    - Redshift to store and compute
    - dbt to transform
        - differentiated `ingest` and `warehouse` schemas to do extraction and transformation work in series
- Our warehouse functions as the foundation of both our human-facing analytics as well as our machine-facing ML data products

{% include video id="chfIo1O0Cpk" provider="youtube" %}

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQwBlws_i0NOB3E_JrZlA99v16LNkqbtw_2_kzTZAHz9tKQtW-oEPaKyKAaTVKRz3LHaq-Zs-SiZikG/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>