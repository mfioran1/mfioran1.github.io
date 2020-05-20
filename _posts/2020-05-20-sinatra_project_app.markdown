---
layout: post
title:      "Sinatra Project App"
date:       2020-05-20 00:58:51 -0400
permalink:  sinatra_project_app
---


My Sinatra project was I created a workout tracking app that would let you create new instances of workouts, while also having the ability to write your thoughts or how you felt about your workout as well. It follows the basic CRUD examples you would want to use in a basic Sinatra application.

First Part:

  I began setting up my program by creating my gemfile bundle and setting up my config.ru to get the base portion of it working. Then I set up my config/environment.rb so I could get the program to require bundler and establish the connection between ActiveRecord and Sinatra. Once everything was set up I then moved over to created the Databases and classes.
	
	Second Part:
	
	I knew to begin with I would need to create 2 tables in ActiveRecord for databases. A users table which would be used to store the username, password, and email of said users using the program. The other table would be to track the workouts that would be inputted. I wanted the users to be able to be able to thoroughly write down what their workout was so I made columns for the title, duration, level (ex. beginner, intermediate, advanced), details on the specific moves and reps you did, and I also added an area for comments on how they felt about the workout, things they would have done differently etc.
	
	I then set up the models in user.rb and workout.rb and each of their respective classes. the class Workout was simple enough as I only needed it to belong to the User class. In the User class I had wrote that it has many workouts, has_secure_password which encrypts the password for the User, and I created a slug method in order to use the users username in the url, instead of their assigned ID to give it a cleaner look. Once all this was set up, in my terminal I ran rake db:migrate in order to get the databases up and running.
	
	Third Part:
	
	Now that it was all up and running I then set up my controllers. My main controller Application Controller was used to configure what you needed such as setting up :sessions for password security. We also set up the homepage and logout features, I also set up my helpers methods which allow me to check if what the person using the app is the said user that should be using it or not. My other two controllers were created in order to separate and organize the controllers.
	
	In the User Controller I set up what needed to be done to either sign up or log in and the main show page for said user.
	
	In the Workout Controller is where I did my main CRUD actions, this is where the main work was getting done.
	
	Final Thoughts/Things to improve on:
	
	Overall I thought the project was interesting and fun to create, I got to try out using flash error messages which I thought were interesting and took a couple of run throughs of the app to find out the best place to use them. What I need to improve on is saving my code after doing a little bit to keep it organized on my commits. I kept just doing work and can see that it would be tough for someone to go over the process I went through since I would work until I felt like I did enough, save and come back later to it. My next project will definitely be more organized.

	
	
	
