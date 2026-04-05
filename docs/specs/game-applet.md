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
* Remove the "This site is open source ..." from the site's footer.

## More Revisions

* Add an explicit contiguous column showing a check (yes) or x (no) for each district, as opposed to separately below.
  Use an icon for the column heading, like Dave's Redistricting does, instead of the word "Contiguous".
* Replace the district color green with a different color, so green can be used for a party.
* Make the orange party green (G); and make the blue party orange (O). 
* Reduce the opactity of the district colors, so the underlying blocks are more visible in contrast.
* Make the "Blocks" heading "Assigned", to clarify that it shows the number of blocks assigned to the district.
* Makes the "Split (B-O)" two separate columns "#O" (for the number of orange blocks) and "#G" (for the number of green blocks).
* Call "Partisan Lean" at the bottom "Partisan Split" instead.
