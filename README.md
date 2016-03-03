# three-trackballcontrols

![NPM](https://nodei.co/npm/three-trackballcontrols.png)

![Dependency Badge](https://david-dm.org/jonlim/three-trackballcontrols.svg)

A module for using THREE.TrackballControls with nodejs

# Setup and Installation

## Pre-requisites

* Three.js installed via npm (`npm install three`)

## Installation

`npm install three-trackballcontrols`

## Usage

Assuminng that you're using `three-trackballcontrols` in the same code as `three`,
all you have to do is require it right after `three`.

`var THREE = require('three');`  
`var TrackballControls = require('three-trackballcontrols');`

And when you're setting up your camera:

`this.controls = new TrackballControls( this.camera, this.renderBox );`

Then you're off to the races!

# To-Dos

* Testing