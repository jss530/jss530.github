---
layout: post
title:  "CLI Data Gem Project: A Journal"
date:   2017-08-14 20:12:13 -0400
---


**Day 1**: Let's get started!

Starting the project is definitely daunting. At first I was staring at my blank computer screen, thinking: ok, where do I begin? For inspiration, I watched the entire CLI Data Gem Walkthrough video. This was extremely helpful, as was Rob Dodson's blog post "[How to Write a Command Line Ruby Gem](http://robdodson.me/how-to-write-a-command-line-ruby-gem/)." Then I wrote a simple action plan - here's a screenshot:

![](https://r3itsa-bn1305.files.1drv.com/y4mypSazJSjyV6S-Ahdgyr8ooXY8GigqKXboH_QNCTYqFUik0CXWCtGd0fqH5FY74rE12jt6usMkokk1POqo7fuP7xF_C9PVhIxWVdOvoE_E_nPGf3fQJlG1VC3yyBr0v6Z6xxzg-hrdFjjPzULydzN8YMUwLesK0oqJ00uLCHpLD8gu1OIiaJk6F16q8hmgT7T4cFGdb2_bZmpxWFQSfZy9Q?width=462&height=181&cropmode=none)

Once I installed the bundler gem, I generated the boilerplate for my own gem (following the instructions in Dodson's blog). I highly suggest reading through each of the files that are generated, because there are some very helpful instructions that will help you set the foundation for your gem. 

Lesson of the day: ***Always write an action plan!*** Whenever I felt like I was getting off course, I would take a look at the plan again to set myself straight. I started on the CLI first by writing my greeting to the user. Once this was done, it felt natural to move over to the .rb file and start on my methods. First, I wrote the names of the methods that I thought I would need to create, plus ideas regarding those methods' behavoirs:

![](https://r3h3xw-bn1305.files.1drv.com/y4mp9ksQB5WOYjSy4Bmt35S9BVqfMDS4fweXliZNiiNi5upugyci8D-eb0kdtGMyjJHOtuGhBl_Z7xH5Za4n_ZseNjRvsf8bODMGQE2DLNKeERjS0XB8ZOnHwo-fcb5AAfS_YVVIf9FFVxSqaGYA-JRkh6gxCL4p3ICbX241yvcR8mB8CwtHWDTN_RZ-mlj1qOeH2Dc49ms1nysMYmDzovERA?width=630&height=413&cropmode=none)

**Day 2**: 99 Problems, and my gem definitely is 1.

To say Day 2 was a frustrating one is an understatement. As I started building my methods and attempted to test, I encountered one error after another. The main issue I was experiencing was trying to load Nokogiri. After 2 hours of troubleshooting and nearing the point of giving up for the day, I had an idea: maybe I was requiring it in the wrong file? Here's the main lesson for the day: ***Make sure all your requirements are in the right file***! Once I moved the requirement to my Gemfile, I was able to start testing.

**Day 3**: A change of plans.

On Day 3, I finally got to work on my scraping method. This is when I encountered a major problem: I realized the CSS on the original site I wanted to use was extremely convoluted. There weren't many clear divs, classes, or IDs. I wanted to stay with a gem based on wine, so I searched for other sites that offered top wine lists. I ended up finding a much better one that also had an added bonus -- tasting notes and descriptions! Lesson of the day: ***Dont be afraid to change plans!*** Once I switched my scraped site, everything started to fall into place. I built the rest of my method skeletons before finishing for the day:

![](https://r3gspa-bn1305.files.1drv.com/y4m6EMdoNGHirVdP4WHJechjpAzjnySuV1FISoPU3hwFuDitXvbQGaKyoP_vODb7FACfWRSG5R5upaak1p6k_lKZ6KOuo3-tzhdhlrWfkiFd4eUaTRWVdUFGmZumO8qMCJIhWJauyd-RnAXvdcI7SFo2K01EygOwLCyvOn_BACG4Zw0DS6T9Hdo02w4uuqa0V6ugj1AMzmaHjISyXYm2owEOQ?width=878&height=246&cropmode=none)

**Day 4:** Finishing touches!

Day 4 was focused on finishing the last couple of methods, building the CLI accordingly, and testing. Based on the tests, I tweaked the CLI and finally submitted. Wow, this was some ride! But I learned so much from this experience - and even better, I gained confidence in myself. My first project from scratch - done! 


