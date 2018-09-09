---
layout: post
title:      "Learn IDE vs Atom"
date:       2018-09-08 23:21:57 -0400
permalink:  using_learn_ide_vs_atom
---


When I first started the Fullstack Web Development program, I got on board with the IDE that Learn.co provided.  It's very easy to install and seamless funtionality of using it with the labs is what kept me using it.  However, every instructor or tech specialist I had come across used something other than the Learn IDE.  I knew eventually I would need to transition to an outside IDE or text editor/terminal set-up.

**Learn IDE**

There are a few advantages of using the Learn IDE.  My favorite features include the "Open IDE" button for labs.  It saves you the time of forking and cloning the lab from github.  I also like the ability to run test by typing in "learn" in the terminal.  It saves the time of typing in the full file name.  Having the terminal, file browser, and text editor in the same environment is the best part.  I only realized the convenience of all this now because I recently transitioned to using Atom paired with my terminal.

**Transitioning**

The Learn IDE is based from Atom, the open source text editor developed by Github.  I downloaded it around the same time I started this program to see which I'd find easier to use.  I had no clue what I was doing.  It's stayed dorment among all my other applications while I got used to using the Learn IDE.  I was starting my CLI Data Gem Project and watched a walkthrough video of Avi bulding a gem.  Guess what he's using...Atom.  It was a little hard to follow Avi's workflow using the IDE, so I decided it was time to give Atom another shot.

I vastly underestimated what I was getting myself into.  Setting up a new gem project, creating a respository for it on Github, linking the respository to the project, etc etc. These were all things I had come across at the beginning but I had gotten so relient on the Learn IDE, I had to relearn everything.  I felt like I was wasting time but I had gotten so deep in Atom it was too late to start over with the Learn IDE.

I started making some progress. My file structure was all set up and I started coding my scraper.  I hit a wall when I was trying to get my gem to run.  I had no clue what I was doing wrong.  I had no tests to fallback on to tell me what I needed to fix.  I spent 2 nights trying to sift through ggogle, old labs, and stackoverflow before I got help.  Using the ask a question feature (which I didn't know I couldn't do if I was working on a project), my bin files were up and running within about 10 minutes of troubleshooting.

What I got that was the most helpful, is how to debug using pry.  I was trying before but I didn't even know where I should pause the program to start using pry.  If I were stuck using the Learn IDE, I would just type in "learn" and see which tests were failing.  Here, I had to figure out which piece of code I thought was breaking and inspect that.  To do that, you have to really understand what's going on and what the code you're writing should do.

As painful as it was, I'm so glad I went this route.  I really felt like everything I learned up until that point came together.  I directly saw how these skills could help me in a real coding.  I went from making tests pass for labs to building something from nothing with a better understanding for the language and concepts.

**Atom**

All in all, Atom is the best.  Even though it's a text editor, there's so many add-ons that people have built that you can customize any feature you'd like with it.  One feature that's already embedded is it's connection to github.  It was so easy to make commits and push them to my respository.  I never really understood that concept because I only used "learn submit" to commit a lab through the Learn IDE.  But, it's even easier to do through Atom vs. the terminal commands.

Once you save any file changes, toggle the git view and use the interface to commit those changes.
![](http://blog.atom.io/img/posts/github-package-coauthor-amend.gif)

Moving forward, I'm going to use Atom much more to retain what I know and be less relient on the convenience of the Learn IDE.
