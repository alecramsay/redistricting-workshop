# Game / Puzzle Implementation

Now I want an HTML / Javascript implementation of the game / puzzle we designed.

* Make the puzzle page a link off the main page.
* Give the page a title like "Redistricting Puzzles".
* Have the page describe the political geography of the game:
  - The # of blocks
  - The # of districts
  - The # of cyan and green blocks
  - The rules for how to determine the winner of a district
  - Etc.
* Make the page present a series of puzzles:
  - Puzzle 1: Proportional (3 cyan, 2 green)
  - Puzzle 2: Cyan Gerrymander (4 cyan, 1 green)
  - Puzzle 3: Green Gerrymander (2 cyan, 3 green)
* Allow the puzzles to be selected via a dropdown menu or something like that.
* As districts are drawn, show the partisan lean for the map, i.e., how many districts are cyan vs. green.
* Allow the user to reset the map and start over.

What else should we include in the implementation?

## Revisions

* Put the Home link on a line above the title.
* Left-justify the "Redistricting Puzzles" title.

* Use hexagonal blocks to clarify adjacency, instead of square blocks.
* Use a palette of CVD-friendly colors for the districts.
* Use CVD-friendly colors for the party colors, instead of cyan and green.

* Consolidate information about districts in a panel to the left of the "map" of blocks:
  - Show the district # and color
  - Show the number of blocks assigned to the district
  - Show the party split of the blocks assigned to the district, e.g., 5-0, 4-1, 3-2, etc.

* Change "Hello, World!" to TODO.

## More Revisions

* Add an explicit contiguous column showing a check (yes) or x (no) for each district, as opposed to separately below.
  Use an icon for the column heading, like Dave's Redistricting does, instead of the word "Contiguous".
* Replace the district color green with a different color, so green can be used for a party.
* Make the orange party green (G); and make the blue party orange (O). 
* Reduce the opactity of the district colors, so the underlying blocks are more visible in contrast.
* Make the "Blocks" heading "Assigned", to clarify that it shows the number of blocks assigned to the district.
* Makes the "Split (B-O)" two separate columns "#O" (for the number of orange blocks) and "#G" (for the number of green blocks).
* Call "Partisan Lean" at the bottom "Partisan Split" instead.

## Clean Up

On the home page:
* Remove the "This site is open source ..." from the site's footer.
* Change the home page title color to black.
* Change "TODO" on the home page to "Welcome to the Redistricting Workshop website!"

On the puzzle page:
* Swap orange and green for parties, i.e. 15 green and 10 orange. 
  Use the same voter layout.
* Change the dropdown text to reflect this change.
* Replace the text after the title with this (no blockquotes, just regular text):

> What is gerrymandering? How does the *mechanism* of single-member districts (SMD) enable it?
>
> This applet allows you to explore these questions by drawing 3 maps for a toy state.
> The state has 25 voters, each in their own block.
> There are 15 who vote Green (G) and 10 who vote Orange (O). 
>
> When you draw a map:
> - A district is won by whichever party has a majority of voters, i.e., at least 3 of its 5 blocks.
> - Districts must be contiguous: every block in a district must share an edge with at least one other block in the same district.
> - The dot inside each block shows the voter's party (G or O). The background color shows which district it belongs to.
> - Click a district row in the panel to select it, then click blocks on the map to assign them. 
>   Clicking a block already in the active district removes it.
>
> There are 3 different outcomes in the Puzzle dropdown:
> - 1 -- Proportional: 3 Green, 2 Orange
> - 2 -- Green Gerrymander: 4 Green, 1 Orange
> - 3 -- Orange Gerrymander: 2 Green, 3 Orange
> Can you draw maps that achieve all three results?

* Once the user has successfully drawn all 3 maps, go to a final page that shows a congratulatory message, e.g., 
  "Congratulations! You've successfully drawn maps for all three scenarios!" along with the following text:

> Single-member districts (SMD) distort how votes get translated into seats.
> That is an inherent property of the mechanism.
> The same *political geography* yields different outcomes, depending on how the lines are drawn.
>
> A gerrymander is not about crazy district shapes.
> Gerrymandering is grouping voters for political advantage.
> The two main techniques are "packing" -- concentrating one party's voters into a district where they win by a large margin, 
> wasting their surplus votes -- and "cracking" —- splitting a party's voters across multiple districts where they are always 
> in the minority.
>
> Beware "neutral" criteria, e.g., compact districts aren't always fair due to the urban/rural sort.
> See [Compact Districts Aren't Fair](https://medium.com/dra-2020/compact-districts-arent-fair-7c17c2ff5d7e).
>
> Racial gerrymandering is illegal, but partisan gerrymandering is not.

## Tweaks

* Use two ASCII hexagon characters as the "contiguous" column header:
  https://www.alt-codes.net/hexagon-symbols
* Make a gerrymandering page.
* Move the "What is gerrymandering? ..." text and puzzle link from the home page to the gerrymandering page.
  Put a link to the gerrymandering page on the home page. The link text should be "What is gerrymandering?"
* On the gerrymangering page, put the link to the puzzle page on a new line.
* Instead of automatically (and only) going to the page with the takeaways after the user has successfully drawn all 3 maps,
  put a link to takeaways at the bottom of the puzzle page.
* Make the congratulatory messsage be a pop up. 