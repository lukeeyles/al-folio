---
layout: page
title: aircraft interceptor
description: Control a simulated aircraft to predict location and intercept enemy aircraft in a 2D airspace.
img: assets/img/aircraft-interceptor.gif
importance: 4
category: academic
---

In Programming for Mechatronic Systems at university, a project I undertook was to use C++ with ROS to predict the trajectory of enemy aircraft and intercept them in a simulated 2D airspace. By developing an algorithm to predict the interception point, I averaged 60 intercepted within 5 minutes, exeeding the threshold for bonus marks by 50%.

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/aircraft-interceptor.gif" title="Aircraft interceptor simulation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The prediction algorithm I developed was iterative, and worked by calculating the trajectory of the enemy aircraft, and estimating the time to intercept using the distance from my aircraft to the enemy. The enemy aircraft's position was then extrapolated along it's trajectory using this time to intercept, and the new estimate of the time to intercept was calculated with the extrapolated point. This was then repeated until the difference between subsequent estimates fell under an error threshold, which would give the final interception point as the goal location for my aircraft to go to.