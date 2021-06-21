# Service Development 101

Persona(s) Relevant:

- Developer

Difficulty Level:

- Taking it Further

Time to Create Content:

- 4 Weeks

Estimated Student Time:

- 90 Minutes

Part of Larger Series:

- Service Development

Content Type:

- Learning Lab

Pre-Req:
- Yang 101-301
- XML 101-301

## High Level Design

- NSO Services Overview (40%)
  - What is a NSO Service?
    - An abstraction of collected configuration, variable inputs and associated optional code logic
    - Services vs. Other NSO Device Config Mgmt
      - Other Device Manager Config Mgmt
        - Device Templates
        - Device Manager ad hoc changes (in CLI, API, etc.)
      - Services allow bundling of logic, service lifecycle management (this concept needs explanation)
      - FASTMAP
        - service meta data, backpointer / refcount, giving an example, showing that config is kept track of when removed or added. 
        - re-deploy, check-sync deep, removing service if overlapping config with other service 
    - Defining terms: (NSO Development Guide PDF 5.5 p.194)
      - Service model
      - Service Instance
      - Service Type
      - Device Configuration
      - Service Template
        - template is declarative. 
- Service Mapping (20%)
  - mapping not from workflow or sequence of commands 
  - not worried about CRUD, since FASTMAP takes care of it, don't need to defining delete or error handling, focus on create. 
  - Service mapping and service model design should not be tightly coupled to the vendor CLI syntax
  - Service Mapping Design Strategies
    - Service Template only
    - Code + Template
    - Code only (Java / Python)
    - Pros / cons
- Learn by Doing: The Breakdown of a Simple Service (40%)
  - use ncs-make-package, but paste in yang/templates and run makefile
    - Simple Yang model
    - Simple Template (covering at least two NED types / device types)
    - No code yet
    - explain the file layout
  - Show service CRUD on CLI/GUI, including dry-run, re-deploy, diff from Out of Band change
