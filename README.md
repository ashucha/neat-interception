# Optimization of Target Interception via NEAT

This project aims to develop an optimal target interception algorithm for small unmanned aerial systems (sUAS) via the NEAT algorithm.

## Motivation

The adoption of sUAS into various applications, including defense, search and rescue, agricultural monitoring, and payload delivery has often relied primarily on human operators to pilot these systems. In recent years, there has been a rapid transition towards a reliance on autonomous aerial vehicles to conduct such missions. One application of sUAS that is relevant across these various fields is autonomously navigating an aircraft towards another moving (perhaps aerial) target. For ease of explanation, the military applications of such technology will be considered for case studies.

Consider, for example, utilizing autonomous drone swarms to monitor and investigate airspace incursions. Here, endurance and speed are necessary for loitering/detection and interception respectively. Being such a high-priority mission as safeguarding airspace, the latter portion of this mission is of paramount importance and must be executed with great precision, especially if a threat is confirmed and must be eliminated. Thus, an optimal interception algorithm is necessary that maneuvers towards a target with great speed, accuracy, and precision. Such is the mission of this project.

Initially, this project will consider navigation in two dimensions with starting input parameters of target position and velocity and interceptor position and velocity and an output of interceptor acceleration. It will also assume that the target is navigating on a steady trajectory. The parameters will be iteratively improved via the NEAT algorithm to find optimal values for quick, accurate, and precise target interception.

Later, more complexity will be added to the algorithm, including navigation in three dimensions and a target that navigates in an unpredictable manner. Eventually, the hope for this project is that it achieves a result that is more optimal than the proportional navigation algorithm, i.e. a lower time to target. If this result is achieved, then the bar will be raised to hopefully surpass more complex and accurate algorithms such as augmented proportional navigation.

## Rationale

The motivation behind using NEAT to optimize autonomous interception is guided by the hypothesis that using such an unsupervised approach could yield more favorable outcomes than existing approaches that utilize human intuition. It was inspired by the simulation-based method that SpaceX used to autonomously navigate its Starship booster back towards the launch tower and be caught by two robotic arms. According to engineers involved in designing the algorithm, they conducted a large number of simulations using a evolutionary reinforcement learning approach whereby the algorithm would seek to emulate more successful control algorithms and disregard less successful ones. If this approach emulated standard evolutionary approaches, then these more successful algorithms would "reproduce" with one another, combining their various parameters with preference given to the more successful algorithm's traits. Theoretically, this should yield an increasingly successful set of algorithms, and after multiple iterations, the most successful candidate(s) would be chosen as the final algorithm(s).

Thus, considering that an autonomous control algorithm for aerospace applications could be developed using an evolutionary approach, this project will follow the same method in hopes of developing a more optimal autonomous interception algorithm.
