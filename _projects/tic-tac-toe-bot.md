---
layout: page
title: tic-tac-toe bot
description: Robot arm that plays tic-tac-toe with a person.
img: assets/img/tic-tac-toe-bot-small.gif
importance: 2
category: academic
---

For my major project in the university subject Robotics, I led a team with two others to program a Dobot Magician to play Tic-Tac-Toe against a person.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <div class="iframe-container">
            <iframe width="700" height="394" src="https://www.youtube.com/embed/gn4-HONhFDk" title="YouTube video player" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
    </div>
</div>
<div class="caption">
    Video of the team explaining the features of the system.
</div>

The project was made in MATLAB, with Peter Corke's Robotics Toolbox used to compute the forward kinematics and Jacobian, and animate the robot. A Raspberry Pi running ROS was used to control the Dobot, and commands were sent over the network using MATLAB's ROS Toolbox.

A webcam was used with MATLAB's Image Processing Toolbox to detect when the person had finished their turn, and signal the robot to play. The location the person placed their tile was detected by using a camera model to transform the 3D positions of each tile into 2D points in the image, and then sampling the image to detect the colour in each possible tile location.

Inverse kinematics of the Dobot were required to control it to pick up the tiles and place them down in the right position. The inverse kinematics of the Dobot are unique in that it has 4 joints, but only 3 degrees of freedom as the end effector always points down. This meant that the built in inverse kinematics function in Peter Corke's Robotics Toolbox couldn't be used, so a custom inverse kinematics function was developed. This custom function had the advantage of being an exact solution, making it faster than the built in function which used an optimisation approach.

This project was the largest team project I had worked on at the time, and it was challenging to coordinate the team and ensure everyone had a part to work on. As a result I learned the importance of good project planning, so that everyone is on the same page about what needs to be done and clear roles can be assigned. Without this planning, it was difficult for everyone in the team to contribute equally.