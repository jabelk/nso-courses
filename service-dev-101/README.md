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

- Learn by Example: NSO Services (60%)
  - Use existing SVI service in the sandbox (don't worry about the selfttest package at this point) to teach service concepts in action (i.e. create service instance, then explain what that means, probably look at they Yang / XML afterwards as it is a bit more abstract than seeing config being calculated and modified on the devices. Order not critical if there is a reason to do otherwise, also can use a different service if a good reason)
    - Defining terms: 
      - FASTMAP (just an overview of benefits and outcomes, give more details of theory and design implications in 301 lab)
        - service meta data, backpointer / refcount, giving an example, showing that config is kept track of when removed or added. 
          - compared to other automation technologies where you have to manually define the update / delete config statements. FASTMAP calculates for you. 
        - re-deploy, check-sync deep, removing service if overlapping config with other service 
        - Brief discussion on how Service Templates have FASTMAP and device templates outside of services do not (mentioning tradeoffs briefly)
      - Service model (NSO Development Guide PDF 5.5 p.194)
      - Service Instance
      - Service Type
      - Device Configuration
      - Service Template
        - template is declarative. 
        - worth mentioning that the template is in XML to make it easy for NSO to read it in, NSO will transform it into native vendor CLI syntax behind the scenes when sending to the device. Sometimes confusion thinking that you are crafting NETCONF or something since NETCONF uses XML and Yang, and NSO uses XML and Yang (and NETCONF in different ways)
        - template processing instructions brief overview, with links to the Learn by Doing examples that illustrate them in more detail for further study. 
  - Show service CRUD on CLI/GUI, including dry-run, re-deploy, diff from the service taking into account an Out of Band change (probably will have to make that change by logging in manually so NSO will not see it)

- Learn by Doing: The Breakdown of a Simple Service (40%)
  - use ncs-make-package, but give the snippets to paste in yang/templates and run makefile
    - Explain the typical development workflow:
      -  find pieces of config in CDB or write a pending transaction that is discarded, convert it to XML from NSO CLI display output
      - Put XML into template file
      - Use Yang constructs to define input data model for config and service (Leaf, List, Container, etc.)
      - Compile Yang, ensure Yang and XML files are saved and not still in edit mode
      - Packages reload (possibly with force)
      - Create test service instances against netsim and then against live devices
      - Continue this process for each piece of the config and each input. Starting with no inputs on the template and adding incrementally, making sure things still work. 
    - Simple Yang model
    - Simple Template (covering at least two NED types / device types), not having too many lines of config at this point or super complex interactions, letting them see how the moving pieces fit together of templates / fastmap / yang etc. 
    - No code yet
    - explain the file layout

