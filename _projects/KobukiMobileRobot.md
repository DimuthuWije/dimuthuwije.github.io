---
layout: page
title: Kobuki Mobile Robot
description: ROS2 Based Mobile Robot Control
img: assets/img/projects/KobukiBanner.jpeg
importance: 7
category: Selected Projects
related_publications: false
slug: ros2-mobile-robot-control
---

## ROS2 Mobile Robot Motion Control

This project involved the practical implementation of ROS2 based mobile robot control using a Kobuki differential-drive platform.

The work focused on understanding robotic software architectures, ROS2 communication concepts, velocity command generation, and feedback-based control using real robotic hardware. A ROS2-based control workflow was implemented to command the robot through predefined trajectories while utilizing odometry feedback for closed-loop motion control.

---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">

        <video
            controls
            preload="metadata"
            poster="/assets/img/projects/KobukiBanner.jpeg"
            class="img-fluid rounded z-depth-1"
            style="width:100%; aspect-ratio:16/9; background:#000;">
            <source src="/assets/video/Kobuki.mp4" type="video/mp4">
        </video>

    </div>
</div>

<div class="caption">
    Kobuki mobile robot executing programmed motion commands using ROS2.
</div>

---

## Mobile Robot Platform

The experiments were performed using a Kobuki differential drive mobile robot platform with ROS2 compatible control interfaces.

The platform provided access to velocity commands, odometry feedback, and sensor information through ROS2 topics, enabling practical experimentation with robot communication and feedback-based control.

<div class="row justify-content-sm-center">

    <div class="col-sm-6 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/KobukiTop.jpeg" 
        title="Kobuki mobile robot platform" 
        class="img-fluid rounded z-depth-1" %}

    </div>

    <div class="col-sm-6 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/KobukiBottom.jpeg" 
        title="Kobuki robot underside" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    Kobuki differential-drive mobile robot platform used for ROS2-based motion control experiments.
</div>

---

## ROS2 Communication Architecture

The robot was controlled using ROS2 publisher–subscriber communication.

Keyboard-based teleoperation commands were converted into velocity messages and published through the `/commands/velocity` topic. The Kobuki driver node subscribed to these commands, interfaced with the robot base controller, and published sensor and odometry feedback.

The main ROS2 nodes involved were:

- `/kobuki_keyop_node` - Generates velocity commands through ROS2 teleoperation
- `/kobuki` - Kobuki driver node responsible for robot control and sensor feedback

<div class="row justify-content-center">

    <div class="col-sm-8 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/RQTGRAPH.svg" 
        title="ROS2 node and topic communication graph" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    ROS2 communication graph showing the interaction between command generation and the Kobuki driver node.
</div>


<div class="row justify-content-center">

    <div class="col-sm-10 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/ROS2Nodes.png" 
        title="ROS2 Kobuki node publishers and subscribers" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    ROS2 node information showing the available publisher and subscriber interfaces of the Kobuki driver.
</div>

---


## Odometry-Based Motion Control

A custom ROS2 Python controller was implemented to execute predefined trajectories using feedback from the robot's odometry.

The controller subscribed to the `/odom` topic to estimate robot position and orientation while publishing velocity commands through `/commands/velocity`. This enabled distance-based motion control instead of relying only on fixed timing delays.

The implementation involved:

- ROS2 publisher and subscriber communication
- Odometry feedback processing
- Position-based distance estimation
- Orientation extraction from quaternion data
- Closed-loop trajectory execution

The ROS2 communication interfaces were configured as:

```python
self.publisher = self.create_publisher(
    Twist,
    '/commands/velocity',
    10
)

self.subscription = self.create_subscription(
    Odometry,
    '/odom',
    self.odom_callback,
    10
)
```

Robot position and orientation feedback were extracted from odometry messages:

```python
def odom_callback(self, msg):

    self.x = msg.pose.pose.position.x
    self.y = msg.pose.pose.position.y

    q = msg.pose.pose.orientation

    siny_cosp = 2.0 * (q.w*q.z + q.x*q.y)
    cosy_cosp = 1.0 - 2.0 * (q.y*q.y + q.z*q.z)

    self.angle = math.atan2(
        siny_cosp,
        cosy_cosp
    )
```


Using these motion primitives, the robot was commanded to execute a square trajectory consisting of repeated forward movements and 90-degree turns:

```python
def move_square(self):

    for side in range(4):

        self.move_forward(0.375)
        self.turn(90)
```

The project provided practical experience with ROS2 nodes, topics, publishers, subscribers, robot drivers, odometry-based feedback control, and real-world operation of a differential-drive mobile robot platform, supporting future work in autonomous navigation and robotic systems.