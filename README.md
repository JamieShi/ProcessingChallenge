# Processing
- https://jamieshi.github.io/processing/
- this is my notes for Coding Challenges of Processing from https://thecodingtrain.com/CodingChallenges/

### 1. Starfield
- how to create 3D illusion in a 2D space with `z`?
- key concept: far items are smaller; far items move slower
    
      // z decreases, the star moves more quickly
      float sx = map(x / z, 0, 1, 0, width/2);
      float sy = map(y / z, 0, 1, 0, height/2);;
      float r = map(z, 0, width/2, 16, 0);
      ellipse(sx, sy, r, r);
