# Service Development 201

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

## High Level Design

- Learn by Doing: A Python Based Service
  - create using ncs-make-package, option to add an action template. 
  - setting a variable from the yang data model, and a variable purely from the code, showing how each would be applied to a template, using $VARNAME, with dollar sign being different
  - Service Python Classes and Methods, parameters explained and how to use ServiceCallbacks / ncs.application.Application
    - cb_create(), cb_pre_lock_create(), cb_pre_modification(), cb_post_modification(), setup(), teardown(), register_service()
    - basic warnings given around having service create make a REST call, read a file or anything like that. 
  - Other Tips:
    - Using opaque to keep random choices stable between redeploys
    - setting operational data
  - Using Resource Manager for things like VLAN IDs
    - using Resource manager Python API to reserve IDs. 
    

