# Game / Puzzles Re-Design

I want to redesign the game/redistricting puzzle.
I will do this in stages.

## Step 1: Load & Verify the Political Geography

The political geography (PG) of the new puzzles is in the `lessons/pg.txt` file.
It should be an 8x8 grid where each cell is either R for Red or B for Blue.
There should be 32 R's and 32 B's, for a total of 64 cells.

Load the pg, e.g., `pg = [list(line.strip()) for line in open("lessons/pg.txt")]`
and verify that the totals are correct.

## Step 2: Move Puzzle Files to a Subdirectory

Before starting on the puzzle redesign, I first want to:
- Create a new subdirectory `puzzles` under `lessons`
- Move all existing files in `lessons` there, except for `index.md`.
- Fix up any links in the site to work with the files in their new location.

## Step 3: Redesign the Puzzle

This is the new set of puzzles using the PG in `pg.txt`:

-   There are 4 districts, each with 16 cells (voters).
-   Each district must contiguous which in this chess/checkers-style board means each square in a district
    must share an edge with at least one other square in the same district.
-   To start, show the PG as a grid of 8x8 cells, with a dot in each cell showing R(ed) or B(lue) according to the pg.txt file.
-   As in the previous puzzles, let the user create districts by clicking on cells.
-   A district is won by R(ed) or B(lue) if it has more R or B voters, respectively.
    So, 9 or more cells of one color wins a district.
-   A district with 8 R and 8 B voters is a tie and does not contribute to either side's total.
-   Color the districts as follows: if R wins, use some shade of red; if B wins, use some shade of blue; 
    if it's a tie, use some shade of yellow. Use colors and intensities so that the PG colors are also visible.
-   There are 4 puzzles in this game: competitive, sweetheart, packing, and cracking.
-   In the competitive puzzle, the user should try to create 4 districts that are as competitive as possible, 
    i.e., with 8 R and 8 B voters in each district.
-   In the sweetheart puzzle, the user should try to create 2 R districts and 2 B districts where all districts are
    as uncompetitive (lopsided) as possible.
-   In the packing puzzle, the user should try to create 1 R district and 3 B districts with the 3 B districts as safe as possible.
-   In the cracking puzzle, the user should try to create 3 R districts and 1 B district with the 3 R districts as safe as possible.

## Step 4: Clean Up

-   Draw a thicker-than-between-cells black border around each district.
-   Fill the voter circles with the colors (red, blue) and use white reversed text for the 'R' and 'B' labels in them.
-   If 3 districts have been drawn completely, automatically draw the 4th district as the remaining cells.
-   Add a Map Colors / Partisan Lean toggle -- partisan lean is the current red/blue coloring; map colors should use the district
    colors.
-   The `Home` buttons on the puzzle and takeaway pages go to https://alecramsay.github.io/redistricting-workshop/lessons/ instead of https://alecramsay.github.io/redistricting-workshop/.

As for nudges:
-   Competitive puzzle: With this PG, one can draw 4 8-8 perfectly competitive districts.
-   Sweetheart puzzle: With this PG, one can draw 2 11-5 Red districts and 2 11-5 Blue districts.
-   Packing puzzle: With this PG, one can draw 3 11-5 Blue districts and 1 16-0 Red district.
-   Cracking puzzle: With this PG, one can draw 3 9-7 Red districts and 1 11-5 Blue district.
-   Note: a 9-7 Red district has 9 Red voters and 7 Blue voters; an 11-5 Blue district has 11 Blue voters and 5 Red voters.

## Step 5: More Clean Up

-   Add exterior district borders.
-   Make district borders thicker.
-   Make voter circles less intense.
-   When coloring districts by partisan lean, change the color dynamically based on how many Red and Blue voters in the district
    after each assignment.
-   The Home buttons issue noted above is not fixed yet.