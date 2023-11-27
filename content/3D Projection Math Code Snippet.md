---
tags:
  - atom
  - programming
  - graphics-programming
  - quartz-sync
  - javascript
---

This is a snippet of code I used to project an object from 3D world space into 2D screen space. It's used in a game I made where obstacles are approaching the player from the horizon.

```javascript

/*
obstacles aren't approaching in perspective:
  should move along perspective lines, rather than going straight down regardless of position
  y position on canvas should be faster as it approaches the player, instead of staying a constant speed on canvas

  we can figure out the position and rotation of the camera by noting where the horizon is on screen and how high above the ground the camera is
*/

/*
Projects a point in world space [ptX, ptY, ptZ] to screen space [x, y]
*/
function project(ptX, ptY, ptZ, camX, camY, camZ, eulerAngleX,
  eulerAngleY, eulerAngleZ, viewerX, viewerY, viewerZ) {

  var X = ptX - camX;
  var Y = ptY - camY;
  var Z = ptZ - camZ;

  // pre-compute trig values
  var cx = Math.cos(eulerAngleX);
  var cy = Math.cos(eulerAngleY);
  var cz = Math.cos(eulerAngleZ);
  var sx = Math.sin(eulerAngleX);
  var sy = Math.sin(eulerAngleY);
  var sz = Math.sin(eulerAngleZ);

  // transform from world space to camera space
  var dX = cy * (sz * Y + cz * X) - sy * Z;
  var dY = sx * (cy * Z + sy * (sz * Y + cz * X)) + cx * (cz * Y - sz * X);
  var dZ = cx * (cy * Z + sy * (sz * Y + cz * X)) - sx * (cz * Y - sz * X);

  // then transform to screen space
  var screenX = (viewerZ / dZ) * dX - viewerX;
  var screenY = (viewerZ / dZ) * dY - viewerY;

  return [screenX, screenY];
}
```

reference: https://en.wikipedia.org/wiki/3D_projection#Weak_perspective_projection