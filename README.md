# Processing
- https://jamieshi.github.io/processing/
- this is my notes for Coding Challenges of Processing from https://thecodingtrain.com/CodingChallenges/

### 1. Starfield (Processing)
##### 12/27/18 3:28 PM
- how to create 3D illusion in a 2D space **without** 3D library (`P3D`)?
- key concept: far items are smaller; far items move slower
    
      // z decreases, the star moves more quickly
      float sx = map(x / z, 0, 1, 0, width/2);
      float sy = map(y / z, 0, 1, 0, height/2);;
      float r = map(z, 0, width/2, 16, 0);
      ellipse(sx, sy, r, r);

### 2. Menger Sponge (Processing)

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


### 3. The Snake Game (P5)
- similar to Tetris I wrote before. several edge cases
- introduction to P5

### 4. Purple Rain (Processing)
- not watched since I don't like the final result

### 5. Space invader (P5)
- not watched, too long

### 6. Mitosis Simulation (P5)
- **canvas** (by pixel) vs. **dom** (by element)
- optional argument to constructor 
- Deep and Shallow Copy in Javascript
- Recursion -> add objects to list -> may want to iterate from back to avoid infinite loop


### 7 - 9. Solar System, 2D, 3D, texture (Processing)
- cross product - perpendicular
- 3D texture
	- `PShape a; shape(a);`
- object shines instead of point light?

### 10. Maze Generator (P5.js) (algorithm)
- Depth-first search - stack
- backtracking

### 11. 3D terrain generation with Perlin noise (Processing)
- Perlin noise: random smooth number 
	- `noise(x,y)` as `z` value

### 12.  Lorenz Attractor (Processing)
- differential equation(s) 

### 13.  Reaction Diffusion Algorithm (p5.js)
- http://www.karlsims.com/rd.html
- convolution 
- grid & next grid (swap)
	- show color based percentage of cell A & B 
	- **Laplacian** function (gradient & divergence)

### 14. Fractal Tree
- 
