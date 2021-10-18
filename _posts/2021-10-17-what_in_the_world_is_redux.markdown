---
layout: post
title:      "What in the world is Redux?"
date:       2021-10-16 23:24:39 +0000
permalink:  what_in_the_world_is_redux
---

Redux is complex. It's a lot. But what is it? What purpose does it serve?

According to the [redux docs](https://redux.js.org/introduction/getting-started): 

>Redux is a predictable state container for JavaScript apps.
It helps you write applications that behave consistently, run in different environments (client, server, and native), and are easy to test. On top of that, it provides a great developer experience, such as live code editing combined with a time traveling debugger.

One of my favorite features of Redux is the [redux devtools chrome extension](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=en). This allows you to easily step into Redux and see your Redux store and all your state easily in one place.

So... Redux. What does it do?

Stephen Grider does a great job of explaining this in his [Modern React with Redux course](https://www.udemy.com/course/react-redux/) on Udemy (which I *highly* recommend).

In order to understand this analogy, it's important to be aware of the Redux Cycle: Action Creator - Action - Dispatch - Reducer - State.

He uses an analogy of an insurance company. This insurance company processes new policies as well as claims on existing policies.


The way it works is a customer fills out a form, this form is for creating/modifying a policy or creating/modifying a claim. That form is received by a representative from the company who then passes it to the appropriate department. The department files the form, then passes along to management, where they keep all the most up-to-date information.

This compares to the Redux Cycle in the following way:

- Action Creator: The person dropping off the form.
- Action: The physical form that states whether it is to create/modify a policy, or create/modify a claim.
- Dispatch: The company representative that receives the form.
- Reducer: Passes the form to the appropriate department
- State: Management who has the compiled data

![](https://media.giphy.com/media/3qsrkMGIeJzfLD1G9n/giphy.gif)

The neat thing about Redux, is it allows a component to access only the bits and pieces of state it needs - similarly to how the  claims department doesn't need to know when a policy is created, only needs to know about claims.

This anology has helped me to better understand the purpose of Redux and accessing and storing pieces of state.
