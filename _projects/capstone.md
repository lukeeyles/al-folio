---
layout: page
title: capstone
description: Control software for JEXO exoskeleton arm.
img: assets/img/jexo-me.gif
importance: 1
category: academic
---

My Capstone Project was the final thesis of my engineering degree, and was by far the largest project I've undertaken at university. My Capstone involved the upper limb exoskeleton robot, [JEXO](https://www.youtube.com/watch?v=kX14O9Y1GCg), which the UTS Robotics Institute developed in 2012. This robot was built to be a research platform to test control algorithms related to human-robot interaction. However, the robot’s control software became outdated, having not received any updates since 2017. It also lacked consistent documentation, making it time-consuming for newcomers to the project to develop a complete understanding of the software. There was also no way to test new software without access to the physical robot, compounding this problem. 

In this project, I updated the JEXO codebase using modern ROS features and best practice conventions to improve maintainability, robustness, and ease of use when implementing new control systems. I also analysed the theory behind the control systems implemented in the existing code, and performed a literature review to research alternative control strategies. 

Using [Gazebo simulator](https://gazebosim.org/home) together with integration from [ROS Control](http://wiki.ros.org/ros_control), I developed a simulation to enable programming and testing control algorithms without requiring access to the physical exoskeleton. The architecture of ROS Control decouples controllers from the hardware, which enables the same controllers to be used for both the real robot and the simulation. Using ROS Control's controller switching functionality, I implemented a way to seamlessly change between admittance control, end effector velocity control, and joint velocity control.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <div class="iframe-container">
            <iframe width="700" height="394" src="https://www.youtube.com/embed/6opZxjLgjLw" title="YouTube video player" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
    </div>
</div>
<div class="caption">
    Video demonstrating switching controllers on the exoskeleton.
</div>

I also created detailed documentation for the new codebase. Together with the improved modularity, this allows future controllers to be developed more easily as it reduces the time to learn and understand the control software. Overall, my work on this project greatly improved the functionality of JEXO as a research platform.

Read my full thesis <a href="/assets/pdf/Luke-Eyles-Capstone.pdf" target="_blank">here</a>.