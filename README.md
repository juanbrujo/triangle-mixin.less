#triangle-mixin.less

`Less CSS triangle mixin`, create any kind of triangles with ease.

### Demo: 
[Codepen.io Demo](http://codepen.io/juanbrujo/pen/dleuF)

###Types of triangle
	top
	bottom
	left
	right
	topright
	topleft
	bottomright
	bottomleft

###Use:

	.triangle(direction,width,height,color);
	
By default it creates an isosceles triangle, but  you can make scalene triangles too, just play with different values for `width`/`height`.

###Example:

	@square: 50px;
	@color: red;
	selector {
	  .triangle(bottomright,@square,@square,@color);
	}