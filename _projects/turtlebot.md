---
layout: page
title: cereal finding robot
description: Turtlebot controlled to find the right cereal box, and drive towards it.
img: assets/img/turtlebot2.png
importance: 3
category: academic
---

For the major project in the subject Sensors and Control, I led a team with two others to program a TurtleBot to look for cereal boxes, recognise the chosen box, and drive along the line normal to the box. 

MATLAB's Image Processing Toolbox was used to recognise the cereal boxes. A pinhole camera model of the TurtleBot's camera was created using the [Camera Calibration Toolbox](http://robots.stanford.edu/cs223b04/JeanYvesCalib/). This model was used to transform the image points on the cereal box into 3D space. The robot was then controlled using a P controller to rotate on the spot to the correct angle, drive towards the normal of the box, face the box, and then drive to the box.

As the team leader, I worked early in the project to plan the code structure and divide the work among the team. This was key to the success of the project as everyone was on the same page from the beginning, and everyone had a specific part of the project that they were responsible for.