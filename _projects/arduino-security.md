---
layout: page
title: arduino security
description: Distance sensor and arduino used to scan room, detect changes, and create ASCII map.
img: assets/img/arduino-security.jpg
importance: 5
category: academic
---

I programmed an Arduino security system to scan the room and detect any changes using a distance sensor mounted to a stepper motor, as part of the university subject Mechatronics 2. An LCD shield was used to interface with the system and switch between calibration mode, security mode, and mapping mode.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/map.png" title="Comparison of map generated in mapping mode and polar plot of distance readings" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Comparison of map generated in mapping mode and polar plot of distance readings.
</div>

Mapping mode scanned the room and created an ASCII map of occupied and unoccupied cells. To accomplish this, I created an algorithm that iterated over each cell of the map, and converted the location of the cell to polar coordinates. The angle of the cell was used to find the distance reading taken at the closest angle. The distance of the cell was then compared to the distance sensor reading. If the cell was closer than the sensor reading, it was counted as unoccupied, and if the cell was further away, this meant it was occupied (or behind an object). By generating the map iterating cell by cell, I was able to overcome the memory limitations of the Arduino by printing the map as it was calculated instead of storing the whole map in memory.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <div class="iframe-container">
            <iframe width="700" height="394" src="https://www.youtube.com/embed/kGq7JqLd3MY" title="YouTube video player" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
    </div>
</div>
<div class="caption">
    Video demonstrating the mapping function and explaining the algorithm behind it.
</div>