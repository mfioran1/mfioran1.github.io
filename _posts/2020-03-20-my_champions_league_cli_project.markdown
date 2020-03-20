---
layout: post
title:      "My Champions League CLI project"
date:       2020-03-20 19:29:04 +0000
permalink:  my_champions_league_cli_project
---


I decided to do my CLI project on my favorite sport to watch: soccer. I watch the english premier league like most people here watch the NFL so I figured I would do something that was probably going to be different than most of the projects out there. My goal was to have an interactive program that would show you which of the 4 top teams of the premier league would be qualifying to the champions league tournament. 

The beginning of it started off easy enough, writing out the cli portion was pretty simple and straightforward which would begin by showing you the top 4 teams in the premier league. This would be created by iterating through the scraped information with a `each.with_index` which gives out the teams in a numbered value. You then would be able to select whichever of the top 4 teams you like and see their stats (wins, losses, draws and total points scored from games played)

Where I started to have issues was with the scraping. I started scraping from the website https://www.espn.com/soccer/standings/_/league/eng.1 
The tricky part was trying to get the statistics of the page. They were nested in one giant array for all 20 teams. This was proving to be tough as I only needed the top 4 teams and I didnt need all of the integers in from the top 4 either. I tried iterating through the information but I just found it easier to just separate the top 4 positions into their own class method, and scrape for the individual position instead of the top 4. A little bulkier of code but I found it worked better and smoother. Once all the information was done it was pretty much smooth sailing from there.
