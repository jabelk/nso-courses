# nso-courses

## Resources  

### Yang
- 5.5 development guide chapter 5
- https://www.oreilly.com/library/view/network-programmability-with/9780135180471/
- https://tools.ietf.org/html/rfc6020
- https://developer.cisco.com/learning/modules/nso-basics/nso-basics-cisco-it-103/step/1
- https://napalm-automation.net/yang-for-dummies/
- https://github.com/NSO-developer/nso-5-day-training/blob/master/Yang%20Cheat%20Sheet.pdf
- https://github.com/NSO-developer/nso-5-day-training/blob/master/LectureNotes/NSO_Day_2_yang_xml_and_rest_api.pdf
- http://66.218.245.39/doc/html/ch06.html (confd user guide)

### XML / XPATH

example from Hank
```
    list switch-pair {
      tailf:info "A pair of network switches which are deployed in the fabric to offer connectivity redundancy. Configuration (and port usage) is common within the pair.";
      ordered-by user; 

      leaf-list switch {
        ordered-by user;  
        type leafref { 
          path "/ncs:devices/ncs:device/ncs:name"; 
        }
        tailf:info "The two devices which make up the switch pair. The first entered will be hold primary roles where appropriate.";
        min-elements 2;
        max-elements 2;
      }

      // Constraints
      //  - Same NED as primary 
      must "/ncs:devices/ncs:device[ncs:name=current()/switch[1]]/ncs:device-type/ncs:cli/ncs:ned-id = /ncs:devices/ncs:device[ncs:name=current()/switch[2]]/ncs:device-type/ncs:cli/ncs:ned-id" {
        error-message "primary and secondary members of a switch pair must use the same NED";
      }

      // Constraints 
      //  - A network device cannot be a part of more than one fabric 
      //  - Get a count of how many times each switch shows up in any network fabric
      must "
            count(/network-fabric/switch-pair/switch[text() = current()/switch[1]]) <= 1
            and count(/network-fabric/switch-pair/switch[text() = current()/switch[2]]) <= 1
            " {
        error-message "A device cannot be a member of more than one switch-pair.";
      }

    }
```

- examples.ncs/service-provider in installation docs, mpls-vpn-new-template/packages/l3vpn/templates
- http://userguides.tail-f.com/ncs/nso-5.4/doc/html/nso_man/man.5.tailf_yang_extensions.html (XPATH FUNCTIONS section at bottom)
- https://www.amazon.com/XML-Pocket-Consultant-William-Stanek/dp/0735611831
- https://github.com/jabelk/ntp_server_example
- https://github.com/jabelk/radius_server_example
- https://devhints.io/xpath
- https://www.ciscolive.com/c/dam/r/ciscolive/emea/docs/2019/pdf/LABSPG-2442-LG.pdf 
- https://www.w3.org/TR/1999/REC-xpath-19991116/
- https://community.cisco.com/t5/nso-developer-hub-discussions/ned-id-old-style-syntax/m-p/4271523#M5992
- https://community.cisco.com/t5/nso-developer-hub-discussions/select-service-instances-by-partial-key-in-java/m-p/4185713#M5837
- https://community.cisco.com/t5/nso-developer-hub-discussions/if-ned-greater-than/m-p/4175480#M5787
- https://community.cisco.com/t5/nso-developer-hub-discussions/interface-shutdown-test-for-existence-in-xml-template/m-p/4170866#M5756
- https://community.cisco.com/t5/nso-developer-hub-discussions/multiple-keys-validation-performance/m-p/4170508#M5753
- https://community.cisco.com/t5/nso-developer-hub-discussions/interface-shutdown-test-for-existence-in-xml-template/m-p/4170418#M5751
- https://community.cisco.com/t5/nso-developer-hub-discussions/is-it-possible-to-generate-an-xpath-to-a-node-using-the-python/m-p/4138268#M5597
- https://community.cisco.com/t5/nso-developer-hub-discussions/how-can-i-remove-from-nso-a-device-associated-with-device-groups/m-p/4161433#M5705
- https://community.cisco.com/t5/nso-developer-hub-discussions/xpath-position/m-p/3513828
- https://community.cisco.com/t5/nso-developer-hub-discussions/xpath-check-for-config-templates/m-p/3775889
- https://community.cisco.com/t5/nso-developer-hub-discussions/unable-to-use-xpath-as-a-value-when-deploying-a-device-template/m-p/4105161
- https://community.cisco.com/t5/nso-developer-hub-discussions/nso-xpath-difference-using-xpath-on-leaf-and-on-when-statement/td-p/3864470
- https://community.cisco.com/t5/nso-developer-hub-discussions/xpath-lookup-for-bigip-ltm-data/td-p/3717664
- https://community.cisco.com/t5/nso-developer-hub-discussions/reading-value-using-xpath-service-reconciliation/td-p/3582393
- https://community.cisco.com/t5/nso-developer-hub-discussions/can-i-use-something-like-in-name-leaf-field-for-an-xpath-eval/td-p/3926284
- kicker in confd: https://info.tail-f.com/hubfs/Whitepapers/Using%20the%20Kicker%20Feature%20in%20ConfD%20-%20Rev%20A%202020-07-15.pdf
- https://community.cisco.com/t5/nso-developer-hub-discussions/understanding-kickers/td-p/3890298
