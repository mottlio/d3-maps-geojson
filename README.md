The aim of this project is to use D3 to translate geoJSON into valid SVG path elements.

Methods used:

**d3.geoPath()** - it returns a function which takes geoJSON data and translates it into an SVG path command.

Structurally similar to d3.pie, d3.histogram, d3.arc.

Path elements are than appended to the SVG element.

**TopoJSON** - instead of coordinates uses arcs - this reduces duplication of data (when two neighbouring elements are drawn no need to duplicate coordinates of their borders). Same data can be encoded more succintly resulting in a smaller file size.

For example, these could be sides of rectangles:

"arcs": [
    [
      [ 0,  100 ], //this is where the arc starts
      [ 100, 0 ] //this is where it ends
    ],
    [
      [ 100, 100 ],
      [ 0, -100 ]
    ],
]

**TopoJSON cannot be translated directly by D3**

TopoJSON -> geoJSON -> SVG path

For TopoJSON -> geoJSON the TOPOJSON LIBRARY is used (must be included in index.html file via a <script> tag)