---
published: false # work in progress
layout: post
title:  "Simple Linear Regression for the Uninclined"
---

# Motivation
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**We don't know how to effectively teach math.**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This is not news, a particularly interesting statement, or an excuse for those of us who would prefer to blame our mathematical shortcomings on a 'system' that has failed them (though this does occur, I am sure). So why state it at all? Because in my (very) brief time attending the University of Washington I have seen this problem continue to go unsolved. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Let's say that you're enrolled in a program whose application process was holistic--even if your past course-load isn't entirely in line with what the program's degree plan assumes you know, other parts of your application may pick up the slack, so to speak. This is done in an effort to enroll a diverse cohort each year into a given program who can provide unique, valuable perspectives to the classroom; and it's a great effort at that. Now, for no reason at all, let's assume that this program is epidemiology, where you're required to take biostatistic courses that can, at times, be mathematically challenging. If you're coming from a soft-science, history, philosophy, or other non-mathematically-involved undergraduate program, how can you be expected to be prepared to have strange letters and symbols thrown at you at the rapid pace of a quarter system? 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I believe that there is a great deal of practical value in just wanting to know what you need to know when it comes to regression models. For many in this field, simple linear regression, multiple regression, and *maybe* (and I truly do stress this maybe) ANOVA models will suffice to be a successful epidemiologist. The mathematical theory and proofs are not useful, informative, or productive to dive into and learn. That is the reality, and as such I hope for this to be a good primer 




# The Basics
---
## Linearity
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;When you think of linearity, what is the first thing that comes to mind? Time, for example, is linear (and also relative, but that's a topic for physicists to stress about); that is, you're always progressing from the past to the future at a literally constant rate. Wages are also linear; if you earn minimum wage in Texas ($7.25 in 2025) and work exactly 40 hours per week, you will make exactly $58 per day and $290 per week that you work. This is considered a linear relationship, because the change in money earned is the same from hour 1 to hour 2 as it was from hour 0 to hour 1.(**Figure 1.1**)

#### Figure 1.1
![Figure1.1](assets/img/Figure 1.1.png)

This relationship is what the **slope-intercept form** (*y = mx + b*) equation represents. There are two properties that we should recall from this elementary (but very powerful!) equation:

1) When *x = 0*, we have that *y = b*, which is called the x-intercept. For some real-world applications, such as the one seen above, when *x = 0* then *y = 0* (you can't earn negative money, but definition).

2) *x* is also called the *slope*. You might remember the saying "rise over run", which is all the slope is: to get from one data point to the next, how much do we have to "rise" (what is the change in *y*), and how much do we have "run" (what is the change in *x*). Again using the wage example, the slope is *7.25/1*, because for each hour worked (the *x*) we earn $7.25. 

## So why (simple) linear regression? 
There are a few big reasons why linear regression is as popular as it is. 

1) It's flexible (more on this later)

2) Very well understood (i.e., good documentation. Tons, in fact)

3) Easy to interpret (relative to other models and statistical methods)

4) Building block for more general models

Also, what are they used for? 

1) Study association between a single response (a single *y*) and predictor (*x*)

**or**

2) Predict the response value given the values of the predictor

## How to (broadly) interpret the model
