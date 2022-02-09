---
title: 'Migrating 387 data models from Redshift to Snowflake @ dbt Meetup'
slug: 'migrating-redshift-snowflake-dbt-meetup'
date: 2020-02-01 00:00:00
categories:
  - talks
tags:
  - dbt
  - analytics engineering
  - Bowery
excerpt: A talk with Travis Dunlop for the dbt meet-up we hosted at Bowery. We shared revelations from our experiencing of migrating our dbt project from Redshift to Snowflake.
---

In February 2020, we hosted the NYC dbt MeetUp at the Bowery Farming office. [Travis Dunlop](https://www.linkedin.com/in/travis-dunlop/) and I shared some learnings from our experience migrating our 387 model dbt project from Redshift to Snowflake. 

Our key points were
 - Redshift was great for the first 2 years of growth, but we were starting to spend more time managing and problem solving to keep our hourly run times under an hour.
 - Snowflake looked to be cost-competitive in a number of trials.
 - Snowflake has surprisingly weak documentation to support this transition, and in fact referenced a dbt blog post when we inquired
 - We developed a workflow to compare materialized tables from the redshift and snowflake branches and automate testing of the diff. We worked through the list of tables as a team, finding and resolving differences. This process took 40 people-days.
 - The biggest syntax differences for our codebase were
  - Snowflake has `lateral flatten` to extract JSON into rows. Nice
  - `is_null` vs `is_null_value()` distinction in snowflake for SQL vs JSON nulls
  - `least` and `greatest` behavior when the set includes nulls
  - we had relied `using` for succinct expression of joins which behaves differently in Snowflake, so we moved to stricter `on` syntax
  - Snowflake has no `infinity` timestamp which we'd used for our slowly changing dimensions

{% include video id="VhH614WVufM" provider="youtube" %}

