# OCTANE-API
Open Car (Mobility) Testing Automation Networked Environment API.

The OCTANE API provides facility enumeration, control, orchestration, data collection, and simulation functionality in a mobility test facility/proving ground. It provides support for creating an environment for repeatable test cases.

OCTANE is a REST web API with additional support for push/polling facility events using Socket.IO endpoints.

OCTANE was developed at University of Michigan's Mcity Test Facility to enhance the user experience while testing connected and automated vehicles.

# About Mcity
Mcity funds research and provides testing at our one-of-a-kind proving ground simulating the complexities of an urban environment, and through on-road vehicle deployments to a variety of settings in Ann Arbor and Southeast Michigan.

Mcity brings together partners from industry, government, and academia to develop the foundation for an ecosystem of connected and automated vehicles for moving people and goods. Such a system has the potential to dramatically improve safety, sustainability, and accessibility.

# Why OCTANE?
The Mcity test facility is a highly automated and connected proving ground in Southeast Michigan. Mcity developed the OCTANE API giving facility users access to develop control, orchestration, and the ability to easily run repeatable tests at the facility.

Our vision is that other facilities will implement the API standard on top of their hardware to provide a software abstraction layer of the facility. This allows mobility for tests and control scripts to move between multiple facilities that may have dissimilar hardware, and devices.

# Using OCTANE
OCTANE is a specification for an API written using OAS3.0.
The easiest way to visualize the API is by viewing the Mcity implementation on [Mvillage](https://mvillage.um.city/apidocs/)

The easiest way to edit the current version is using the [Swagger Editor](https://editor.swagger.io/?url=https://raw.githubusercontent.com/mcity/octane-api/master/api.yaml)

# Status of OCTANE
Jul 29th, 2019 - Mcity runs an implementation of the Octane API specified in this repository. The specification and implementation are both under active development. We are using api-roadmap.yaml to guide the type of functions we plan to implement.

We host both a test and production environment of this implementation for users of the test facility.
The test environment can be found at https://mvillage.um.city/apidocs. The test environment does not support Socket.IO push messages.

The next major part of our work is to finish V2X functionality and move to data collection.

Implemented:
* Intersections
* Signals
* Gates
* Crosswalks
* Rail crossings
* Facility information
* Socket IO push notifications and chat/synchronization.
* Sensor (Packages, Radar, LIDAR, Camera) enumeration.
* V2X - Experimental

Planned Development Schedule:
* 08/2019 - V2X
* 09/2019 - Sensor Data Collection / Weather / Logging / Requests
* 10/2019 - Robot Control / Segments / Lighting control / Maintenance Equipment
* 11/2019 - Scenario Storage, Playback, Status /  Weather control
* 12/2019 - UI Interface for control / First full API spec release (RON 1)

# Release schedule / numbering
The latest version of the API lives in the master branch in api.yaml

The broad road map for planned features is loosely specified in api-roadmap.yaml

Released are granted a Release Order Number (RON) and each RON will have it's own branch at time of release. 
The highest RON branch is the latest standard of the API.

* 06/27/18 - Initial spec release
* 03/01/19 - Mcity initial implementation release
* 03/16/19 - Release .0.2 with signal support and conversion to OAS3.0.
* 03/24/19 - Release .0.3 with sensor support and enhanced rail functionality.
* 05/15/19 - Release .0.4 added documentation around Socket.IO connection and Initial V2X work, Intersection Phase documentation of timing/colors.
* 07/29/19 - Release .0.6 added more V2X endpoints, socketio endpoints for V2X, favorites to management nodes, and fixes to documentation for endpoints, initial data collection enumeration. Adjusted release schedule.

# Contributing to OCTANE
To contribute to releases, submit requests through the GitHub issues feature for discussion or proposed changed via Pull Requests.

## Licensing
The OCTANE API spec is licensed through the MIT license.

## Maintainer
This API is presently maintained by @gmcguire and @tsworman
