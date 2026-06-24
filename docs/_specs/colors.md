# Colors

I want to change the district coloring.

For partisan lean, I want to use the DRA color stops noted below which depend on the Blue vote share as a [0.0 - 1.0] fraction. 
There is no competitive/tied yellow coloring.
Use 50% opacity over white for the colors, so that the map is not too dark and the voters are still visible.

For map colors, I want to use 4 CVD-friendly colors that don't include blue or red and that work well being adjacent (i.e., coloring maps).

-----
Here are the DRA color stops. This is full opacity.

// For Partisan District Scale (12 stops)

export const PartisanDistrictClassicColors = [

  '#960018',  // 

  '#960018',  // .00 <= .40

  '#FF2020',  //

  '#FF2020',  // .40 <= .45

  '#FF6060',  //

  '#FFDEDE',  // .45 <= .50

  '#DEDEFF',  //

  '#6060FF',  // .50 <= .55

  '#2020FF',  //

  '#2020FF',  // .55 <= .60

  '#00008B',  //

  '#00008B',  // .60 <= 1.0

];


According to ChatGPT, this is the same set of colors rendered at 50% opacity over white:

export const PartisanDistrictClassicColors50 = [
  '#CB808C',  // #960018
  '#CB808C',
  '#FF9090',  // #FF2020
  '#FF9090',
  '#FFB0B0',  // #FF6060
  '#FFEFEF',  // #FFDEDE
  '#EFEFFF',  // #DEDEFF
  '#B0B0FF',  // #6060FF
  '#9090FF',  // #2020FF
  '#9090FF',
  '#8080C5',  // #00008B
  '#8080C5',
];

-----
## Map colors (chosen)

4 CVD-friendly colors for coloring districts (the "Map Colors" view), drawn from
the Okabe–Ito palette. None is blue or red, so they never read as a party color,
and all four stay distinguishable under common color-vision deficiencies and when
adjacent.

These are the swatch / district-identification colors at full strength:

  '#E69F00',  // Orange
  '#009E73',  // Bluish green
  '#F0E442',  // Yellow
  '#CC79A7',  // Reddish purple

On the map they fill cells at 50% opacity over the white grid background, the same
way the partisan colors are rendered, so the voter dots stay visible:

  'rgba(230,159,0,0.50)',    // #E69F00 Orange
  'rgba(0,158,115,0.50)',    // #009E73 Bluish green
  'rgba(240,228,66,0.50)',   // #F0E442 Yellow
  'rgba(204,121,167,0.50)',  // #CC79A7 Reddish purple

Implemented in docs/lessons/puzzles/play.html as DISTRICT_BORDER (full strength
swatches) and DISTRICT_MAP_FILL (50% cell fills). The map grid has a white
background; the puzzle page background is not white, and that's OK.