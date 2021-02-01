# XML and XPATH for NSO 201

Persona(s) Relevant:

- NetDevOps
- Developer

Difficulty Level:

- Taking it Further

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

- How XML Namespaces are used in NSO APIs: (25%)
  - RESTCONF (paths have prefix changes ncs:.../cisco-ios-ned:.../etc), | display restconf on CLI
  - Python Maapi / Maagic (paths have dunder ncs__object.ios__object)
  - Creating Device templates (apart from services) using XML with variables
- Basic Templating Constructs in Templates: (50%)
  - XPATH Functions basics:
    - Why / When to use
    - Tradeoff of complexity in the code and ease of maintenance 
    - template processing instructions:
      - conditionals, loops, setting variables (set, foreach, if, for)
    - XML NSO tags (nocreate, merge, etc. )
- Converting between XML, JSON and YAML (25%)
  - Using quick online tools like JSON2YAML for quick visuals
  - Using CLI options on show running-configuration | display xml / json / xpath
  - Using Python (just an example, don't need to teach it in detail)
  - Save configuration snippet in XML with CLI for service template development, noting which tags are needed and not needed (excluding `<config>` tags that will already be in a template) 

### Resources
examples.ncs/service-provider in installation docs, mpls-vpn-new-template/packages/l3vpn/templates
https://github.com/jabelk/ntp_server_example
https://github.com/jabelk/radius_server_example
https://devhints.io/xpath
https://www.ciscolive.com/c/dam/r/ciscolive/emea/docs/2019/pdf/LABSPG-2442-LG.pdf 
https://www.w3.org/TR/1999/REC-xpath-19991116/
https://community.cisco.com/t5/nso-developer-hub-discussions/ned-id-old-style-syntax/m-p/4271523#M5992
https://community.cisco.com/t5/nso-developer-hub-discussions/select-service-instances-by-partial-key-in-java/m-p/4185713#M5837
https://community.cisco.com/t5/nso-developer-hub-discussions/if-ned-greater-than/m-p/4175480#M5787
https://community.cisco.com/t5/nso-developer-hub-discussions/interface-shutdown-test-for-existence-in-xml-template/m-p/4170866#M5756
https://community.cisco.com/t5/nso-developer-hub-discussions/multiple-keys-validation-performance/m-p/4170508#M5753
https://community.cisco.com/t5/nso-developer-hub-discussions/interface-shutdown-test-for-existence-in-xml-template/m-p/4170418#M5751
https://community.cisco.com/t5/nso-developer-hub-discussions/is-it-possible-to-generate-an-xpath-to-a-node-using-the-python/m-p/4138268#M5597