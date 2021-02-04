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

The student will understand:

- Structured Data Basics (10%)
  - JSON vs XML vs YAML
  - The value of structured data vs unstructured data
- Data modeling basics (40%)
  - What is a data model? Why do they help? What problems are they trying to solve? what problems happen when a data model is not used?
    - input validation
    - output validation
    - data types
    - API contracts, expecting certain structure of payload
    - Comparison to the `?` in a network CLI, giving available options
    - Examples of the same data not constrained by a model, and the problems it creates for coders
    - examples of the same data, but represented differently (list of lists vs list of dictionaries vs etc.)
  - What are examples of data models?
  - Why is a data modeling language needed?
- Yang: A networking Data Modeling Language (40%)
  - What is a data modeling language?
  - What features and benefits do we get through sticking to just one language (Yang)?
  - Where is Yang used and how is it used differently?
    - Yang in NETCONF/RESTCONF/gNMI etc
    - Yang in NSO 
  - Where to find Yang data models (10%)
    - Device models (GitHub or ask device for its model)
    - NSO models (src file in installation folder or NED)
  - Brief overview of Yang syntax and usage