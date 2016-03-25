---
layout: post
comments: True
title:  "Bus It Baby | never miss your final bus stop!"
date:   2016-01-07
categories: [hack reactor, software engineering, bootcamp, thesis, legacy]
---

My Greenfield project, (which was my first group project at Hack Reactor) is called ‘Bus It Baby’. Yes… the name of the app sounds a bit strange and it does make our team cringe slightly in embarrassment whenever we have to talk about it. But it did bring a lot of joy to the HRR9 cohort!

I had a wonderful opportunity to work on this app with three other amazing developers – Alon Robinson, David Lee, and Mykia Smith. Alon came up with the idea of this app; he wanted to develop a mobile app where public transit riders can enter in their destination stops and when they are within a specific distance from the destination, an alarm would trigger so that even if they are asleep, listening to music or even day dreaming, they wouldn’t miss their final stops.

**Tech Stack : Ionic, AngularJS, Firebase, Google Maps API, Bootstrap, SASS**

We wanted our app to do the following broadly:
- allow users to sign in through Google
- allow users to select destination and the distance from it
- trigger alarm when user reaches the final destination
- (store user information into a database, if we had time left)

And here are the features we managed to implement:
- a mobile app using Ionic and AngularJS, optimized for iOS
- authentication for Github (instead of Google) by integrating the app with Firebase
- tracking/calculating distance between user and specified final destination by integrating the app with Google Maps API

![Bus It Baby]({{ site.url }}/assets/busitbaby.jpg)


Takeaways:

- Managing scope is difficult! This was the first group project for all of us and in the beginning, all of us were super excited and wanted to build an awesome full functioning app. The possibilities seemed limitless!! But, we had a 4-day time limitation for Greenfield and it was just impossible to build something that we originally had in mind. So we had to adjust our scope a lot as we developed Bus It Baby.
- It is important to divide tasks and keep track of what everyone is doing. We used waffle.io to view everyone’s task logs and having a visualization of what everyone is doing and where the app was in terms of progress was very helpful.
- Google Maps API is awesome! I got a chance to familiarize myself a bit with Google Maps API during Greenfield and since it is so well documented, you can really take time to learn it and use in any ways that are needed.
- Angular & Ionic are a match made in heaven! This description is also on the Ionic website and they are not kidding. Ionic utilizes AngularJS and it just feels like you are writing an Angular app and it also has great CLI, allowing you to create, build, test, and deploy your app easily.

Overall, I had so much fun during Greenfield. I couldn’t ask for a better team; the communication was so awesome and fun and the level of passion, energy, and humor everyone brought to the team just made Bus It Baby all the more special for me.