# Yang for NSO 101

Persona(s) Relevant:

- NetDevOps
- Operations
- Developer

Difficulty Level:

- NSO Basics

Time to Create Content:

- 2 Weeks

Estimated Student Time:

- 45 Minutes

Part of Larger Series:

- Yang in NSO

Content Type:

- Learning Lab

## High Level Design

- Background Knowledge (30%)
  - CLI vs API (Human vs Machine oriented interfaces)
  - Structured vs Unstructured Data (TCP header example, Ambiguous Cisco CLI commands - determining input fields and constraints)
  - What is a data model? Why do they help? What problems are they trying to solve? what problems happen when a data model is not used?
    - input validation
    - output validation
    - data types
    - API contracts, expecting certain structure of payload
    - Comparison to the `?` in a network CLI, giving available options
    - Examples of the same data not constrained by a model, and the problems it creates for coders
    - examples of the same data, but represented differently (list of lists vs list of dictionaries vs etc.)
    - Additional resources (videos from Hank on APIs, NETCONF and Yang)
      - https://developer.cisco.com/video/net-prog-basics/01-programming_fundamentals/data_formats
      - https://developer.cisco.com/video/net-prog-basics/02-network_device_apis/yang
- Yang: A networking Data Modeling Language (30%)
  - What is a data modeling language?
  - What features and benefits do we get through sticking to just one language (Yang)?
  - Where is Yang used and how is it used differently?
    - Yang in NETCONF/RESTCONF/gNMI etc
    - Yang in NSO 
  - Where to find Yang data models (10%)
    - Device models (GitHub or ask device for its model)
    - NSO models (src file in installation folder or NED)
- NSO and Yang (40%)
  - NSO Application Architecture (CDB, Packages, Northbound APIs, Southbound Devices)
  - Feature parity across all APIs because using Yang / ConfD
  - The extensibility of NSO using Yang and packages (services or not) by extending the NSO data model
  - Demonstrate NSO extensible through a simple package
    - Show the CLI / GUI having new fields with a container with a leaf
    - show the input failing to commit based on input validation
    - show a leaf-list with the same thing
    - use intuitive names for the yang model like "leaf input-field" so student can correlate
    - show side by side with the data model and it showing up in NSO GUI / CLI
    - demonstration is to show power of data modeling, before really teaching all the ins and outs of Yang
    - use pre-staged packages that can be git cloned and a script that requires no knowledge of Yang or makefiles