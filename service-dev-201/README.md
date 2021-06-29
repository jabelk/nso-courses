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
- Further showcase examples, building on the dev guide. Showing both using Python in a service and outside a service for ad hoc scripting. 
- Python in NSO, Services and Scripting
  - Basic explanation of value that adding code to services gives and how to create a package with Python and one with action starter code.
  - Basic explanation of `ncs` (the Python objects auto-generated based on the Yang model of NSO/NEDs/Packages) and `_ncs` (legacy lower level package for power XPATH users), they have to be run on same system as NSO, included in Python Path with `ncsrc`
  - ncs_pycli can be pretty helpful for these module explorations, show how to use
  - Provide a basic example of using Python in a service, walk through each component explaining what it does. 
    - setting a variable in the template from the yang service model, and a variable defined purely from the code, showing how each would be applied to a template, using $VARNAME, with dollar sign being different
    - Debugging Python code (setting breakpoints and finding log files, common mistakes)
    - using commit flags in Python in a service (commit dry-run outformat native)
    - Service Python Classes and Methods, parameters explained and how to use ServiceCallbacks / ncs.application.Application
      - cb_create()
  - Walk through an action example, using network relevant code, explain why action used vs service 
  - Show an audit / remediate type of Python script, that is looking for particular values to be present. Print the violations out, then set the correct values. 
  - Show how to find the Python path for a particular object found in the CLI (from XPATH, or other methods)
- More Showcase code, A more complicated service, perhaps one that supports two device types or something like that.
