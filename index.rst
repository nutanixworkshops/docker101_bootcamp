.. title:: Introduction to Docker

.. toctree::
  :maxdepth: 2
  :caption: Labs
  :name: _labs
  :hidden:

  containers/containers
  day1/day1
  day2/day2
  day3/day3
  day4/day4
  day5/day5
  day6/day6
  day7/day7

.. _getting_started:

---------------------
Scenario introduction
---------------------
Welcome to a day in the life of an administrator called John. John is working for an organization that is thinking about if it would be possible to put one of their applications, a NGINX Load balancer and some NGINX based web servers into a container based workload. Today the application consists of Virtual Machines based on the Linux Distribution Ubuntu 18.04 LTS.

.. _requirements:

Requirements
++++++++++++

John has been asked to investigate the following set requirements by the organization:

#. Containerization using Docker.
#. Should be able to be “transported” to cloud platforms like AWS and GCP.
#. Changing the configuration should be outside of the container, if it can be done.
#. Changes to configuration and the web application should not be lost in case of a restart/reboot of the container
#. A reboot of the host that serves the container should not impact the accessibility of the containerized web servers (read application).
#. Update to the containers must have:
   
   #. A fall back path
   #. No impact on application delivery

#. Stretched goal: deployment of the containers, when there is an update, gets automated.

John has no to little experience with containers and wants this investigation to also help him in getting a better understanding of containers and the workloads that can be used in this world.
To support John in his quest he has created a path to get his knowledge up and running in small steps. The path he created looks like this:

- What are containers?
- For what workloads can I use it and would it fit the set request?
- What the pre-requirements to get started with Docker?
- Can I use pre-build containers that are out there, if any?
- How can I create my own containers if the prebuilt are not solving my issues?
- How can I make the solution for LB and 1 container?
- How can I make the solution scale?
- How can I deploy new containers after there has been an update? (stretched goal)

This workshop is showing you how John steps through most of the set items in his path... 

.. note::
  The workshop can be run fully from your own laptop as it is not using any Nutanix related features. It is built to let you get familiar with Docker and Docker Swarm. The total amount of time for the workshop is a full day.
  Commands that need to be run are in **bold** so you can keep track and find them easily.


Agenda
++++++++++

- What are containers?
- Day 1 - General Docker

  + Needed resources to build the test environment
  + Installing Docker
  + Run first container
  + Container management
  + Docker usefull commands

- Day 2 - Advanced Docker

  + Change and create images/containers

- Day 3 - More advanced Docker

  + Detach files from conatiner images

- Day 4 - Connect containers together

  + Creating a loadbalancer
  + Creating Dockerfile

- Day 5 - Storing images and create a HA solution

  + Store images
  + Start of Docker Swarm

- Day 6 - Dockerfile and changing images with Docker Swarm

  + Create a new Dockerfile
  + Store the created images
  + Testing failures

- Day 7 - Scaling,rebalancing and Monitoring

  + Scale the applications
  + Rebalance the containers
  + Monitor the test environment

