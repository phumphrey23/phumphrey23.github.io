---
layout: post
title:      "CLI Data Gem Project"
date:       2018-09-08 22:01:50 -0400
permalink:  cli_data_gem_project
---



I came up with the concept for my CLI data gem project while procrastinating on the first concept I was going to do.  Initially, I was going to scrape fashion sites like Forever 21, Zara, and H&M for their latest deals.  It was overwhelming.  These sites are all very different in format and I couldn’t figure out for the life of me how I was going to make it different from Avi’s Daily Deals gem.

So I went on Instagram…a lot.  Working full time and doing this program has left me with quite a few sleepless nights and lots of take-out.  I follow a lot of food accounts on instagram and I was trying to figure out some meals I can make in bulk to have throughout the week and save time for the important stuff.  My favorite food account is @buzzfeedtasty.  Out of curiosity, I searched to see if they had a website. I found [tasty.co](https://tasty.co/)! And it was a pretty simple format that reminded me of the Flatiron student’s site from the Student Scraper lab.

I modeled my structure after the Student Scraper lab.  I had a recipe class, a scraper class, and a command line interface.  Then I started adding notes in my interface of how I wanted things to function.  

How it was going to work:
1. The user would input ingredients they had or wanted to use as a search
2. The gem would scrape tasty.co for recipe titles that contained those ingredients
3. The user would choose which recipe they’d like to try
4. The gem would scrape the chosen recipe for a list of ingredients and instructions

Initially I started to follow the Student Scraper approach with my scraper and push the collected recipe info into hashes and arrays.  I ran into a wall trying to test/run my program so I got some help from Project Support.  This session was so important! I had almost no practice debugging with pry.  I relied too much on passing tests in past projects.  I also learned the importance of objects.  Using hashes and arrays was literally the opposite of what Object Oriented Ruby is about.  I learned that I could utilize my recipe objects by adding attributes to those instances of recipes I created from the info I scraped.

I knew about objects and how to instantiate them from all the labs I’ve done but this session really brought it all together for me.  I knew the "how" and now I got the “why”.  This made EVERYTHING much easier to understand.

Taking a user’s input and doing something with it was something we did in the Tic Tac Toe project.  So I modeled some of my Interface and Bin files after that. I got my gem to work for the most part to do the initial tasks.  I just needed to account for any user error and problems that were created.

Major issues to resolve:
* Invalid user inputs
* Searching non-ingredients still produces valid results
* Search not found
* Recipes within a recipe's title

I used a bunch of if statements to restart the program if a user input anything invalid when prompted or a search wasn’t’t found.  Initially I wanted users to only search ingredients but because of how I generated the search url based on the input, they could search anything.  Searching by a course, meal name, or anything food related that would produce something from tasty.co worked for my gem.  Instead of figuring out some way to narrow the search, I changed the prompt message to let users search a wider scope.

What gave me the hardest time was scraping titles within titles.  Tasty has compilations of recipes within their recipe options.  A title such as “Meal Prep Breakfast for the Week” contained 11 recipes within.  Luckily, if a recipe was a compilation it literally had the word “compilation” in the url.  

I used an if statement for the recipe_title scraper that would choose which nokogiri selector to use if the url had “complication”.  The hard part was figuring out which method would take care of running through all the following steps of printing those titles, taking in the user input for the selected recipe, and displaying the ingredients and instructions.  It was a loop within a loop situation.  One that I had not seen during this program or had any references on how to approach.

I decided to address it in the recipe_info method from my Interface.  When the scrape_recipe_info method was called on a compilation recipe, it produced an empty array for ingredients and instruction.  I used this as a condition to determine whether it should print the recipe info and finish or fall into the secondary loop.  This got me the results I wanted.

This was a great project to help me put to use everything I’ve learned so far.  I got three major take aways from this project:

1. The importance of objects
2. Debugging
3. How to use Atom (which is so major, I wrote a separate post about it [here](https://tasty.co/).)
