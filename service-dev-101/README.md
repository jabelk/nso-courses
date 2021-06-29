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
- NEW Showcase Development Guide

## High Level Design
- (assuming this content flows from the interactive New Development Guide)
- Showcase Examples Teaching (or briefly reviewing from the Dev Guide) the Following Concepts through live output:
  - FASTMAP 
        - service meta data, backpointer / refcount, giving an example, showing that config is kept track of when removed or added. (| display service to show FASTMAP)
        - compared to other automation technologies where you have to manually define the update / delete config statements. FASTMAP calculates for you. 
        - re-deploy, check-sync deep, removing service if overlapping config with other service 
        - Brief discussion on how Service Templates have FASTMAP and device templates outside of services do not (mentioning tradeoffs briefly)
    - Service Concepts: 
      - Service model
      - Service Instance
      - Service Type
      - Service Template
        - template is declarative. 
        - worth mentioning that the template is in XML to make it easy for NSO to read it in, NSO will transform it into native vendor CLI syntax behind the scenes when sending to the device. Sometimes confusion thinking that you are crafting NETCONF or something since NETCONF uses XML and Yang, and NSO uses XML and Yang (and NETCONF in different ways)
        - template processing instructions brief overview, with links to the Learn by Doing examples that illustrate them in more detail for further study. 
      - briefly cover package-meta-data since that is one part of the link between code and model