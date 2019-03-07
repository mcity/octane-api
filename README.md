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
OCTANE is a specification for an API written using Swagger.
The easiest way to edit and visualize the API is by loading the api.yaml file into the online editor at https://editor.swagger.io/

# Status of OCTANE
Mar 7th, 2019 - Mcity runs an implementation of the Octane API specified in this repository. The specification and implementation are both under active development. We are using api-roadmap.yaml to guide the type of functions we plan to implement.

We host both a test and production environment of this implementation for users of the test facility.
The test environment can be found at https://mvillage.um.city/apidocs

The web socket (Socket.io) support is _experimental_ and not well documented. The REST API is our current recommendation for users.

The next major part of our work is on the signal abstration of traffic lights.

Implemented:
* Intersections
* Gates
* Crosswalks
* Rail crossings
* Facility information
* Initial Signal work
* Initial websockt work

Planned Schedule:
* 03/2019 - Signals / Rail functions / Requests
* 04/2019 - Segments / Sensors / Weather / Websockets / Logs / V2X
* 05/2019 - V2X / Lighting control / Maintenance Equipment
* 06/2019 - Data Collection / Additional Sensor work
* 07/2019 - Robot Control / Weather control
* 08/2019 - Scenario Storage / Playback / Status
* 09/2019 - UI Interface for control / First full API spec release (RON 1)

# Release schedule / numbering
The latest version of the API lives in the master branch in api.yaml

The broad roadmap for planned features is loosely specified in api-roadmap.yaml

Released are granted a Release Order Number (RON) and each RON will have it's own branch at time of release. 
The highest RON branch is the latest standard of the API.

* 06/27/18 - Initial spec release
* 03/01/19 - Mcity initial implementation release

# Contributing to OCTANE
To contribute to releases, submit requests through the GitHub issues feature for discussion or proposed changed via Pull Requests.

## Licensing
The OCTANE API spec is licensed through the MIT license.

## Maintainer
This API is presently maintained by @gmcguire and @tsworman
