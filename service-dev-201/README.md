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

- Service Discovery (development ch 11)
  - services deployed manually, or through older system
  - import existing services into NSO
  - import device into NSO
    - write yang for data model and mapping logic
    - display service meta data, 
    - redeploy reconicle discard non service config dry run
    - examples.ncs/getting started/ developing with ncs/ 4-rfs-service
- Templates
  - Device vs Config vs Service vs Feature Templates (Ch12 development pdf)
    - defining terms: from pdf
    - naming conventions for config-template 'package name-feature.xml'
    - Writing a Config Template from a Device Template, save to file after drafting
    - Writing a Config Template from a Device Config snippet, display xml, save
  - Built-In Features
    - predefined variables: $DEVICE, $TEMPLATE_NAME, $SCHEMA_OPAQUE 
    - Templates are declarative, tags: merge, replace, delete, create, nocreate
    - basic string variables $VARNAME
    - Template processing instructions
      - set variable
      - if else
      - for loop
      - copy-tree
      - set-context-node
      - set-root-node
      - save-context
      - switch context
      - if-ned-id elif-ned-id 
    - ordered-by user lists / leaf-lists, using insert="" and guard attribute, ACLs multiple services on same list
    - Debugging Templates
      - debug template, debug xpath
      - things to look for, common mistakes
    - Service Templates
      - examples.ncs/service-provider/simple-mpls-vpn
      - ncs:servicepoint
      - xpath and template processing instructions examples
      - supported-ned-ids in the package meta data.xml file, benefits time savings and fewer errors
      - 

