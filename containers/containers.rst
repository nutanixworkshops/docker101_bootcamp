.. _containers:
.. title:: Introduction to Docker

Containers - What are they?
---------------------------

.. note::
   Estimated amount of time: **10 minutes**

Using Google to find the definition of containers, you will get a lot of hits. One of the most common hits is related to Docker. Using this engine, as set by the requirements of John’s organization, their websites shows the following definition:
“A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.


*"Container images become containers at runtime and in the case of Docker containers - images become containers when they run on Docker Engine. Available for both Linux and Windows-based applications, containerized software will always run the same, regardless of the infrastructure. Containers isolate software from its environment and ensure that it works uniformly despite differences for instance between development and staging.” (https://www.docker.com/resources/what-container)"*

Wow that is a lot of text. But what does this mean? In short it can be explained as follows:
“Containers are constructs that have enough binaries from an operating system (Windows or Linux) and supporting binaries to run one or more applications in an isolated environment”.
Ok so they are a kind of VMs? Well no! VM runs a full blown Operating System whereas containers only have parts of the Operating System. Just enough to run applications. The below image might be more explanatory.

.. figure:: images/container.png

Pros on containers
++++++++++++++++++

Hmm ok, but why do I want to use containers and not normal VMs as that is what I am used to? Again on Google there are a lot of hits on this question. Putting some of them together leads to the following list (none extensive) of Pros:

#. Low on resources consumption
#. Small and therefore easy and faster to deploy
#. Can run on anything that supports the Docker engine including Cloud
#. Immutable constructs from application’s point of view. Once in a container, the application will ALWAYS behave the same independent of the Operating System.
#. Isolation of application on the same host.

Cons on containers
++++++++++++++++++

Ok, but what are situations that won’t work with containers? Using Google again, with a a lot of hits, the below list is summing up (none extensive) Cons:

#. Use of different Operating Systems and/or kernels
#. Lot of data that needs to be stored
#. High security needs
#. More performance
#. Must have a GUI
#. Easier management
#. Run multiple applications in one container

Conclusion - based on the set requirements
++++++++++++++++++++++++++++++++++++++++++

Based on the set requirements by the organization:

#. Containerization using Docker.
#. Should be able to be “transported” to cloud platforms like AWS and GCP.
#. Changing the configuration should be outside of the container, if it can be done.
#. Changes to configuration and the web application should not be lost in case of a restart/reboot of the container.
#. A reboot of the host that serves the container should not impact the accessibility of the containerized web servers (read application).
#. Update to the containers must have:

   #) A fall back path
   #) No impact on application delivery

#. Stretched goal: deployment of the containers, when there is an update, gets automated. This needs to be investigated in a later stage **(is not part of this workshop)**.

The set requirements can be met using containerization.
