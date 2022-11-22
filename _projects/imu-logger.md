---
layout: page
title: imu data logger
description: Robust system to autonomously record sensor data from an IMU to a single board computer using C++.
img: assets/img/imu2.png
importance: 1
category: professional
---

In my work at Jenkins Engineering Defence Systems, I designed a system to autonomously record sensor data from an inertial measurement unit (IMU) to a single board computer using C++. The system needed to be robust, as it would be left unmonitored for months at a time, and also needed to be resilient to power outages.

Power outages posed a data corruption risk, and in the worst case could corrupt the entire filesystem. To reduce this risk, I set the file system to read only at all times, unless I was writing data. I also created a service to start the program automatically when power was available again, and ran experiments to confirm the system’s resilience to outages.

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/imu.png" title="IMU axes" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
