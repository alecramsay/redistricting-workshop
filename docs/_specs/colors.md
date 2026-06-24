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