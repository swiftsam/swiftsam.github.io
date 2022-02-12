---
title: 'Using dbt in a machine learning pipeline @ dbt Meetup'
slug: 'dbt-in-ml-pipeline-dbt-meetup'
date: 2019-05-23 00:00:00
categories:
  - talks
tags:
  - dbt
  - ml engineering
  - Bowery
excerpt: How we use dbt as our feature store for most ML projects at Bowery Farming which allows for an elegant stack, predictable dependencies across code bases, and quick development.
---

In May of 2019, I gave a talk at the dbt NYC Meetup about how we were using dbt as our ML feature engineering layer at Bowery Farming. 

My main points were

- schemas in a dbt project can be described by their purpose and their relationship to up- and down-stream processes
- feature engineering for ML projects is a pain point for many teams, which choices that present tough choices
    - 1st party ML platforms: great if you've got the team for it
    - ML as a service services: SaaS lock-in, platform limitations 
    - Deploy the notebook: limited re-usability, engineering 
- We use a pattern of 3 models in our `predict` schema for batch ML models  
    - `m_[model]_obs`- 1 record per observation with features as columns
    - `m_[model]_preds` - 1 record per production inference (potentially many-to-one to `_obs`), differentiated by timestamp and model hash
    - `m_[model]` - observations joined to "current" inference for downstream use


{% include video id="dm0x9bNtO8s" provider="youtube" %}


<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vT83_uBkgjoARToUImGhD1cbPZ7C9vPjLXd3LeEEKxU0Q17yQEiqjNCrFROGPmD9tANcZeAbF_eA0xG/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>