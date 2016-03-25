---
layout: post
comments: True
title:  "ContractFix | The quickest, easiest way to do contracts"
date:   2016-01-06
categories: [hack reactor, software engineering, bootcamp, thesis, contracts, negotiation]
---

This post will introduce my latest project, ContractFix.

During Hack Reactor, you are given several opportunities to create few group projects. For the first two projects – Greenfield and Legacy, we have 4-day time limitation so it is difficult to develop applications that are fully functional and launchable. However, for the final thesis project, we are given 4-weeks. Naturally, most of us wanted to take on something that is more scalable and complex.

One of my classmates, Ahmet, came up with the idea of the app (checkout his blog! – http://jsville.com) and few of us who loved it formed a team of four. Ahmet has an incredible amount of project management experience and at his past jobs, he always thought too much unnecessary money and time are spent and wasted for contract negotiation because of mailing or emailing back and forth revisions, having to visit the other signing party to finalize deals, etc, so why not create a platform that allows easy and smooth contract negotiation, management, and signing?

We originally wanted to offer two different types of services – one designed for companies/corporates and the other designed for individuals. However, during brainstorming, it became apparent that if we were to include features needed for companies, the scope of the project would be too big and the 4-weeks we have definitely would not be enough. So we decided to focus on catering to individuals needs for now.

**Tech Stack: Node.js, Hapi.js, MongoDB, AngularJS, Bootstrap, CSS**

We wanted our application to do the following: allow users to

- sign up and verify their accounts
- create, edit, and save contracts
- select pre-loaded templates or start from an empty editor
- track changes that they make for the contracts
- invite other parties to edit contracts
- submit digital signatures for all signing parties
- view past and current contracts on user dashboard

While these features initially sounded like they were very much doable, some of them were extremely challenging, especially creating of the editor that tracks changes and implementation of digital signature. Luckily, my teammates Michael and Ahmet were able to implement these features after putting in hours and hours of work. Michael basically engineered a text editor and revision system based on CKEDITOR and Ahmet engineered the digital signature portion using OpenPGP.js at the back-end and AngularJS and jSignature on the front-end.

**Digital Signature Page**
![Digital Signature Page]({{ site.url }}/assets/signature.png)
**Editor Page**
![Editor Page]({{ site.url }}/assets/editor.png)

Another challenge was figuring out the user flow and designing the front-end UI. Because our app required quite a number of complex functionalities, we spent a lot of time in the beginning developing a project plan and defining product requirements which helped us tremendously later. I mainly worked on building the Angular app, transforming UI mock-ups into front-end UI, implementing client-side authentication using JSON Web Tokens and building a user dashboard to allow users to view and access their past and current contracts.

**ContractFix Landing Page**
![ContractFix Landing Page]({{ site.url }}/assets/landingpage.png)
**User Dashboard Page**
![User Dashboard Page]({{ site.url }}/assets/dashboard.png)

Some of the things I learned and took away:

- Be resourceful and make less work for yourself. During thesis, Ahmet introduced us all to several different programs – Paw and Robomongo, which made testing requests between the server and the client-side and viewing the database easier.
- Keep in mind any technical debt you are accumulating. Although we did try to modularize our codes as much as possible, by the end of the project, we were so concentrated in getting the work that we wrote some codes that were not very ideal – for example, making HTTP requests directly inside a controller and not making use of services. Luckily we did not run into Git merge conflicts but this sometimes made it difficult to see where errors occurred and now we have a lot of refactoring to do. Also, we did not make use of TDD or continuous integration.
- Front-end work is important for team’s confidence. This is a tip I got from my brother who is also a software engineer. We spent a great deal of time styling our app because usually groups with more beautiful apps seem to feel better about their projects. Because we had weekly progress/check-in presentation, if your group had a lot to show on the front-end, it definitely made an impression.
- Communicate!!! I cannot emphasize enough the importance of communication between teammates. If you have great, honest, and respectful communication happening within your group, you will naturally love spending time working on the project and be more inclined to put in more hours of work. Also take some time in the beginning to divide roles and everyone should take full responsibility for what they promised to complete.
Overall, I learned so much in the past 4 weeks and I am so thankful that I got a chance to work with such an awesome team. Some of us are planning on taking the app to the next level as well. In the meantime, check out our deployed app [here][contractFix]!

[contractFix]: https://contract-fix.herokuapp.com/