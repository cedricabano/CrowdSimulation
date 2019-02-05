# CrowdSimulation
## Overview
This project was initially developed jointly with @KevinWu97 for a group project for CS 442: Game Science.  The goal of this project is to develop tools and resources to be used by building designers to test escape route availability and safety in a disaster scenario.  Using Unity, we developed an escape simulator for multiple agents with limited knowledge, implementing features which added to the realism of the scenario.  This includes imperfect memory retention, primacy and recency, and limited communication.  The simulation developed in class exists as a limited proof of concept, as due to the time constraints of the class we were unable to properly develop external features to make it playable/interactive.  The original project is located [here](https://github.com/dodecaphobia/CS442-Group-17) and cannot be further developed, as it is set to be uploaded to a Rutgers website (URL pending).

This project intends to expand the depth and scope of the features currently implemented and develop an interactive interface in which this could be utilized.

## Features
The simulator spawns agents on a pre-generated map with preset nodes at designated spawn points.  These agents will attempt to move to the exit, but will do so with an imperfect knowledge of the map which expands with exploration.  Upon entering a certain radius of another agent, each agent will attempt to communicate - with probabilistic success based on social variables within each agent - and if successful, will query the other agent for the best path to the exit.  Agents will convey this information over time and will stop communicating if the radius of communication is exited; for the current implementation, agents will stop moving during interaction, to facilitate this mechanic.

The simulated agents retain an imperfect knowledge of the map which shifts based on experience.  We implemented primacy and recency as heuristic effects affecting recall of nodes, affecting all forms of queries regarding paths to the exit.

## Current Issues
* Due to time constraints, map design was kept to a minimum, with a focus on feature implementation for proof of concept.  Later updates faced significant issues due to inherent slowness of manual generation of map elements, resulting in slower feature testing.
* There is currently no interactive interface with which to adjust variables (e.g. social factor, variables for primacy/recency, etc.).  This not only delays development/testing of features but also limits the effectiveness at satisfying the goals of this project, namely to create tools to be used during building design.
* Limited motive complexity of agents prevents accurate response simulation.  A person in a disaster scenario, while typically aiming to escape with their lives, may possess different motives, or may execute different strategies to the same end.  As such, the simulator is not currently geared to providing an accurate simulation of typical escape scenarios, and is inequipped to analyze different disaster scenarios (e.g. active shooter scenarios).

## Roadmap
### Testing
* Procedural map generation for testing purposes.
* Interactive interface to adjust individual variables for testing purposes.
### Implementation
* Interactive interface to allow for map construction by user.
* Automated graph generation from map data.
* Behavior trees to more accurately model behavior.

## Credits
I would like to thank my partner, @KevinWu97, without which this project would not have gotten of the ground.  I would also like to thank Mubbasir Kapadia for his guidance and contributions to the project, and for designing the framework of the class in which this project was developed.
