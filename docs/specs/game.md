Now I want to design an interactive "game" for exploring redistricting and gerrymandering.

I want to borrow aspects of these two sources:

* The New York Times redistricting game -- https://www.nytimes.com/interactive/2022/01/27/us/politics/congressional-gerrymandering-redistricting-game-2022.html; and
* The Wikipedia page on gerrymandering -- https://en.wikipedia.org/wiki/Gerrymandering 

I want to design a game that has the following features:

* Uses hexagonal blocks a la the New York Times’ Hexapolis game
* Has 5 districts, instead of 9
* Has 35 people, instead of 135, i.e., 7 people per district instead of 15
* Uses cyan and green for the parties, instead of purple and yellow
* Has 21 cyan blocks and 14 green blocks
* So a proportional map would be 3 cyan and 2 green districts, 
  where a district goes for a party by having a majority of voters

* No complicating minority considerations — just partisan
* For the default configuration of voters — i.e., the default political geography — I want it to be possible to draw maps with:
  - 5 cyan and 0 green districts
  - 3 cyan and 2 green, and
  - 2 cyan and 3 green 

* I want to be able to change this default configuration of voters, i.e., explore alternative political geographies.

Can you help me design this game?

(Once I have a solid design, I will ask you to implement it in code, but for now I just want to focus on the design.)