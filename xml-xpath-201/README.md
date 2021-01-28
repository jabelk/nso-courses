# XML and XPATH for NSO 101

Persona(s) Relevant:

- NetDevOps
- Developer

Difficulty Level:

- Taking it Further

Time to Create Content:

- 2 Weeks

Estimated Student Time:

- 45 Minutes

Part of Larger Series:

- XML and XPATH for NSO

Content Type:

- Learning Lab

## High Level Design

The student will understand:

- How XML Namespaces are used in the APIs: (15%)
  - RESTCONF (paths have prefix changes ncs:.../cisco-ios-ned:.../etc), | display restconf on CLI
  - Python Maapi / Maagic (paths have dunder ncs__object.ios__object)
- XPATH Usage: (30%)
  - XPATH Functions basics
  - Debug template XPATH (as an FYI or example, templates knowledge assumed)
  - XPATH displayed in CLI and GUI for reference and navigation
- Converting between XML, JSON and YAML (25%)
  - Using quick online tools like JSON2YAML for quick visuals
  - Using CLI options on show running-configuration | display xml / json / xpath
  - Using Python (just an example, don't need to teach it in detail)
- Exporting Configuration to a file: (30%)
  - Save configuration snippet in XML for service template development, noting which tags are needed and not needed (excluding `<config>` tags that will already be in a template) 

https://developer.cisco.com/learning/modules/nso-basics/nso-basics-cisco-it-103/step/6 