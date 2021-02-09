# XML and XPATH for NSO 101

Persona(s) Relevant:

- NetDevOps
- Operations
- Developer

Difficulty Level:

- NSO Basics

Time to Create Content:

- 2 Weeks

Estimated Student Time:

- 100 Minutes

Part of Larger Series:

- XML and XPATH for NSO

Content Type:

- Learning Lab

## High Level Design

The student will understand:

- Structured Data Basics (10%)
  - JSON vs XML vs YAML
  - Converting between XML, JSON and YAML  
    - Using quick online tools like JSON2YAML for quick visuals
    - Reference Hank's video on JSON/XML/YAML for deeper dive
    - https://developer.cisco.com/video/net-prog-basics/01-programming_fundamentals/data_formats
- XML Syntax using networking examples: (30%)
  - Root / Child / Subchild
  - XML Elements
  - XML Attributes (metadata)
  - XML Namespaces (using prefixes)
  - XML Comments
  - Double vs Single quotes
- Why XML is important in NSO: (30%)
  - CDB represented to the user in XML for device and application configuration
  - Getting the Data from NSO in XML:
    - show running-configuration | display xml
    - commit dry-run outformat xml
    - show configuration display xml (to show pending change)
- XPATH Basics: (30%)
  - XPATH purpose, syntax, and usage (comparing to URL syntax for reference)
  - Viewing XPATH in the NSO CLI
  - Using CLI options on show running-configuration | display xml / json / xpath / prefix

## Examples

https://developer.cisco.com/learning/modules/nso-basics/nso-basics-cisco-it-103/step/6 