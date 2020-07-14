# OCTANE-API
Open Car (Mobility) Testing Automation Networked Environment API.

The Mcity developed OCTANE API allows users to control many aspects of test facility or Smart City Infrastructure. This RESTful web API offers an abstracted solution for enumerating, query, and control of devices such as traffic signals, rail crossings, crosswalks, cameras, lighting, and construction equipment from a centralized location.

OCTANE easily integrates with many common traffic control devices and attempts to simplify working with complicated devices like traffic controllers. From a phone, laptop, or vehicle computing platform your software can interact with the environment around it. The environment is easily extendable and well documented allowing you to quickly build support for existing custom hardware.

The specification for the OCTANE API is available at https://github.com/mcity/octane-api

# About Mcity
Mcity funds research and provides testing at our one-of-a-kind proving ground simulating the complexities of an urban environment, and through on-road vehicle deployments to a variety of settings in Ann Arbor and Southeast Michigan.

Mcity brings together partners from industry, government, and academia to develop the foundation for an ecosystem of connected and automated vehicles for moving people and goods. Such a system has the potential to dramatically improve safety, sustainability, and accessibility.

# Why OCTANE?
The Mcity test facility is a highly automated and connected proving ground in Southeast Michigan. Mcity developed the OCTANE API giving facility users access to develop control, orchestration, and the ability to easily run repeatable tests at the facility.

Our vision is that other facilities will implement the API standard on top of their hardware to provide a software abstraction layer of the facility. This allows mobility for tests and control scripts to move between multiple facilities that may have dissimilar hardware, and devices.

# Using OCTANE's OAS Spec
OCTANE is a specification for an API written using OAS3.0.
The easiest way to visualize the API is by viewing the Mcity implementation on [Mvillage](https://otane.mvillage.um.city/apidocs/)
You can use the [Swagger Editor](https://editor.swagger.io/?url=https://raw.githubusercontent.com/mcity/octane-api/master/api.yaml) to work with this spec.

# Status of OCTANE
July 14th, 2020 - Mcity runs an implementation of the Octane API specified in this repository. The specification and implementation are both under active development.

We host both a test and production environment of this implementation for users of the test facility.
The test environment can be found at https://octane.mvillage.um.city/apidocs.

The Mcity implementation of this API and supporting tools can be licensed from the University of Michigan. Please contact us for more information.

Our current focus is on the addition of robotic platforms and server side scenario execution via control server or Edge node.

Implemented:
* Facility - Multi-facility
* Intersections
* Signals
* Gates
* Crosswalks
* Lighting
* Safety Devices (Cones, Message Boards, Arrow Boards)
* Garage Door openers
* Rail crossings
* Facility information
* Socket IO - Push notifications and chat/synchronization.
* Sensor (Packages, Radar, LIDAR, Camera) - Enumeration and power control.
* Sessions - Management and multi-tenant support
* Scenario Storage -  status, enumeration.
* V2X - Enumeration and power control, TSCBM/SPaT/BSM/BSM send/receive
* Maintenance devices - Lawnmowers
* Triggers

Planned Development Schedule:
* 08/2020 - Edge Nodes, Robot Control, Weather state, Logging / Requests
* 09/2020 - Scenario Server side processing, Sensor Data Collection
* 11/2020 - First full API spec release (RON 1)

# Release schedule / numbering
The latest version of the API lives in the master branch in api.yaml


Released are granted a Release Order Number (RON) and each RON will have it's own branch at time of release. 
The highest RON branch is the latest standard of the API.

* 06/27/18 - Initial spec release
* 03/01/19 - Mcity initial implementation release
* 03/16/19 - Release .0.2 with signal support and conversion to OAS3.0.
* 03/24/19 - Release .0.3 with sensor support and enhanced rail functionality.
* 05/15/19 - Release .0.4 added documentation around Socket.IO connection and Initial V2X work, Intersection Phase documentation of timing/colors.
* 07/29/19 - Release .0.6 added more V2X endpoints, socketio endpoints for V2X, favorites to management nodes, and fixes to documentation for endpoints, initial data collection enumeration. Adjusted release schedule.
* 12/12/19 - Release .0.7 fixes for Socket.IO message type declarations, scenario storage and enumeration, lighting modules, power control for intersections, sensors and lights. Additional fixes for V2X radio supported/enabled.
* 12/12/19 - Release .0.8 Power control of sensors updated to add ability to control power at multiple levels through use of patch.
* 03/31/20 - Release .0.9 Add lighting control, garage door control, and initial implementations for safety devices. Multi-tenant facility support was added along with session management endpoints. Initial point of interest socket messages, along with work to support multiple map overlays at a facility. Intersection support has been enhanced by adding stop block enumeration for intersections with support.
* 04/10/20 - Cleanup of this repository and additional documentation. Additions to .9 spec to handle PSM V2X broadcast.
* 07/14/20 - Adds .10 spec to handle cleaner PSM/SPaT/BSM broadcast and receive. Addition of maintenance device endpoints.

# Contributing to OCTANE
To contribute to releases, submit requests through the GitHub issues feature for discussion or proposed changed via Pull Requests.

## Licensing
The OCTANE API spec is licensed through the MIT license.

## Maintainer
This API is presently maintained by @gmcguire, @tsworman, and @eserzomcity
