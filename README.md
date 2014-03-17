#triangle-mixin.less

![triangle-mixin.less](https://dl.dropboxusercontent.com/u/3522/less-triangle.jpg)
`Less CSS triangle mixin`, create any kind of triangles with ease.

### Demo: 
[Codepen.io Demo](http://codepen.io/juanbrujo/pen/dleuF)

###Triangles: direction
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

###Advanced
	@square: 50px;
	@color: red;
	
	.advanced {
  	  width: @square*2;
  	  height: @square;
  	  line-height: @square;
  	  background-color: @color;
  	  position: relative;
  	    	  
  	    &:after {
   		  position: absolute;
    	  left: 0;
    	  top: -@square;
    	  .triangle(top,@square,@square,@color);
  	    }
  	    &:before {
    	  position: absolute;
    	  left: 0;
    	  top: @square;
    	  .triangle(topleft,@square*2,@square*2,@color);
  	    }
	  }