---
layout: post
title:      "prepper-first full-stack project"
date:       2021-04-02 17:26:46 -0400
permalink:  prepper-first_full-stack_project
---

#### What is it?
In prepper, a user can choose a category- Ruby, Rails, or Javascript. Each category contains several different word lists related to that category (for example: Ruby Basics, Intermediate Ruby, etc.). Each word list consists of 10 words. These 10 words are not shown to the user; they can only see the title of the list.

When a user opens the page, they have the option to select a category or create a new list. If they choose a category, they then have the option to select one of the word lists in that category. Once a user has selected a word list and clicks "I'm Ready", the Web Speech API will start listening. The goal is to say as many words as possible from the selected word list, knowing only the title of the list, in 30 seconds. Once 30 seconds is up, a user is presented with the results!

The game is similar to the popular TV show Family Fued. This app was created to help users prepare for any event where it's important that they remember to mention specific key words. A user can also create their own list and test their knowledge in preparation for an event such as an exam or interview.

#### Challenges
* The first challenge is that the Web Speech API is currently *only* supported on Chrome or Edge. 

* Secondly, if you're fairly new to Javascript, navigating the web speech documentation can be confusing. Aside from the [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API), this article from [Google](https://developers.google.com/web/updates/2013/01/Voice-Driven-Web-Apps-Introduction-to-the-Web-Speech-API) helped me to understand some of the underlying functions that come with the SpeechRecognition.

* There's a few good tutorials out there for using the Web Speech API. None of them covered exactly what I wanted to implement, so I really learned how to play with "console.log" and "debugger" to figure out what my code was doing, and how to get it to do what I wanted it to.

* I had to re-learn some of the styling concepts. I have a form with 10 text boxes, so formatting those boxes in a visually pleasing way is important. I ended up using grid to get the input fields where I wanted them.

* I ran into an issue using innerHTML which effectively un-binded my event listeners. This was probably the most frustrating bug I encountered making this project. [This stackOverflow post](https://stackoverflow.com/questions/38361875/element-innerhtml-getting-rid-of-event-listeners) did a really good job of explaining why it was doing what it was and how to fix it. It took a while to find out what the issue was, but I learned a **LOT** from debugging this.

#### Final Notes
This is definitely my favorite project thus far. It took a little longer than I wanted, but the ultimate goal is to host this project. I have a short list of things I want to revisit after I graduate, like making the category dropdown more dynamic. 

It's funny how a project can seem easy to implement, then takes 200+ lines of Javascript! 
