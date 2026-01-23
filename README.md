# Modernizing ROS 2 Skills: Hacking and Orchestrating Cloud Brains, Physical Sensors, and the Network
> 

## :eyeglasses: Abstract   
The learning curve for ROS2 can be steep, often requiring the installation and resolution of diverse software dependencies across operating systems, sensors, network configurations and robotic platforms. By combining virtual machines (VMs), with their off-the-shelf, ready-to-use environments resources and modern container registry workflows, we can reduce this complexity and enables learners to focus more directly on developing ROS2 skills. This approach also offers a smoother onboarding process for participants with varying levels of technical experience. In this talk, we share hands-on insights from our hackathon, which explored a distributed setup involving two servers located in different University College London (UCL) departments --Advanced Research Computing (ARC) and Civil, Environmental and Geomatic Engineering (CEGE)-- connected via a Zero Overhead Network Protocol (Zenoh) router with 10 GbE connectivity. One server from CEGE was connected to physical sensors --laser scanners, Inertial Measurement Units, and cameras-- with data streamed through the ROSBridge suite and Zenoh. On the ARC server and platforms (unified-AI and condenser), participants worked with off-the-shelf VMs and within containerised environments running ROS 2 Humble on Ubuntu 22.04. Five to ten participants accessed live sensor data via the ROSBridge Suite to visualise streams, perform object recognition and segmentation, and analyse outputs. They experimented with network constraints by varying sample rates, data types, and file sizes, and explored the trade-off between CPU usage for core ROS 2 packages and GPU demands for intensive tasks. Lessons on containerisation for virtual machines, managing dependencies, understanding latency and bandwidth, balancing resources, and cost considerations were shared, alongside next steps and a call for collaboration to advance ROS 2 skills and infrastructure in academia.

See the link to our hackathon for further details, the discussion forum, and ways to get involved: https://github.com/UCL-CyberPhysicalSystems/hackathon-01



## :school_satchel: Slides

https://ucl-cyberphysicalsystems.github.io/fosdem2026/

## FOSDEM2026

* https://fosdem.org/2026/schedule/event/3SFYWM-hacking-cyber-physical_systems-with-ros2/


## :octocat: Clone repository
See [CONTRIBUTING](CONTRIBUTING.md) for details on clonning repo, raising issues and guidelines for contributing.

