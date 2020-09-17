---
layout: post
title:      "ShareSomethingGood - Sinatra Project"
date:       2020-09-17 06:19:03 +0000
permalink:  sharesomethinggood_-_sinatra_project
---


My background is in Psychology, so I knew for this project I wanted to do something regarding mental health. I started with doing some basic research and found some disappointing statistics referencing the increase in anxiety, depression, and suicidal thoughts since the beginning of the year, and even compared to previous years. Before I get into the details of my project, I'd like to discuss some of the research I found that motivated me to create this app.

First, [an empirical study showed that negative stimuli have a more profound impact on humans than positive stimuli](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3652533/). This negativity bias suggests that humans have to work harder to reap benefits of positive stimuli. Secondly, [another study found that there's potentially a media bias towards negative new sources versus positive ones](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=1780162), meaning it's possible that the media reports more negative news than positive news, making it seem like disproportionately bad things are happening. Lastly, [this study found that people who find the life meaning in their career, friends, health, or spouse are more likely to have a higher life satisfaction than people who find life meaning elsewhere.](https://www.pewresearch.org/fact-tank/2018/11/20/americans-who-find-meaning-in-these-four-areas-have-higher-life-satisfaction/)

With this in mind, I wanted to create something that would encourage users to focus in areas associated with higher life satisfaction: Career, Friends, Health, or Spouse. 

The welcome page displays the information on the same studies mentioned above, and offers the user to sign in or create an account. Once the user is logged in, they are presented with their home page, along with the posts they created. From there, they can navigate via the navigation bar to view other users' posts, create a new post, or logout. If they chose to view other users' posts, they can click on a hyperlink of the user's name to view all of that user's posts on a separate page. The user can also create a new post. When creating a post, they must select a topic: Career, Friends, Health, Spouse. If the user wants to delete a post they created, they can do so easily from the edit menu.

I used the created two tables- Users (has_many posts) and Posts (belongs_to user). Once the tables were set up and migrated, I created the models and set up their relationships. Then I created some seed data to test the functionality of my routes. The login/logout routes were created in the Users controller, along with the signup route. I used ActiveRecord's validation feature to ensure that emails are unique and a user can't create multiple accounts using the same email. Once the user controller was set up, I started on the post controller, using the CRUD routes and RESTful design. For creating a new post form,  I decided to only display the "edit" button on a user's homepage on their own posts, this would help with the user interface and avoid confusion about what can be edited. If a user does attempt to edit a post via URL, they'll be presented with a flash message notifying them that they are not authorized to make any changes to the post unless it is their own. Lastly, if a user is not logged in, the only page they can access is the login, welcome, and signup pages.

I hope to eventually expand on the project, allowing users to comment on each other's posts, and users receiving "good karma" for every post they share. I'd also like to change some of the design and also add some features that would allow users to add friends and message each other, as well as filter the "All Posts" page so they can view posts from a specific topic. 

Lots of ideas and can't wait to keep working on it!

Carrie
