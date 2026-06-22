# Beta Feedback

These notes describe changes to make, based on feedback from Beta testers.

## First User

-   Pull the actual puzzles out from the instructions and into a separate dedicated page.
-   Add a link to this puzzles page from the instructions page. Open this new puzzles page in a new tab 
    so that users can easily switch back and forth between the instructions and the puzzles.

-   On the puzzles page, frame the district selector in a box of similar weight to the exterior border of the map, 
    so it's defined visually as distinct from the map.
-   Include the district results summary in the box.
-   In the district selector, add a reset button on each district that unassigns all voters from that district.
-   Label the district selector "Districts" and the map "Map".

-   Make the completion congratulations message non-modal and off to the side or below the map, 
    so users can still see the completed map.
-   Make Map Colors the default coloring mode.

-   Add the ability to save/load maps (not necessarily completed), so users can show others their solutions
    or save interim solutions to work on later.

-   Get rid of the intermediate "What is gerrymandering?" page, i.e., have the instructions page be the first thing users see 
    when they click on the lesson. 

## Tweaks

-   Move the "Districts" label outside the district selector box.
-   Line the district selector box and the map box up vertically.
-   Switch the order of the View options -- Map Colors first (default), then Partisan Lean.

-   Can we allow users to name the file and specify the location when saving a map w/o a security issue? 
-   I have canonical solutions for the 5 puzzles. Can these be made available to users to load, i.e., as part of the site?

-   Make the default file name track the puzzle scenario using the same default as the canonical solutions, e.g., proportional.json.
-   Move the "Solution" button below the district selector in the space to the left of the map.
    Rename it "Show Solution".
-   What is the "Warning: this site" message on Save about?

-   Showing the solution shouldn't result in the "Puzzle solved!" message.
-   Make the default location for saving/loading maps be the downloads folder.

## Bugs

-   When you load an example solution, clicking on a voter in the selected district results in the completion message,
    as opposed to unassigning it from the district (leaving it unassigned).
-   If a district has more voters than the target number, clicking on one of those voters doesn't unassign the voter from the district
    leaving them unassigned. Instead, it assigns them to some other (next?) district.
-   The correct behavior is always that clicking on a voter should (a) unassign the voter from the district if the selected district
    is the same as the assigned district and (b) assign the voter to the selected district if the selected district is different from the assigned district.
-   Review this assign/unassign behavior and interactions with loading example solutions. 

## More Tweaks

-   Change the "Show Solution" button text to "Show Example Solution".
-   Make the instructions page a Markdown file, so it's easier to edit and format.
-   Add a bounding box underneath the district selector and to the left of the map.
    Make it fill that space with the same margins.
    Show the "Show Example Solution" button in this box, and move the completion message to this box as well.