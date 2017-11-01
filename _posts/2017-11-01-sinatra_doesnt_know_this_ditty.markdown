---
layout: post
title:      "'Sinatra doesn't know this ditty'"
date:       2017-11-01 23:15:31 +0000
permalink:  sinatra_doesnt_know_this_ditty
---

**Sinatra Portfolio Project Mode, Day 1**

Compared to the CLI Gem project, I embarked on the Sinatra portfolio project with a considerable amount of more confidence. This confidence was quickly shattered, however, when I realized I was encountering the same issue I had with the CLI gem: I had NO idea how to get started. The Corneal Gem [https://github.com/thebrianemory/corneal
](http://) was a lifesaver. It gave me the structure and gems that I needed to at least get started.

When it came to choosing a topic, I decided to build upon my CLI Project. That gem allowed users to access a list of the Top 50 wines in the world, and to select a wine in order to view a wine critic's description. For my Sinatra app, I wanted to go more personal: this time, I wanted users to be able to access a list of their own wines, as well as view/compose their own tasting notes. I absolutely love wine, and try to maintain a (very) small collection: even with a rotating cellar of 20-30 bottles, I find it difficult to remember what I actually own. With this plan in mind, by the end of day 1 I had my app skeleton built, design and features mapped out, and a plan of attack for Day 2. Or so I thought .

**Day 2: Less Project Mode, more SUPER FRUSTRATED Mode**

Much like the second day of my CLI Project, Day 2 of my Sinatra project was plagued with frustration and errors. Let's just say, Mr. Sinatra didn't know a lot of my ditties. The only page working was the index page, despite all my attempts at reworking. Login and Signup pages refused to appear, it seemed as if the Controllers weren't recognizing each other, and my Helper methods weren't working. After 3 hours of increasing frustration, I decided to walk away and start fresh the next day. 


**Day 3: Ok, things are happening!**

The moral of the story is: sometimes you need to know when to walk away. On Day 3, I was able to view my code with a clear mind, and instantly things started coming together. I re-built my Controllers and separated my Helper class into its own file. I also noticed a coding mistake in my helper method, which was the reason for it not working. I finished my user and wine controllers and views, and started some basic work on the app flow.

**Day 4: Finishing touches**

It's crazy the difference just two days can make. Two days before, I felt like the project was hopeless. Now, on day 4, it is almost complete. On day 4, one of the biggest hurdles I had to overcome was getting the Flash messaging to work. For some reason, my computer and rack-flash just do. not. get. along. No matter what I tried, I couldn't get the error message to appear. It turned out, instead of flash, I needed to use sessions. Here is the blog that was a lifesaver: [http://roseweixel.github.io/blog/2014/10/28/flash-messages-with-sessions-in-sinatra/](http://). 

With that solved, my app is complete! As always, despite all the ups & downs, there is nothing more gratifying than finishing!


