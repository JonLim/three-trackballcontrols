# three-trackballcontrols

[![NPM](https://nodei.co/npm/three-trackballcontrols.png)](https://www.npmjs.com/package/three-trackballcontrols)

![Dependency Badge](https://david-dm.org/jonlim/three-trackballcontrols.svg)

A module for using `TrackballControls` for `three.js` with NodeJS.

# Installation

`npm install three-trackballcontrols` or `yarn add three-trackballcontrols`

# Usage

Example was using `three.js` + `three-trackballcontrols` inside of a very simple React app.

```javascript
import * as THREE from 'three';
import TrackballControls from 'three-trackballcontrols';

// Assumes there is a `camera` and `renderer` initialized.
const controls = new TrackballControls(camera, renderer.domElement);

// Any manual camera changes should be done first, then update the controls.
camera.position.z = 5;
controls.update();

const animate = function () {
  requestAnimationFrame(animate);

  // Required for updating during animations.
  controls.update();
  renderer.render(scene, camera);
}
animate();
```

# To-Dos

* Support for further touch events