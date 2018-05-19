The aim of this project is to use D3 to translate geoJSON into valid SVG path elements.

Methods used:

**d3.geoPath()** - it returns a function which takes geoJSON data and translates it into an SVG path command.

Structurally similar to d3.pie, d3.histogram, d3.arc.

Path elements are than appended to the SVG element.