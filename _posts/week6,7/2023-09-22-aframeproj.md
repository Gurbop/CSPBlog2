---
toc: true
comments: false
layout: post
title: 3D Aframe
description: gy
type: hacks
courses: { compsci: {week: 5} }
--- 
<html>
    <head>
        <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
    </head>
      <head>
    <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
    <script src="https://unpkg.com/aframe-environment-component@1.3.3/dist/aframe-environment-component.min.js"></script>
  </head>
  <body>
  <a-entity environment="preset: <name of the preset>"></a-entity>
    <a-scene>
      <a-box position="1 4.5 -7.5" rotation="0 0 0" color="#000000"></a-box>
      <a-sphere position="0 1.25 -5" radius=".75" color="#F4AB02"></a-sphere>
      <a-cylinder position="1 0.75 -8" radius="0.5" height="7.5" color="#FFC65D"></a-cylinder>
      <a-plane position="1 4.5 -7.5" rotation="0 0 -90" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-sky color="#28E9EF"></a-sky>
    <!-- Car -->
    <a-entity id="car" position="0 1 0">
      <!-- Body -->
      <a-box position="0 0.5 0" width="2" height="1" depth="4" color="blue"></a-box>
      <!-- Wheels -->
      <a-cylinder position="-0.8 0.2 1.8" rotation="0 0 0" radius="0.3" height="0.2" color="black"></a-cylinder>
      <a-cylinder position="0.8 0.2 1.8" rotation="0 0 0" radius="0.3" height="0.2" color="black"></a-cylinder>
      <a-cylinder position="-0.8 0.2 -1.8" rotation="0 0 0" radius="0.3" height="0.2" color="black"></a-cylinder>
      <a-cylinder position="0.8 0.2 -1.8" rotation="0 0 0" radius="0.3" height="0.2" color="black"></a-cylinder>
    </a-entity>
    <!-- Controls -->
    <a-entity id="controls" position="0 1.6 0">
      <a-plane position="0 0 0" rotation="-90 0 0" width="2" height="2" color="transparent" cursor></a-plane>
    </a-entity>
    </a-scene>
      <script>
    document.addEventListener('keydown', function(event){
      var car = document.getElementById('car');
      var position = car.getAttribute('position');
      switch (event.key) {
        case 'ArrowUp':
          position.z -= 0.1;
          break;
        case 'ArrowDown':
          position.z += 0.1;
          break;
      }
      car.setAttribute('position', position);
    };
  </body>
</html>