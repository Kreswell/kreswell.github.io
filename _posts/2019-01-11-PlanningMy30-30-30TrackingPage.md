---
title: Planning My 30-30-30 Tracking Page
subtitle: Way overthinking my fitness tracking.
date: 2019-01-11
tags: [programming, 30-30-30]
---

OK:
1. I really hate tedious bookkeeping (not great for someone in scientific research, I know), so the more I can automate my diet and exercise tracking, the more likely I am to stick with it.
2. One of the reasons I moved my blog over to Github is to give me a space to do some recreational/practice programming.
3. One of the best ways to manage ADHD is to externalize everything, and a good way to do that is to talk it out here.
So, here's my plan for how I'm going to set up my progress tracking page.

{: .box-warning}
**Warning:** Things are about to get pretty technical.

This page is mainly for my own reference. I'm not really expecting anyone else to be interested in reading it.

# Goals
The goals are pretty simple: use the APIs for various web apps, mainly Fitbit, to grab my weight and exercise data, display it in a nicely formatted way, and do some analysis of it.

# Problems
The two main issues I'm having to work around are:
1. Github Pages doesn't provide a back end. There's no server side to read/write files from/to. As far as I can tell, it also can't write to a file in its repository.
2. Accessing my Fitbit and MyFitnessPal data requires authentication (OAuth 2.0). The authentication info needs to be kept somewhere private, not on my Github repository.

# Plan
So my plan is to write a python script that will run on my computer and do the following:
- [ ] Do the authentication to allow me to access my Fitbit data.
- [ ] Get my fitness data from Fitbit via API request. That includes:
- Steps
- Calories eaten (entered via MyFitnessPal, but pushed to Fitbit)
- Calorie goal/total
- Weight
- [ ] Get my (manually entered) run data from somewhere easily accessible to my phone (for entering) and the script.
- Probably a Google spreadsheet.
- Possibly a file on the Github repository.
- [ ] Write it to a file.
- Probably a csv, since it will be organized in a flat table, but...
- xml or json might be more friendly to being translated into web page content, or...
- a markdown or html file already formatted for website display.
- [ ] Push the file to the Github repository for this site.
- [ ] Do some analysis and make some plots.
- Mainly trend plots to help determine the Calorie intake or Calorie deficit that corresponds to 1lb/week weight loss.
- Probably some other plots to help visualize my progress.
- [ ] Save those plots and push them to the repository.
I'd also like to
- [ ] Write a short shell script to periodically run the python script, so the data on this website automatically updates.
- Once per hour is probably a good rate.
- Will probably run on my home PC (Windows).
