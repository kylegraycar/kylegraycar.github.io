---
layout: post
title: "Ruby & Rails"
description: Codecademy courses finished!
date: 2015-12-14 12:52:00
featured_image: /assets/RubyCourseComplete.jpg
categories: website
tags: web development, codecademy, Ruby, Ruby on Rails
---
This is a celebratory post to mark my completion of the Ruby and Ruby on Rails courses on [Codecademy][]!

![RubyCourseComplete][]

![RailsCourseComplete][]

I'm a complete n00b when it comes to web programming, so Codecademy seemed like the best place to get started. After taking these courses I'm... still an utter beginner, but will be continuing to look for **free** online resources to educate myself. At least now I know that Ruby and Ruby on Rails aren't the same thing...

In this post 
------------
Are my thoughts on:

- [Ruby](#ruby)
- [Ruby on Rails](#ruby-on-rails)
- [My next steps](#my-next-steps)

Ruby
----
Wikipedia has a good one liner on what [Ruby][] is:

> Ruby is a dynamic, reflective, object-oriented, general-purpose programming language.

Ruby was founded in the mid-1990s by Yukihiro Matsumoto. This is what he said about the idea behind it:

> Often people, especially computer engineers, focus on the machines. They think, "By doing this, the machine will run fast. By doing this, the machine will run more effectively. By doing this, the machine will something something something." **They are focusing on machines. But in fact we need to focus on humans,** on how humans care about doing programming or operating the application of the machines. We are the masters. They are the slaves.

A human-centric programming language sounds great to me. Nevertheless, I still found Ruby to be utterly complicated at times, so I shudder to think of what other, computer-centric programming languages might be like.

Here's my limited take on it: In Ruby, data (numbers, letters, names, symbols, etc.) is organized into variables. These variables can then be organized into methods and classes to manipulate the data and create more data as purposed to suit the objectives of the programmer. There are different kinds of variables, depending on where they're located and what functions you want for them. There's also different parameters and characteristics that can be assigned to methods and classes. Ruby struck me as kind of algebraic, really.

One important thing I've realized about Ruby is that there can be so many different ways of accomplishing the same objective. The best way is the one that requires the least complexity in coding.

Here's a bit of Ruby code from the "A night at the Movies" lesson on Codecademy. Even if you've never seen Ruby before, I bet you could figure out what the purpose is here.

	movies = {
	  Memento: 3,
	  Primer: 4,
	  Ishtar: 1
	}

	puts "What would you like to do?"
	puts "-- Type 'add' to add a movie."

	choice = gets.chomp.downcase
	case choice
	when 'add'
	  puts "What movie do you want to add?"
	  title = gets.chomp
	  if movies[title.to_sym].nil?
	    puts "What's the rating? (Type a number 0 to 4.)"
	    rating = gets.chomp
	    movies[title.to_sym] = rating.to_i
	    puts "#{title} has been added with a rating of #{rating}."
	  else
	    puts "That movie already exists! Its rating is #{movies[title.to_sym]}."
	  end
	else
	  puts "Sorry, I didn't understand you."
	end

This is a neat way to create your own movie list with ratings (there were also actions to `'update'`, `'delete'` and `'display'` movies that I took out for simplicity). I thought this was a good demonstration of how Ruby reads pretty intuitively.

Ruby on Rails
-------------
Rails is another beast entirely. A beast with Ruby blood. Here's what Wikipedia says about [Rails][]:

> Ruby on Rails, or simply Rails, is a web application framework written in Ruby under MIT License. Rails is a model–view–controller (MVC) framework, providing default structures for a database, a web service, and web pages.

David Heinemeier Hansson created Rails in 2004 for [Basecamp][]'s project management tool. He then released it open source. There are two core prinicples within the philosophy behind Rails, Convention over Configuration and Don't Repeat Yourself.

- Convention over Congiguration (CoC):

> ... means a developer only needs to specify unconventional aspects of the application. Generally, Ruby on Rails conventions lead to less code and less repetition.

- Don't Repeat Yourself (DRY):

> ... means that information is located in a single, unambiguous place. For example, using the ActiveRecord module of Rails, the developer does not need to specify database column names in class definitions. Instead, Ruby on Rails can retrieve this information from the database based on the class name.

Although [Jekyll][]'s static webpage framework did serve as a nice training ground for me, the jump from learning the Ruby lang straight to trying to grasp the Rails framework was pretty rough. 

Here's an example... A core part of Rails that Codecademy introduces to you is the [Request-Response Cycle][]. Here's what that looks like:

![RequestResponseCycle][]

... which made absolutely no sense to me in the beginning. I now understand that through Ruby's objects and logic language developers can use the Rails framework (a crap ton of files and folders) to compute information backwards and forwards from the user to what is displayed on the View (the webpage itself with HTML and CSS).

A lot of the syntax used for Rails applications isn't covered in the Ruby Codecademy course. I wish there was more integration between the two courses to make the transition from straight Ruby to using Ruby on Rails a little less bumpy.

My next steps
-------------

I want to keep learning how to create webapps with Ruby on Rails using free online resources. There are a couple that I've already been pointed towards (thanks again, [Joel][]!):

1. Rail's online [resources][]
2. [edX][] Courses on Engineering Software as a Service (SaaS)

Once I work through more courses and have graduated from "utter beginner" to regular beginner I'll then try to create my own simple Rails web app that users could interact with. 

I'll be updating this site with what I find. Please leave a comment if you know of any additional resources for developing webapps with Ruby on Rails!

[Codecademy]: https://www.codecademy.com
[Ruby]: https://en.wikipedia.org/wiki/Ruby_(programming_language)
[Rails]: https://en.wikipedia.org/wiki/Ruby_on_Rails
[Basecamp]: https://basecamp.com/?source=rails
[Jekyll]: https://jekyllrb.com
[Request-Response Cycle]: https://www.codecademy.com/articles/request-response-cycle-dynamic
[Joel]: http://www.jgraycar.com
[resources]: http://rubyonrails.org/documentation/
[edX]: https://www.edx.org

[RubyCourseComplete]: /assets/RubyCourseComplete.jpg
[RailsCourseComplete]: /assets/RailsCourseComplete.jpg
[RequestResponseCycle]: /assets/RequestResponseCycle.png "Source: Codecademy.com"