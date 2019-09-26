---
layout: post
title:      "CLI: Ruby Project "
date:       2019-09-26 07:53:00 +0000
permalink:  cli_ruby_project
---


<h2>Creating a Ruby Gem </h2>

For this project we created a Ruby gem that would scrape a movie ticket site (specifically Fandango) for new and upcoming movies, and gie information on the movies.

<h2>Getting Started</h2>

All projects need a plan. To get started we need to ask a few questions:

<li> How do we create a ruby gem?</li>
<li>How do we want users to interact with our gem</li>
<li>How do we get data for our gem?</li>

These are our requirements to create our working gem.

<h3> How do we create a ruby gem?</h3>

A bit of searching lead us to a video on [New Gems with Bundler](http://railscasts.com/episodes/245-new-gem-with-bundler) where we learned that using the ```bundle gem [gem_name]``` bash command that the skeleton for a new gem would be generated. 

<h3>How do we want users to interact with our gem?</h3>

I find that placing yourself as a user and seeing it from their persepective is the best way to answer this question. What kind of flow would our program need to have to be a plesant experience. 

Users should be greeted or notified that they are currently using the CLI Movie Gem. 

Users should see which options are avaliable as well as how to navigate the CLI.

Users should be able to exit the program from the CLI and never have to use programming commands in the program to do so.

<h3>How do we get data for our gem?</h3>

To get data we will need to either work with an API or a scraper.  For this gem we've gone with a scraper class that would grab the movie synopsis off of movie ticket sites, [Fandango]https://www.fandango.com/) in this case. 


<h3>Structure</h3>

The structure and flow of a program make programing easier for both the users and the programmers alike. In the gem we've created a user would type "./bin/new_movies"

within the new_movies file a new CLI instance is created and we incapsulate all of the navigations and scraping of data in the ```.call``` method.

```.call``` greets users to let them know the program is running. The ```call```  method contains a ```list_movies``` method which should list the movies that are new and coming soon via the Fandango site.  The ```call```  method also contains a ```menu``` method which allows users to navigate and exit the program. 

```list_movies``` creates instances of movies from information scraped on the Fandango New+Coming Soon carousel at the bottom of the page. 

Users are directed to select the number of the movie they would like to learn more about. When selecting that movie our movie class will scrape the site associated with the selected movie and grab the synopsis of that movie to be printed in the terminal for users to see. 

<h3>Avoiding Errors</h3>

To make sure the user has control of the gem at all times it is important to give direction/instructions where you can and prevent users from making certain decisions. In this case we chose to limit the selection options. Users can only select one of the movies. If they choose a number that is not listed such as #9999 the a prompt instructs users on their options. The ```menu``` method makes any input that wasn't explicitly listed as an option to be invalid.  





