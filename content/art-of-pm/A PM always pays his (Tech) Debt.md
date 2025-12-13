---
title: A PM always pays his (Tech) Debt
date: 2025-11-16
summary:
tags:
  - ProductManagement
description:
keywords:
  - Product Manager Portfolio
  - Product Strategy
  - Product Management
draft: false
categories:
  - Product Strategy
  - The Art of PM
slug: a-pm-always-pays-his-tech-debt
weight: 3
cover:
  image: /img/a-pm-always-pays-his-tech-debt.png
  alt: a-pm-always-pays-his-tech-debt
---
## Some Intro

Think of it this way. You started working and earning in your early twenties. You were basking in the glory of the newfound financial freedom. You wanted more, and hence you toiled, you learned the industry, learned about business and consumers, and slowly you moved up the ladder, earning more and more. But there was something that kept building up - Taxes and EMIs, responsibilities, deteriorating health and relationships, creeping up depressions and anxieties. You didn’t pay much attention to it earlier and didn’t invest properly (in health, wealth and relationships). Now they have started hurting you. Though the ==influx of wealth has grown, you are not able to enjoy it like you used to do. You want to go out and party, roam the world, and live carefree like you used to do, but things keeps pulling you back.==

This is similar to what **Tech Debt** is. You started building a product, and applied quick fixes and hacks to grow it without thinking about overall architecture and optimizations. You went on adding more and more features to the customers' (and the sales teams') likings, kept on experimenting while ignoring the health of the system. Pretty soon the health deteriorates and it’s time to pay the accumulated debt. And there you are, tussling between how much time should you need to allocate to new feature requests and how much to improve the system's health.

_PS: You can refer back to this analogy throughout this article, and also use it whenever you need to explain tech debt to the VPs. You can thank me later_ 😉

## Why is making that small tweak taking weeks?

![technical debt](https://media.licdn.com/dms/image/v2/D5612AQE8v7NBe9ULCg/article-inline_image-shrink_1000_1488/article-inline_image-shrink_1000_1488/0/1665205268216?e=1764806400&v=beta&t=UOeJkF25zCaQqyPJZwfQbiD4sbLfveANQLSiJ-3pN_k)

A picture tells a thousand words, and this picture tells an entire story, a horror one though. This is exactly what accumulating tech debt can do to your system. As a PM, you aspire to do great things for your customers, no matter if you are at a startup, finding the product-market-fit, or at a Fortune 500 company, delivering more and more value based on the market-fit.

In both cases, ==the faster you go, the more tech debt you are accumulating,== they are proportional. Pretty soon you are bound to feel like the tech debt is weighing down your company from achieving the vision you have for the org. How many times we have gotten caught up in situations like

- More and more bugs and hence service tickets opening up, taking up more and more bandwidth of support and tech team
- Fixing that small bugs, or making that small tweak is taking weeks.
- The velocity of the engineering team going down, and business teams complaining about engineering not delivering

These are indications that you have accumulated quite a good amount of tech-debt.

## Can you escape tech debt?

It is very common for an early-stage product to accumulate tech debts. You need to move fast to get out as much customer-facing functionality as you can and there’s no time to pay attention to stability or scalability. At this stage, it is necessary to a large extent.

> A little debt speeds up delivery quite a lot.

==It is OK to make some tradeoffs and not build things in the most robust way as long as you get things out quickly.== You can, rather, you have to keep on saying, ‘**Not Today**’ for a while.

![What do we say to tech debt](https://media.licdn.com/dms/image/v2/D5612AQHfSje3Vezwqg/article-inline_image-shrink_1000_1488/article-inline_image-shrink_1000_1488/0/1665205706868?e=1764806400&v=beta&t=J3A1gSz450psSuPXwQTjkTR7fAD46-9tQtsbJ9WVcT0)

But once the company really starts growing and you start bringing in hundreds of customers, that doesn't work anymore; because the more customers you have, the more your engineering team is going to have to address escalations that happen. The more Functionality you have put out there, the more will be the demand for maintaining and improving that functionality because, like a very wise man once said:

> “No feature is ever done after version one”.

And of course, the more customers you're supporting on your platform, the more those shortcuts that the team did on the technical side would surface. So the team is going to be very distracted with fixing things. And finally, what you are left with is a very complex and very high maintenance product that keeps on breaking and leaking from here and there.

![No alt text provided for this image](https://media.licdn.com/dms/image/v2/D5612AQGjcXm5H_8veQ/article-inline_image-shrink_1500_2232/article-inline_image-shrink_1500_2232/0/1665206114326?e=1764806400&v=beta&t=VMxxKCfuqCmG0ImyZmUcnRMIhIxs3uhYmSmcHnfjM5E)

So the question is **, how much tech debt can you afford to accumulate?** 
(_Callback: ==similar to how much can you let that pot-belly or the back-ache to grow, or that relationship to deteriorate before you start taking care of them_.)==

  

## When chaos arises, the PM will be hunted down

![tech debt](https://media.licdn.com/dms/image/v2/D5612AQFTQ69PXryU9A/article-inline_image-shrink_1500_2232/article-inline_image-shrink_1500_2232/0/1665208828635?e=1764806400&v=beta&t=qC-wMSHO9RVTZpPIC94hI2w-n8n0RV8q97mcxHxfreg)

No matter how much we cover up, ==every company at the end of the day is a sales-driven company.== When you were building and delivering fast, the sales and business team got the hang of it. Now when things start breaking and delivery speed reduces, there will be an impact on growth. When this happens, the scapegoat will always be the Product Team.

There’s not much use in making the business understand the tech debt fallacy either. They are not interested in hearing stories, and in one way it is just to some extent. Their incentives (and somehow their life) depends on sales. When sales are hampered because of product issues, there's an easy punching bag.

You can try reciting a Shakespearean monologue in that meeting room, being all philosophical describing how you were the greatest person on the earth when you delivered faster than light and now it’s time to repay. ==As a PM, however, you have to end up taking the blame anyway. ==, So it's better to be prepared beforehand.

**JTBD:** A PM needs to be very stern here and inform the Stakeholders that the team will be focussing more on putting the house in place and for a while, only very high-impact features will be addressed. You need to show them the picture of the doom and rightly scare them to the core that if things are not taken care of right now, the entire economy of the organization will break. How operations costs will go up, SLAs won't be met, the speed of delivering value will get lesser and lesser, and ultimately lesser conversions and increasing refunds.

---

## Strategies to retire that tech-debt

If you walk around the internet, you will find 2 ways people prefer to solve tech debt, having a certain fixed bandwidth allocated in every sprint and/or having a dedicated team.

Having delivered three 0-to-1 products and two 1-to-N products, one thing I have understood is that One-size doesn’t fit all, and the strategy will vary based on the situation. If we can just be aware of **3 things**, we can have a robust approach to solving the tech debt fallacy.

### **1. Gauging the Runway**

It's absolutely OK to let tech debt accumulate but you need to understand the length of the runway on which you are going to operate your flight. If there is a long runway and you are preparing for that long flight, you can afford to build scrappily for a longer time. But as soon as the flight prepares for take-off, mistakes can cost a humungous amount.

Just like, you don’t need to start investing from the first salary itself, you can take time to enjoy. but you need to get into action as soon as the credit card bills pile up.

Moving on from philosophies and analogies, in reality, the JTBD is to keep a sharp eye on a few things, **the growth curves**, the **number of bugs and issues**, the tech teams' **velocity,** and their **allocation** in resolving bugs vs building features. It’s a combination of all these things that will paint a clear picture of how soon you need to start taking Tech-Debt seriously.

### **2. Know the breaking points thoroughly.**

In today's world, technology is changing faster than in the blink of an eye. It is always tempting to scrap the existing one and adopt the new one as it is more flashy, but at what cost? Will it solve the current breakages, Do you have a log of which scrappy codes and architectures were delivered to keep up with the pace of delivery

Before you fall into the trap of changing to new, do remember, the US defense got rid of Floppy disks used to control US nuclear weapons in 2019. For half a century they used those 8-inch disks, simply because the floppy disks did the job well and securely.

> _(Opinion)_

> _A feasible way to approach this is to Empower the Engineering team to maintain a Confluence page on_ _**“Tech Radar”**__. Whenever a feature is delivered, let the developer put in notes over here on how might this feature behave at a scale, what has the potential to break, and if there is something we should look out for in the near future. Encourage the tech team to keep revisiting this doc during every sprint retro. The Tech Radar might also include frameworks, and architectures that “want to adopt”, “want to assess”, and ”want to avoid”._

> _This single set of artifacts can be the guiding spirit when you get drowned in that sea of tech debt._

**3. Empower the engineering team and provide the leeway.**

At the end of the day, the tech team will resolve the tech debt, for themself, for the business, and for the customer, not the PM. So, whats your role here?

> As a PM, your role is to judge the impending doom and empower the Tech team.

As soon as you have figured out that the runaway is ending, and things have started showing the potential to fall apart, you have to take some steps.

- ==Reduce the size of the feature backlog through ruthless prioritization ==. If you as a PM budge into business and customers to deliver more and more features, it will hurt back. _Don’t take up fancy features in your roadmap if you feel the existing core frame is going to break soon. Ask harsh questions about the impact of a new feature. If the house is breaking then decorations can wait._
- ==Take the Engineering leaders in confidence== and make them understand why you are bringing lesser feature requests to the table. Empower them to dedicate time to retiring tech-debts slowly and steadily.
- ==Leave the strategy of allocation to Engineering leaders.== Don’t fuss about the percentage time allocation or the number of engineers working on them. Instead, work with them to create a system of tracking and monitoring metrics indicating system health.
- ==Keep track of the metrics regularly.== The next time when you are charged about features not getting delivered, these metrics are what will come in handy.

---

The most critical task of a PM in regard to tech debt is to foresee the impending doom. You can wait and enjoy the summer but winter will eventually come for all, and you have to be prepared.

Before winter strikes, just as a cold wind starts blowing, it’s high time to reduce the load of new customer-facing features on the engineering team. Build those logs, those observability services and dashboards, optimize those APIs and queries, build the internal tools, invest time on regression and unit testing, perma-fix those quick-fixes, frameworks, and architecture.

Sooner or later, you have to pay the debt, it’s up to you to decide when and how?