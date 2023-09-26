---
toc: true
comments: false
layout: post
title: 3D Aframe
description: gy
type: plans
courses: { compsci: {week: 5} }
--- 
<html>
    <head>
        <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
    </head>
      <head>
    <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-box position="1 4.5 -7.5" rotation="0 0 0" color="#000000"></a-box>
      <a-sphere position="0 1.25 -5" radius=".75" color="#F4AB02"></a-sphere>
      <a-cylinder position="1 0.75 -8" radius="0.5" height="7.5" color="#FFC65D"></a-cylinder>
      <a-plane position="1 4.5 -7.5" rotation="0 0 -90" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-sky color="#28E9EF"></a-sky>
    </a-scene>
  </body>
</html>