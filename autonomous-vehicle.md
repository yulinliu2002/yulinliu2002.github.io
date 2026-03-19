---
layout: default
title: Autonomous Vehicle Robot
---

<section class="project-hero">
  <p class="section-label">PROJECT</p>
  <h1>Autonomous Vehicle Robot</h1>
  <p class="hero-subtext">
    A lane-following robotic vehicle integrating perception, onboard compute, and AI-assisted autonomy for real-time navigation.
  </p>
  <p>
    <a href="https://github.com/JL2200/mae148_group8" target="_blank" class="button">GitHub Repository</a>
    <a href="/" class="button button-secondary">Back Home</a>
  </p>
</section>

<section class="project-detail">
  <h2>Challenge</h2>
  <p>
    Create a lane-following autonomous vehicle capable of real-time navigation using onboard sensing and compute hardware.
  </p>

  <h2>Solution</h2>
  <ul>
    <li>Integrated <strong>Jetson Nano</strong>, <strong>Oak-D camera</strong>, <strong>Point One GPS</strong>, and <strong>LiDAR</strong> into a custom robotic platform.</li>
    <li>Used <strong>ROS2</strong> and <strong>DonkeyCar</strong> for controls, perception, and communication.</li>
    <li>Built an API layer to incorporate <strong>ChatGPT</strong> for dynamic rerouting and diagnostics.</li>
  </ul>

  <h2>Result</h2>
  <ul>
    <li>Recorded <strong>98% lane-keeping accuracy</strong> over <strong>10 test runs</strong>.</li>
    <li>Reduced reroute latency to <strong>under 200 ms</strong>, completing <strong>5 laps</strong> at an average speed of <strong>1.2 m/s</strong>.</li>
  </ul>

  <figure>
    <img src="/images/AutoCar/github_photo.jpg" alt="TranquiBot with sensor suite">
    <figcaption><em>TranquiBot with sensor suite</em></figcaption>
  </figure>

  <figure>
    <img src="/images/AutoCar/group photo.jpg" alt="Team with TranquiBot after demo">
    <figcaption><em>Team after final demo</em></figcaption>
  </figure>
</section>
