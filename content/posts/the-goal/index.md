+++
author = "Alexey Kondratov"
title = "The Goal: A Business Graphic Novel"
date = "2025-05-04"
description = "Thoughts after reading The Goal: A Business Graphic Novel and an attempt to apply it to the software development industry."
tags = [
    "business",
    "books",
]
+++

<img class="image_200px_right" src="the-goal-cover.png" alt="The Goal: A Business Graphic Novel cover, source: amazon.com">

I've recently read [The Goal: A Business Graphic Novel](https://www.amazon.com/Eliyahu-M-Goldratts-BUSINESS-GRAPHIC/dp/0884272079), which I've found very entertaining and eye-opening so here are my thoughts and my very superficial interpretation of its concepts after reading the book. As it stands from the title, it's a graphic novel, which is based on Eliyahu M. Goldratt's novel [The Goal: A Process of Ongoing Improvement](https://en.wikipedia.org/wiki/The_Goal_(novel)). Yay, that's the right format -- ~business book?~ no, ~business novel?~ no, business **graphic** novel! Honestly, this is the first _business book_ I've read, so take everything written here with a grain of salt.

## Background

It's important to write a couple of sentences about my background, so it was more clear why this book impressed me so much, that I decided to write my very first _blog_ post. You can safely skip reading it to save a spare minute.

Both my parents were soviet radio engineers, so the atmosphere I grew up in was like _'Find a purposeful work of your life (medicine, engineering, science, education, etc.), if you can make good money -- great, but if you cannot --- well, you are anyway doing an important job for society'_. Doing anything just _for money_ was always considered something shameful. I'm not saying here that this particular mindset was unique to the USSR and/or that everyone in the USSR shared it; it's just this explains the young me quite well. Later on, I got my Master's degree in physics, defended a PhD, and spent several years working on fun projects in startups.

Throughout all these years, I was never focused on earning money. Yes, I was earning enough for a living, and my income was gradually growing most of the time, but that is all. Here, I should probably stop; it's enough of a personal touch, but you can already guess why I'm talking that much about money...

## Theory of constraints

At first, let me cite the [Wikipedia page](https://en.wikipedia.org/wiki/Theory_of_constraints):

> The theory of constraints (TOC) is a management paradigm that views any manageable system as being limited in achieving more of its goals by a very small number of constraints. There is always at least one constraint, and TOC uses a focusing process to identify the constraint and restructure the rest of the organization around it. TOC adopts the common idiom "a chain is no stronger than its weakest link". That means that organizations and processes are vulnerable because the weakest person or part can always damage or break them, or at least adversely affect the outcome.
>
> The theory of constraints is an overall management philosophy, introduced by Eliyahu M. Goldratt in his 1984 book titled The Goal, that is geared to help organizations continually achieve their goals. Goldratt adapted the concept to project management with his book Critical Chain, published in 1997.

This is a very good summary, and it looks like the graphic version of the novel does a great job explaining it because this is aligned with how I got the idea of the book.

The novel's plot is built around a plant manager trying to prevent his plant from being shut down due to inefficiency. So, what's The Goal? Surprise-surprise, The Goal of any business is **to make money**. After stating this in the very first pages of the novel, the author suggests three measurements that are crucial for understanding the ideas of the book:

1. **Throughput**, i.e. the rate at which the system generates money through sales.
2. **Inventory**, i.e. the money spent on purchasing stuff that should be sold.
3. **Operational expenses**, i.e. the money spent in order to turn the Inventory into Throughput.

The rest of the book focuses on understanding the **constraints** --- probably the main concept of the theory (hence the name). The story is a bit oversimplified and doesn't perfectly reflect real life, but it's probably inevitable to keep the book's scope and size reasonable. Either way, the main constraint of the system in this particular case appears to be inside the plant itself --- there are certain steps in the production process that are **bottlenecks**, i.e. they limit the throughput of the whole plant.

Although 'bottleneck' sounds like something you can hardly deal with (except by spending more money on increasing its capacity), the whole point of the book is that you can still increase the overall throughput by carefully organizing processes around constraints/bottlenecks. This contradicts a very _natural_ situation when each component/department focuses solely on its own performance. You can notice that I do not use the word 'efficiency' in the text, this is because the novel asks a good question: 'What is efficiency?'. Indeed, are you efficient if you work 100% of the time and your department produces record numbers of some specific component? It's tempting to say 'yes', but does it bring you close to The Goal? Answering this question is much harder, e.g., if all the components you produce just pile up without selling it's hard to say that it's an efficient process.

Ultimately, the book suggests the following flowchart for solving this problem:

1. Identify the system's constraints.
2. Decide how to exploit the system's constricts.
3. Subordinate everything else to the decision in 2.
4. Elevate the system's constraints.
5. Go back to 1.

It's important to note that the novel is indeed built around an oversimplified scenario --- the constraint is internal to the system, and the market can 'absorb' all the goods produced. However, it also acknowledges that the constraint can take many forms: a department, people, policy, the market, and so on.

## Thoughts

Because I'm currently working as a team lead in an engineering department (software development) in a tech DBaaS company, I was constantly thinking about how the same ideas apply there, while reading the book. I think that for software development, time really equals money in terms of Inventory and Operational expenses, so I will use these two words interchangeably.

1. **Throughput**. I'm not sure that I was able to map throughput to software engineering correctly. As per The Goal, throughput is the rate of generating money through sales. Yet, even if your company sells software licenses, engineering teams do not physically 'produce' these licenses. Instead, they produce features that differentiate the product and make it more sellable. For service companies, it's even harder. It will be fairer to define throughput as a rate of delivering production-ready features that bring the product to the state that allows the company to generate money through sales.

2. **Inventory**. I defined inventory as time spent on features/projects that haven't yet reached the production/sellable state. One of my ex-managers once said something like _'If you open 10 PRs that don't get merged or make progress, you've actually achieved less than if you had opened just one and shipped it to production'_. Indeed, by investing our time into projects that are not delivered, we increase our 'inventory', which in turn, doesn't get the company closer to The Goal. I think that [Kanban](https://en.wikipedia.org/wiki/Kanban), with its limit on 'In progress' items, focuses on a very similar idea --- to minimize the excess inventory.

3. **Operational expenses**. The book explicitly suggests separating Inventory and Operational expenses, but I think this doesn't make much sense for software development, at least under my definition of inventory in 2.

4. **Bottlenecks**. Most likely, all of us dealt with bottlenecks before. Your manager likes to micro-manage everything, so the team cannot decide on anything while he is on vacation? Your teammate opens half-baked PRs, so they need many-many review iterations to reach the mergeable state? You are a perfectionist and/or tend to dig way too deep, so you become a bottleneck of a project? There is only one person in your team who can do production deploys, but now they are on sick leave? For the latter, there is a famous concept in risk management -- [Bus factor](https://en.wikipedia.org/wiki/Bus_factor).
   </br></br>
 I think all decent managers try to avoid being bottlenecks themselves and to deal with existing bottlenecks. However, I can barely remember that I've seen software engineering projects that are planned taking into account that some teams (or persons) are bottlenecks. This could be actually a good practice, but I'm afraid that saying 'Hey, I know that your team could be a bottleneck in this project, let's think about how we can deal with it?' could be perceived as something offensive.

All in all, I cannot say that I've learned a lot of absolutely new ideas, but this book helped me make some important connections between concepts that I was already somewhat aware of. My takeaways are:

1. Remind myself what's the business' Goal. I think many engineers (me included) tend to distantiate a bit from all the business stuff and focus on technology. It's important to periodically ask yourself, 'Is what I'm doing actually important for the company and the business right now?'.

2. Keep bottlenecks in mind. 'When we reach the milestone M1, what will be the next bottleneck? Will it be my team/me or someone else? Should we start working on it earlier?' and so on.

3. Effective communication cannot be overestimated, and just asking can get you quite far. I haven't touched this part above, but in the novel, there is a great example: the plant got an order of 950 parts to be shipped within 2 weeks. They did calculations and realized that they could not make it, so they offered 250 parts per week over 4 weeks. And it appeared to be more than acceptable for the customer.

In the end, I want to say that 'The Goal: A Business Graphic Novel' is a really good and fun read, so I suggest you grab a copy and spend a couple of hours reading it.
