---
layout: post
title:      "Rails Project Blog"
date:       2018-01-02 21:18:43 -0500
permalink:  rails_project_blog
---


**Day 1: Getting started**

Now that I'm on my third project, the breakdown of my schedule is starting to feel familiar: I knew most of the day would be spent choosing a project, deciding on features, and then getting myself set up. I encountered some problems getting my rails app started -- at first I tried to build all the folders and files completely from scratch, but that soon felt very conterintuitive. I found a couple different suggestions on Google and ultimately decided to go with typing "rails new commandsapp" in the terminal. This solution gave me all the gems and folders I felt i needed to get started.

Once my skeleton was built, I moved to adding Devise. Devise was one of the concepts I had a hard time grasping during the Rails section, so I was determined to add it to my app so I could learn it better. One of the best sites I found on Devise was on [Launch School's site](http://launchschool.com/blog/how-to-use-devise-in-rails-for-authentication). Not only did it provide step-by-step instructions on how to add it to your rails app, it also gives you a breakdown of some of the important methods Devise automatically adds to your app. I found myself referring to this website frequently while building out my methods. 

**Day 2: OMNIAUTH**

My last two projects were based on wine, so I wanted to try something different this time around. I decided to build an 'online library' where users can rent books, lend them out to other users, and leave their reviews. I chose to focus on adding Omniauth to my app before I started writing all my methods. Little did I know, this would take up the entire day!

The most useful site I found was a blog by developer [Adrian Prieto](http://www.adrianprieto.com/how-to-setup-devise-and-omniauth-for-your-rails-application). His instructions were very clear and succint, and honestly much more helpful than the Learn lesson. I also used [this](http://github.com/plataformatec/devise/wiki/OmniAuth:-Overview) article on Github to fill in some of the gaps in information. Although I followed the instructions step-by-step, I still wasn't able to authenticate through my Twitter account because my localhost URL kept changing. This is the point where I found out that I shouldn't have been using the Learn IDE at all in Rails, and that I should've moved over to a local IDE right after Sinatra (face palm). Once I set up my local IDE, my Omniauth started working. And wow, the local IDE is so much better! I wish I had moved over sooner! So the moral of the story is:

***If you haven't moved over to a local IDE yet and you're in Rails -- stop everything and do it! The Learn Experts can send you a link with the instructions.***

**Day 3: Reset, reset, reset**

Day 3, much like the third day of past projects, was plagued by issues. I started by performing all my migrations and building out my models, controllers, routes, etc. I created some seed data and was able to start testing the methods and views and I was creating. Then, after about 6 hours ... everything broke. And I mean EVERYTHING. I could not longer log in, couldn't sign up, couldn't view my index page .. nothing. I was so frustrated that I stopped for the day, thinking that I needed to view the app with fresh eyes.

**Day 4: It's all about the error messages**.

I actually took a day off between days 3 and 4, which ended up being a great decision because I was really able to approach the app calmly and with an open mind. I looked at my errors again in the terminal and console. I found out my mistake fairly quickly -- I was seeding my database incorrectly, which was leading to errors. Something I didn't know is that if you want to reset your database (for example, if you have a ton of 'test test' and messy-looking items that you want to clean up), all you have to do is use the 'rake db:reset' command. You do NOT need to type 'rake db:seed' again. The reset takes care of the cleaning AND the seeding. This was the reason for all my issues -- I was trying to re-seed a database that already existed.

Once that was solved, I was able to focus on finishing up the app. Something that's been very helpful has been to maintain a Word document with my ideas as to where I want to go next. I'm including a snippet here:
![](http://drive.google.com/file/d/1x3VLEN42huUiKKmNRy8w-rdtLAFd-RYY/view?usp=sharing)

I used to be 'old school' and writing everything down on pen and paper -- but OK, I'm working to become a developer, I think it is time to move to something more electronic. And I have to admit - it is much handier. I approached my app from a user's perspective, planning what to build next based on what I wanted to see as a user. And soon enough, my app was complete! At least for now....

