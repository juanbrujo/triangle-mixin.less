#triangle-mixin.less

![triangle-mixin.less](https://photos-6.dropbox.com/t/0/AAB6RGNGT3RdtUrDsE7fhJWYvZ3s4bLssltFcCCQWmA-Dw/12/3522/jpeg/1024x768/3/1394553600/0/2/less-triangle.jpg/7-Gh2O7w7kKriRYaNODKgaWLSiFJkPzc9C1MRySTr5c)
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