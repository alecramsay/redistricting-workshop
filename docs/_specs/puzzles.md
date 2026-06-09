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