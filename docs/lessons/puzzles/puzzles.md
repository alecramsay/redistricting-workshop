---
layout: default
title: Redistricting Puzzles — Instructions
---

[← Home](../../)

# Redistricting Puzzles

This exercise lets you explore how single-member district (SMD) lines control the translation of votes
into seats. 

You'll draw maps for a simple state with 4 districts.
The state is an 8x8 grid of 64 voters: 32 who vote Red (R) and 32 who vote Blue (B).
The arrangement of the voters in the state is fixed: the state's "political geography" [^1].
Because the district lines can change though, different maps can have very different characteristics, including:

- **Proportional** — 2 Red-leaning-but-somewhat-competitive districts and 2 similar
  Blue-leaning districts
- **Sweetheart** — 2 safe Red districts and 2 safe Blue districts
- **Packed** — Red voters "packed" into 1 district, so Blue wins the other 3
- **Cracked** — Blue voters "cracked" across 3 Red-winning districts, so Blue only wins 1
- **Competitive** — 4 perfectly competitive districts

You will draw a map with each of those outcomes.

For your maps to be valid, they must satisfy 3 requirements:

- **Complete** — all 64 voters must be assigned to a district
- **Equal Population** — each district must have exactly 16 voters, and
- **Contiguous** — the districts must all be contiguous, meaning that
  every voter in a district is adjacent to another voter in the same district
  (shares an edge, not just a corner)

When assessing the partisan outcome of a map, 
a district will be won by Red if it has 9 or more Red voters, by Blue if it has 9 or more Blue voters. 
A district with exactly 8 Red and 8 Blue voters is up for grabs, i.e., is perfectly competitive.


## The Applet

To open the map-drawing applet, click on this link:
[Puzzles](play.html){:target="_blank" rel="noopener"}.
It will open in a new tab, so you can easily switch back here to read the documentation below.

When you open the applet, you'll see several things:

- A **Puzzle** picker dropdown at the top, where you can select which puzzle to solve.
  The choices are the 5 scenarios described above: Proportional, Sweetheart, Packing, Cracking, and Competitive.
- A **View** selector below that, where you can choose between Map Colors (the colors of the districts) and 
  Partisan Lean (whether the district will be won by Red or Blue).
  The more a district is leaning toward one party, the darker that party's color will be in the Partisan Lean view.
- The next lines describes the goal for the puzzle along with a hint about what is possible for that scenario.
- Below that are a **Districts** panel (on the left) and a **Map** (on the right).
- The map starts off empty with no voters assigned to any district. 
  The letter inside each grid square shows that voter's preferred party (R:Red or B:Blue).

To assign a voter to a district, first click on a row in the Districts panel to select the district, 
then click voters on the Map to assign them to that district. 
Note: Clicking a voter already in the selected district *removes* it from that district, i.e., unassigns it.

As you're assigning voters to districts, the Districts panel summarizes your decisions:

- The 1st column shows the map color for each district.
- The 2nd column shows the district's number (1-4).
- The 3rd column shows the number of voters currently assigned to that district out of the required 16.
- The 4th and 5th columns show the number of Red and Blue voters currently assigned to that district, respectively.
- The 6th column indicates whether the district is contiguous (✓) or not (✗).
- When 16 voters have been assigned to a district, the 7th "Winner" column shows which party will win it.
- Finally, to remove all voters from a district at once, you can press the district's **Reset** button. 

A few things show below the Districts panel and to the left of the Map:

- A **Finish Map** button is enabled when 3 districts are complete. 
  Pressing it automatically assigns the remaining voters to the last district.
- A **Show Example Solution** button loads an example solution for the current puzzle.
  There are many possible solutions for each puzzle. These are just relatively straightforward examples.
- When you've solved a puzzle, a "Puzzle solved!" message appears below the buttons. 

Finally, to the right of the Puzzle picker, there are three buttons:

- **Reset** - clears the whole map unassigning all voters from all districts, so you can start over
- **Save** - saves the current assignments to a file, so you can load and show a complete map later or 
  save an interim partial set of assignments that you can reuse as a starting point for further mapdrawing
- **Load** - restores a saved set of assignments, so you can share solutions or pick up previous work

## Footnotes

[^1]: This political geography and the 2nd - 5th scenarios come from "Glossary" at [REDISTRICTING THE NATION](http://bit.ly/2I1JJ90).