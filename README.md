# the matrix oven
Plugin for snapsvg.io, applies all svg transforms into coordinates.

## Usage example:
just call bake() on an element. It will recursively bake itself and its subelements.

	var s = Snap("#svg");
	Snap.load("mascot.svg", function (f) {
		g = f.select("g");
		s.append(g);
	}); 
	g.transform('matrix(0.75, -0.5, 0.5, -0.75, 100, 0)');
	s.select('g').bake(); 
	// -> now the transform matrix is (1,0,0,1,0,0) 
	//    and all coordinates are applied


## More options:
 * param {boolean} toCubics : use only cubic path segments
 * param {integer} dec : number of digits after decimal separator. defaults to 5

## contributions:
matrix oven is based on work by: 
 * https://gist.github.com/timo22345/9413158 
 * https://github.com/duopixel/Method-Draw/blob/master/editor/src/svgcanvas.js

