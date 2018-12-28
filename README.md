# Processing
- https://jamieshi.github.io/processing/
- this is my notes for Coding Challenges of Processing from https://thecodingtrain.com/CodingChallenges/

### 1. Starfield
##### 12/27/18 3:28 PM
- how to create 3D illusion in a 2D space without 3D library (`P3D`)?
- key concept: far items are smaller; far items move slower
    
      // z decreases, the star moves more quickly
      float sx = map(x / z, 0, 1, 0, width/2);
      float sy = map(y / z, 0, 1, 0, height/2);;
      float r = map(z, 0, width/2, 16, 0);
      ellipse(sx, sy, r, r);

### 2. Menger Sponge

#### matrix stacks
-  Every time you do a rotation, translation, or scaling, the information required to do the transformation is accumulated into a table of numbers
-  `pushMatrix()` puts the current status of the coordinate system at the top of a memory area, and `popMatrix()` pulls that status back out

#### Menger Sponge
- https://en.wikipedia.org/wiki/Menger_sponge

#### Fractal and Recursion

		  ArrayList<Box> next = new ArrayList<Box>();
  			for (Box b : sponge) {
  			  ArrayList<Box> newBoxes = b.generate();
  			  next.addAll(newBoxes);
  			}
		  sponge = next;