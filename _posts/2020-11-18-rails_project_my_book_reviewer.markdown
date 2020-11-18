---
layout: post
title:      "Rails Project: My Book Reviewer"
date:       2020-11-18 16:17:40 +0000
permalink:  rails_project_my_book_reviewer
---


My third project which used Ruby on Rails, was for a project I created called the book reviewer. I have always enjoyed using the website goodreads.com so I tried to make a small and simplified version of that. I made it with the ability to create books and then set reviews for them. Other users can see the books that have been created by other people and make reviews for them as well. There is also a catalog section which can organize the books you like in a list format, you can create and edit several lists if you like. This feature is for the user who created it only. 

It uses a normal log in and sign up function, also has the ability  in using Omniauth to sign up with your github log in.

This was a fun project to do unfortunately I did during this test positive for covid. Because of this time I was out and unable to do work on the project when I got back into I had a bit of a timecrunch and had to do a quick job to get out the requirements needed to make it a much better project. But nevertheless I did learn a bunch while completing the project.

One thing I learned the most from this project is learning how to use scope methods properly. Scopes are queries that use an Activerecord::Relation object so you can use them in different parts of your code without having to duplicate the code. Scopes are also nice to use because they're cleaner code due to their syntax. My scope method was used to create a highest ranked review section so the user could see the highest ranked reviews. The code I wrote was as such:

 scope :highest_ranked, -> {joins(:reviews).group("books.id").order("AVG(reviews.rating)  DESC").limit(10)} 

To break down this code the method is called highest_ranked. it joins my reviews of said book (it finds the book from its id.) and orders them by their rating. I also only put a limit of 10 reviews on it to keep it organized.

Then I added into my books_controller the method to be able to create a view page for it so it could be displayed for the user:


def highest_ranked
    @books = Book.highest_ranked
end

Overall this was an informative and fun project to do, if I had more time I would have loved to input a search function and possibly dove into the JS portion to clean it up and make it look more appealing to the eye, but there is always the next project!




