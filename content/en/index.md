---
seo:
  title: Pedro Pathing Documentation
  description: Pedro Pathing leverages Bézier curve generation to produce smoother, faster, and more efficient trajectories for FTC autonomous navigation.
---

::u-page-hero
#title
Pedro Pathing

#description
Unlike conventional pathing systems such as RoadRunner, Pedro Pathing leverages Bézier curve generation to produce smoother, faster, and more efficient trajectories.

Its primary focus is on enhancing the adaptability of robots during autonomous operation by reacting dynamically to environmental changes, reducing error margins, and ensuring optimal path execution.

#links
  :::u-button
  ---
  color: neutral
  size: xl
  to: /en/getting-started/introduction
  trailing-icon: i-lucide-arrow-right
  ---
  Get Started with Pedro Pathing
  :::

  :::u-button
  ---
  color: neutral
  icon: simple-icons-github
  size: xl
  to: https://github.com/Pedro-Pathing
  variant: outline
  ---
  Star on GitHub
  :::
::

::u-page-section
#title
Features

#features
  :::u-page-feature
  ---
  icon: i-lucide-route
  to: /en/reference/beziercurves
  ---
  #title
  [Bézier Curve]{.text-primary} Path Following

  #description
  Pedro Pathing uses Bézier curves for smooth, efficient trajectories. The Weierstrass Approximation Theorem guarantees that any continuous curve can be approximated to arbitrary precision.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-target
  to: /en/tuning/pids
  ---
  #title
  [PIDF]{.text-primary} Control System

  #description
  Three independent PID controllers for translational, heading, and drive correction. Supports single or dual PID systems for fine-tuned performance.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-compass
  to: /en/tuning/localization
  ---
  #title
  Multiple [Localizers]{.text-primary}

  #description
  Supports drive encoders, two-wheel, three-wheel, three-wheel + IMU, goBILDA Pinpoint, and SparkFun OTOS localizers out of the box.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-zap
  to: /en/reference/drive-vector-algorithm
  ---
  #title
  [Fast]{.text-primary} Path Execution

  #description
  Pedro Pathing uses four vectors to calculate optimal wheel powers, with centripetal force correction for accurate curved path following.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-map
  target: _blank
  to: https://visualizer.pedropathing.com
  ---
  #title
  Web-Based [Visualizer]{.text-primary}

  #description
  A no-code, web-based path generator and visualizer that can export code for paths. Design your autonomous routines visually and generate code automatically.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-shield-check
  to: /en/reference/callbacks
  ---
  #title
  [Path Callbacks]{.text-primary}

  #description
  Define custom callbacks that execute at specific points along your path. Support for parametric, temporal, and pose-based triggers for arm actions and more.
  :::
::
