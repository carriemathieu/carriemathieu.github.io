---
layout: post
title:      "prepper-first full-stack project"
date:       2021-04-02 21:26:46 +0000
permalink:  prepper-first_full-stack_project
---

#### What is it?
In prepper, you can choose a category- right now, the options are Ruby, Rails, or Javascript. Each category has a list of words (word_list) covering a certain topic within that category (for example: Ruby Basics, Intermediate Rails, etc.). Each word_list consists of 10 words.

When you open the page, you have the option to choose a category or create a new list. If you choose a category, you then have the option to choose a word_list by the word_list title. Once you've selected your word_list, you click "I'm Ready", then start speaking. The Web Speech API will listen to you speak - the goal is to say as many words from the word_list as possible in 30 seconds. Once 30 seconds is up, you're presented with your results!

#### Challenges
* The first challenge is that the Web Speech API is currently *only* supported on Chrome or Edge. 

* Secondly, if you're fairly new to Javascript, navigating the web speech documentation can be confusing. Aside from the [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API), this article from [Google](https://developers.google.com/web/updates/2013/01/Voice-Driven-Web-Apps-Introduction-to-the-Web-Speech-API) helped me to understand some of the underlying functions that come with the SpeechRecognition.

* There's a few good tutorials out there for using the Web Speech API. None of them covered exactly what I wanted to implement, so I really learned how to play with "console.log" and "debugger" to figure out what my code was doing, and how to get it to do what I wanted it to.

* I had to re-learn some of the styling concepts. I have a form with 10 text boxes, so formatting those boxes in a visually pleasing way is important. I ended up using grid to get the input fields where I wanted them.

* I ran into an issue using innerHTML which effectively un-binded my event listeners. This was probably the most frustrating bug I encountered making this project. [This stackOverflow post](https://stackoverflow.com/questions/38361875/element-innerhtml-getting-rid-of-event-listeners) did a really good job of explaining why it was doing what it was and how to fix it. It took a while to find out what the issue was, but I learned a **LOT** from debugging this.

#### Final Notes
This is definitely my favorite project thus far. It took a little longer than I wanted, but the ultimate goal is to host this project. I have a short list of things I want to revisit after I graduate, like making the category dropdown more dynamic. 

It's funny how a project can seem easy to implement, then takes 200+ lines of Javascript! 
