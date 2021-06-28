# Service Development 301

Persona(s) Relevant:

- Developer

Difficulty Level:

- Taking it Further

Time to Create Content:

- 4 Weeks

Estimated Student Time:

- 60 Minutes

Part of Larger Series:

- Service Development

Content Type:

- Learning Lab

## High Level Design

- Service Design Patterns Overview (20%) 
    - Explain tradeoffs and when to use each, with a link to a github repo that is an example of each type (that works in the sandbox)
        - Regular service
        - Reactive Fastmap
        - Nano Service
        - Stacked Service
- Situational Features to Consider (20%)
    - Using opaque to keep random choices stable between redeploys (for example allocating IP addresses)
    - how and why to set operational data
    - Integrating with Outside Systems
        - IPAM 
        - Monitoring / Operational verification
        - using Resource manager Python API to reserve IDs. 
    - Using Resource Manager for things like VLAN IDs
    - Reactive FASTMAP Services and Nano Services 
        - Other relevant service design best practices regarding how FASTMAP works:
        - basic warnings given around having service create make a REST call, read a file or anything like that. 
- More Showcase examples to walk through (60%)
    - showcasing various service designs and situational features
    - reinforcing previous concepts of FASTMAP and how to create a service




Useful:
- development guide 5.5 p.292 opaque and persistent FASTMAP. (p. 305 of pdf) 
- side effects of fastmap p.239
- from service to rfm to nano service: https://www.youtube.com/watch?v=OIzBhzdAC9M 
    https://github.com/NSO-developer/template-to-nano-example
https://developer.cisco.com/docs/nso/#!service-design/performance
