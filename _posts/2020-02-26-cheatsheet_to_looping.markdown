---
layout: post
title:      "Cheatsheet to Looping"
date:       2020-02-26 01:20:29 -0500
permalink:  cheatsheet_to_looping
---



Looping is used when we need to tell our program to perfrom a task multiple times. This is used to avoid having tremendous amount of code doing the same thing. The most basic form of looping is to use the [loop do] method.

loop do
    puts "This is a loop"
		
	end
	
	This will create an infinite loop of our puts line. We usually do not want this to happen so we could throw a [break] in there to stop the loop.
	
	loop do
	    puts "This is a loop"
			break
	end		
	
	This will however only make the loop be performed once since the [break] will end the code. Lets say we wanted our loop method to loop a certain amount of times. We can use the [times] method in order to perform a loop any specified number of times.
	
	6.times do
	    puts "this will loop 6 times"
		end
		
	The break isn't necessary there because we are only telling the program to loop 6 times and then finish.
	
	Let's say we wanted to make our program count to 10. We can set up a counter to set the integer we wanted and then run the program until it reaches 10.
	
	counter = 0
	loop do
	
	   counter = counter + 1
	   puts "#{counter}"
		 if counter >= 10
		   break
			 end
	end
	
	this loop will keep going until the counter hits 10 and then stop.
	
	These are the basics of loop and can be used in a multitude of scenarios
		
