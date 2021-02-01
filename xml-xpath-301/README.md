# XML and XPATH for NSO 301

Persona(s) Relevant:

- NetDevOps
- Developer

Difficulty Level:

- Taking it Further

Time to Create Content:

- 2 Weeks

Estimated Student Time:

- 60 Minutes

Part of Larger Series:

- XML and XPATH for NSO

Content Type:

- Learning Lab

## High Level Design

The student will understand:

- Advanced examples of XPATH in Templates (40%)
    - examples: deref, current(), String functions (substring, startswith, etc), derived-from, , copy-tree, set-root-node, save-context, switch-context, local-name keypath in templates
- Multi-platform / multi-namespace templates (30%)
    - including / importing templates (l3vpn.xml.in example in mpls-vpn-new-template line 48)
    - 
- Using XML Configuration in NSO: (30%)
  - XPATH eval in dev tools in CLI and python API
  - debug template with XPATH
    - common errors
    - things to look for


### Resources
examples.ncs/service-provider in installation docs, mpls-vpn-new-template/packages/l3vpn/templates
https://devhints.io/xpath
https://www.ciscolive.com/c/dam/r/ciscolive/emea/docs/2019/pdf/LABSPG-2442-LG.pdf 
https://www.w3.org/TR/1999/REC-xpath-19991116/
https://community.cisco.com/t5/nso-developer-hub-discussions/ned-id-old-style-syntax/m-p/4271523#M5992
https://community.cisco.com/t5/nso-developer-hub-discussions/select-service-instances-by-partial-key-in-java/m-p/4185713#M5837
https://community.cisco.com/t5/nso-developer-hub-discussions/if-ned-greater-than/m-p/4175480#M5787
https://community.cisco.com/t5/nso-developer-hub-discussions/interface-shutdown-test-for-existence-in-xml-template/m-p/4170866#M5756
https://community.cisco.com/t5/nso-developer-hub-discussions/multiple-keys-validation-performance/m-p/4170508#M5753
https://community.cisco.com/t5/nso-developer-hub-discussions/interface-shutdown-test-for-existence-in-xml-template/m-p/4170418#M5751
https://community.cisco.com/t5/nso-developer-hub-discussions/how-can-i-remove-from-nso-a-device-associated-with-device-groups/m-p/4161433#M5705
https://community.cisco.com/t5/nso-developer-hub-discussions/is-it-possible-to-generate-an-xpath-to-a-node-using-the-python/m-p/4138268#M5597
https://community.cisco.com/t5/nso-developer-hub-discussions/xpath-position/m-p/3513828
https://community.cisco.com/t5/nso-developer-hub-discussions/xpath-check-for-config-templates/m-p/3775889
https://community.cisco.com/t5/nso-developer-hub-discussions/unable-to-use-xpath-as-a-value-when-deploying-a-device-template/m-p/4105161
https://community.cisco.com/t5/nso-developer-hub-discussions/nso-xpath-difference-using-xpath-on-leaf-and-on-when-statement/td-p/3864470
https://community.cisco.com/t5/nso-developer-hub-discussions/xpath-lookup-for-bigip-ltm-data/td-p/3717664
https://community.cisco.com/t5/nso-developer-hub-discussions/reading-value-using-xpath-service-reconciliation/td-p/3582393
https://community.cisco.com/t5/nso-developer-hub-discussions/can-i-use-something-like-in-name-leaf-field-for-an-xpath-eval/td-p/3926284