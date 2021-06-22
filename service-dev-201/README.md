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

- Learn by Doing: Services with Python (40%)
  - Basic explanation of value that adding code to services gives and how to create a package with Python and one with action starter code.
  - Basic explanation of `ncs` (the Python objects auto-generated based on the Yang model of NSO/NEDs/Packages) and `_ncs` (legacy lower level package for power XPATH users), they have to be run on same system as NSO, included in Python Path with `ncsrc`
  - Provide a basic example of using Python in a service, walk through each component explaining what it does. 
    - setting a variable in the template from the yang service model, and a variable defined purely from the code, showing how each would be applied to a template, using $VARNAME, with dollar sign being different
    - Debugging Python code (setting breakpoints and finding log files, common mistakes)
    - using commit flags in Python in a service (commit dry-run outformat native)
    - basic action example, using network relevant code

- Learn by Example: FASTMAP and Service Theory Revisited (40%)
  - Deeper Theory and design implications of using FASTMAP, walking through explaining each concept with a piece of service code or output
    - explanation of what FASTMAP does, using practical details and examples from NSO / networking, more relevant than just the academic visualization of colored dots in current docs using X/Y/Z and A/B/C variables (though that may help folks with academic CS backgrounds). Might be worth explaining what NSO is trying to achieve with ACID DB principles briefly, and treating the network as a DB with transactional integrity.  
  - Service Python Classes and Methods, parameters explained and how to use ServiceCallbacks / ncs.application.Application
    - cb_create(), cb_pre_lock_create(), cb_pre_modification(), cb_post_modification(), setup(), teardown(), register_service()

- Troubleshooting Service Development (20%)
    - common pitfalls
    - debugging commands
    - log files to check 
    - provide a service that is actually broken and give steps to fix them for example