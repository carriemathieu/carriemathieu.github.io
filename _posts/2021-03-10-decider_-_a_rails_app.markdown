---
layout: post
title:      "Decider - A Rails App"
date:       2021-03-10 22:46:23 +0000
permalink:  decider_-_a_rails_app
---


How many times have you and a group of friends sat around trying to figure out where you were going to go for dinner... only to finally agree upon a solution an hour later? That's where "decider" comes in.

In this app, users can create a "task". This task is essentially an idea for which you are seeking input... it could be where you will travel next for vacation, or what you'll watch for your next movie night, or which Star Wars character is the best.

![](https://media.giphy.com/media/5tRGwBkWx8Vt6/giphy.gif)

Once you've created the "task", users can offer their input, known as "suggestions". If the "task" is 'Our next Netflix binge', then a user could offer a "suggestion" of 'Bridgerton'. 

![](https://media.giphy.com/media/RYY2R6zeSCQ3oTif1I/giphy.gif)

While each user can only submit one suggestion per task, each task can have multiple suggestions. Once a user is content with the number of suggestions, they can opt to "randomize suggestion" which will generate one suggestion out of all the suggestions submitted for that task... and that's the winner! Congrats... you just made a decision with very little effort!

![](https://media.giphy.com/media/4QFAH0qZ0LQnIwVYKT/giphy.gif)

I had a lot of fun creating this app. One of my favorite features is the ability add friends - an idea that [this railscast post](http://railscasts.com/episodes/163-self-referential-association?view=asciicast) explains and walks through really well. While some of this content was out of my comfort zone, I learned a lot by reading through the explanations, and it further solidified my understanding of associations between models and how they interact.

![](https://media.giphy.com/media/TL0IrljE5PjK0PnPRL/giphy.gif)

In addition to the friendship model, I also created models and controllers for tasks and suggestions. The relationships get really tricky here, and I ended up needing to source one of my associations in order to get all the relationships to work. 

In order to generate the random suggestion, I passed the task:id through the link params, to the suggestions controller, and used .shuffle.first of the array of task suggestions- this generated one suggestion at random. I had to play with the routing a little to get this to work, but the end result is worth it.

I also played a little with the styling on this one... while the navbar is all CSS, I did use boostrap cards for the suggestions on the tasks/show page. There's definitely room for improvement and I can't wait to come back after the next lessons to make it even better.

![](https://media.giphy.com/media/POZulBhYwuOI2Dg7oX/giphy.gif)

Link to [decider github repo](https://github.com/carriemathieu/decider)

