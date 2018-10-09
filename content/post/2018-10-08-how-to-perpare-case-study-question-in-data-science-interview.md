---
title: How to Perpare Product Questions in Data Science Interview
author: Frank Zeng
date: '2018-10-08'
slug: how-to-perpare-case-study-question-in-data-science-interview
categories: [Interview]
tags:
  - Data Science
  - Interview
lastmod: '2018-10-08T01:12:48-05:00'
keywords: []
description: ''
comment: no
toc: no
autoCollapseToc: no
contentCopyright: no
reward: no
mathjax: no
---

<!--more-->

1. To think of adding a new feature:

 * If the feature were highly successful, would it be a good thing for the site? You need to find a proxy for demand of that feature in your current data.

2. To test if a feature is successful:
  * Define goal
  * Ask clarifying questions
  * Define a few metrics to measure the goal

3. Cohort Analysis: a group of people became user/customer at the same time (group by join date). Track engagement, retention


4. Check for selection bias:
 * **Self-Selection**: Specific groups of people may be drawn to taking part in a particular study because of self-selecting characteristics.
 
  * The best way around this bias is to draw from a sample that is not self-selecting. This may not always be possible of course, due to experimental constraints (particularly for studies requiring volunteers), but particular effort should be made to avoid the potential for this bias when examining different personality types. The effects of this bias are unlikely to be so detrimental if the experiment is concerned with something more constant, such as psychophysiological measurements.

5. Attrition
  * **Drop out rate** is known as participant attrition, and is most commonly seen within investigations where there is an ongoing intervention with several measurements. If participants drop out of the study in a biased way – if there is a non-random reason why this is occurring – then the remaining participants are unlikely to be representative of the original sample pool (never mind the population at large).
  * For example, a medical trial may see numerous participants exit the study if the medicine doesn’t appear to be working (or is making them ill). In this way, only the remaining (or surviving, in Wald’s case above) participants will be investigated at the end of the experiment.


6. Check for Novelty Effect. 
  * **Novelty Effect:** Users use more a product when it is new, not because it is better, but simply because it is new. As novelty ends, they will use it less. This is called **novelty effect** and often makes tests look like winners when they are not.
  * You can control for this by, in your results, subsetting by drivers for which it is the first experience. Novelty effect obviously doesn't affect new users. If a test iswinning overall, but it is not winning when comparing new users in test vs newusers in control, it is a big warning that there might be a novelty effect [**Example Question:** *"We ran a test. It won by 5%, but, after making the change for all users and waiting for a couple of weeks, we didn't see any improvement in our metric. Why?"* ].


[comment]: <> (Check if you can simply randomly split users, mentally take extreme cases. Let's say the new product has a bug and it is unusable. Or the new product is amazing and test users will use it 24/7. Will these options have any effect on the control group? If the answer is yes, you can't just randomly split users.)

6. Check on cost:
 * **Making a change on the site has some costs by itself:**
Human labor costs, such as engineering time to make the change, product manager time to documentit, customer service time in case some users get confused and reach out tocustomer service representatives with questions.

  * Another way to look at this is opportunity-cost. I.e. all these people are not working on something else with a possibly higher expected value. Risk of bugs. Whenever you touch the code base, there is a non-zero chance that something will go wrong.

7. **You can't run an A/B test for months.** So, whenever your metric needs a long time to be evaluated, you need to find a short term proxy for the long term metric. This is the point of this question as well as similar questions about long term user engagement, retaining users, or estimating customer lifetime value.

8. Avoid vanity metrics, i.e. metrics that look good,but are useless. 

  * A good way to quickly identify if my metrics are useful is: imagine a bot is creating a bunch of fake accounts. Will my metrics go up? Inthe example above, we are good. The engagement metric will drop and alert usthat something not good is going on. On the other hand, if you ONLY looked at new sign ups per day, you would be happy with the fake accounts. If they ask you for just one metric, make sure it is not a metric that a bot could improve.

9. Product growth:
  * Ability to acquire new     
  * Ability to retain current

**Final thoughts:**
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;As you break downthe metric and make assumptions along the way, try to end up in a scenario where nothing actually happened on the site, but it simply changed the user distribution. It makes much easier to give possible reasons as the last step.You can simply take a random country and say users increased there for a local marketing campaign or decreased because of a local competitor launch. It just makes easier to clearly define and delimitate the problem.
