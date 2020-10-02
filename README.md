# three-trackballcontrols

[![NPM](https://nodei.co/npm/three-trackballcontrols.png)](https://www.npmjs.com/package/three-trackballcontrols)

![Dependency Badge](https://david-dm.org/jonlim/three-trackballcontrols.svg)

A module for using THREE.TrackballControls with nodejs

# Setup and Installation

## Installation

`npm install three-trackballcontrols` or `yarn add three-trackballcontrols`

## Usage

### Using as module

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

### Using with CDN / static hosted three.js

Example uses [JSDelivr](https://www.jsdelivr.com/package/npm/three-trackballcontrols) version, look up the latest URL for using with static hosting.

```html
<script type="module">
  import TrackballControls from 'https://cdn.jsdelivr.net/npm/three-trackballcontrols@0.0.8/index.min.js';

  // Assumes that a `camera` and `renderer` initialized.
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
</script>
```

# To-Dos

* Testing