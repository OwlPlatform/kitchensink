# kitchensink
This repository incorporates most components and language interfaces into a single repository. This can serve as a quick start for someone who wants to get started with and Owl Platform deployment but who isn't yet familiar with all of the different components.

Keep in mind that the individual submodules included in the subdirectories of the kitchen sink may have their own licences and may have different authors.

After downloading this repository you will need to initialize the submodules:
```
git submodule init
git submodule update
```

## What is Owl Platform?
Owl Platform is a middleware for internet of things deployments. It allows entry points into the system for self-aware sensors that have some knowledge of their role in the system and simple sensors that just transmit data. Information is associated with real-world objects through a world model layer. Self-aware sensors and stand-alone software, called solvers, then analyses lower-level data and modify object attributes in the world model. Applications access the world model to present information to human consumers. Higher-level software can also access information in the world model created by other solvers in order to add more abstract information into the world model.

## An Example
TODO

## Advantages
* Supports a variety of sensors, both self-aware and simple, including transmit-only sensors through the *aggregator*. This reduces the code needed to add new sensors to the system.
* The *world model* provides a virtual abstraction of your physical space with URI-based named objects with sets of attributes.
* Provenance of data. Each attribute's creation time and creator is tracked so you can easily review the history of your system and replay past events for testing or auditing.
* Minimized exposure areas. Layers are divided into *sensing*, *solving*, and *application*. Software can participate in as many layers as desired, but can choose to only participate in one, again reducing the complexity of adding new sensors into a system.

# Getting Started
Each subdirectory in this repository imports different submodules that may be of use. Some subdirectories are broken down by language. C++ components require CMake and gcc, java components require mvn and the jdk, and Ruby components require ruby and gems.

To get a minimum system running you will need to install the c++ libraries in the protocols directory and the aggregator and world model from the core directory.

A setup guide is included in the *setup-guide" submodule. The setup guide is for a particular demo done with Owl Platform, but you may find it useful to read through some of the installation steps. The demo assumes that you have the Tomcat web server installed.

The contents of each subdirectory are as follows:

## protocols
This directory contains submodules for the GRAIL network protocol written in different languages. These are used by the core components and by apps and tools to communicate with the core components over the network.

## core
This directory contains the core components of a deployment system. These components are the *aggregator* and the *world model*.

## examples
This directory contains some examples of interactions with the aggregator and world model in a variety of languages.

## apps
Existing apps created by different people.

## tools
Tools that simplify management of a running system.
