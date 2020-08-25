---
layout: post
title:      "Travelling through the Star Wars Universe-CLI Gem Project"
date:       2020-08-25 20:38:26 +0000
permalink:  travelling_through_the_star_wars_universe-cli_gem_project
---


For this project, Chewie is your pilot and takes you throughout the Star Wars Universe.

![](https://media2.giphy.com/media/dfzyBlzJH9Q0E/giphy.gif?cid=ecf05e475h921b7zpkal6ufns2q5renaeqbb8b60g7irwvdi&rid=giphy.gif)

I decided to use an API (Application Programming Interface) for this project. I didn't feel as comfortable with APIs so I figured it'd be a good challenge... and it was!

I started with building out my CLI class- the class responsible for interacting with the user. This was the easy part. The user is welcomed to Star Wars Travel Agency.

Next, I pulled the information from the API using RestClient and parsed the data with JSON. I chose to use two parts of the Star Wars API (swapi.dev) - Starships and Planets. The elements I needed were nested inside another hash "results", so I had to account for this before sending my instances to the Starship class: 

```
 def self.get_starships
        starships = RestClient.get('https://swapi.dev/api/starships/')
        @starship = JSON.parse(starships)
        @starship["results"].each do |ship|
            SwTour::Starship.new(ship)
        end
    end
```


This gave me the keys and values I needed. From here, each ship was initialized in the Starship class and added to the class variable, an array, @@all. I looped through @@all to display the starships for the user to choose from:

```
1. CR90 corvette
2. Star Destroyer
3. Sentinel-class landing craft
4. Death Star
5. Millennium Falcon
6. Y-wing
7. X-wing
8. TIE Advanced x1
9. Executor
10. Rebel transport
```

Once the user selects their ship, they are presented with some information about the ship they chose, including the model, manufacturer, and number of crew members, all presented by plugging in the user's ship key to retrieve the needed values.

While it does what I wanted it to do- it wasn't enough! I decided to make an array of all the ships used for the dark side, so when the user chooses the Star Destroyer, Death Star, TIE Advanced x1, Executor, or Sentinel-class landing craft, another message pops up "Looks like you've chosen the dark side!". I also added the colorize gem, and this message is presented in red for extra flare. 

![](https://media1.giphy.com/media/xTiIzjWP7ILGoNkS2Y/giphy.gif?cid=ecf05e47ktl7ybd7t989zxraj38dpbevkessw8igcm8omtwy&rid=giphy.gif)

Next, the user chooses from a selection of planets, retrieved from the API. I found that all this pops up quickly and can seem like a lot happening at once. I decided to add a sleep method for 3 seconds after the starship information is displayed to help slow things down.

Once the user selects a planet, they are presented with additional information including: Climate, Terrain, and Population. Depending on the climate, they may be presented with an additional message (i.e. "Brrr... I hope you brought some warm clothes!" for a frozen climate such as Hoth).

I added another sleep method after the planet information is displayed to give the user time to read. It also doesn't feel much like travelling if the user chooses a planet, and is welcomed to the planet immediately after. The sleep method helps with both of those.

Lastly, the user is welcomed to the planet they chose, and given the option to exit or travel again.

As with any project, I did experience a few hiccups, which I learned so much from. These are some of them:

1) The biggest lesson gained from this project is setting up a gem. It looks easy to just run "bundle gem [project_name]", but getting all the files set up for the first time is a process. All in all, it probably took around 2 hours to get my environment file set up, my bin files set up, my CLI file set up, make sure all files have the requirements they need and are communicating with each other. Next time I'll be able to get through this process much quicker. 

2) One bug I mentioned above. The hash keys and values (ship names/info and planet names/info) I needed from the API were nested inside another hash "results". With the help of binding.pry, I found a way to get the information I needed easily. Pry has become my best friend.

3) Testing is SO important. After my first run-through of letting the user choose to "travel again" or "exit" (instead of the program ending), the list of spaceships and planets presented to the user doubled. Through some debugging, I discovered the ships and planets were being added to the @@all arrays twice. This was fixed by adding a condition: unless @@all.include?(planet)

4) Collaborating objects has been the most difficult topic for me in this course thus far... this project has given me so much practice! I feel much more comfortable than when I started.

I think this is definitely one of those projects that I'll always be working on- I have so many ideas!

Carrie
