# XML and XPATH for NSO 201

Persona(s) Relevant:

- NetDevOps
- Developer

Difficulty Level:

- Taking it Further

Time to Create Content:

- 2 Weeks

Estimated Student Time:

- 120 Minutes

Part of Larger Series:

- XML and XPATH for NSO

Content Type:

- Learning Lab

## High Level Design

The student will understand:

- XPATH Functions basics: (20%)
  - Why / When to use
  - Tradeoff of complexity in the code and ease of maintenance 
  - examples: deref, current(), String functions (substring, startswith, etc)
  - xpath eval command in nso
- XPATH Operators and Data Types (40%)
  - Operators
    - xpath filters there (the []-things)
    - Variable operator $
    - selection operator | 
    - Expression operators: . .. / @ 
    - Wildcard Operators: * @* node() //
  - Data Types
    - node-set
    - String / Number / Boolean
- How XML Namespaces and Module Prefixes are used in NSO APIs: (10%)
  - RESTCONF (paths have prefix changes ncs:.../cisco-ios-ned:.../etc), | display restconf on CLI
  - Python Maapi / Maagic (paths have dunder ncs__object.ios__object)
 

