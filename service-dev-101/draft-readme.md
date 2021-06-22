Okay. First of all, when do you want to talk about what a service does, about the FASTMAP algorithm and all of that? Maybe put the basics into 101 and for 301 do a deep dive into what this means and why that means we need it to be side effect free?
    For sure, I was trying to outline some of that in the 101, "- NSO Services Overview (40%)", but I could add some more bullets. I am not sure what you mean by side effect free, but there is a lot more to deep dive in 301, possibly even cover stacked services. 

I’d probably avoid service discovery, I’d rather spend more time on other things. Maybe add the opaque. Maybe add something about setting operational data. As for all the tempalte processing instructions, didn’t you plan a separate lesson only on template processing?
    Fair enough, I saw a decent amount in the service design guide, but I think we have so much material to cover, that service discovery is something we can leave to the user to figure out, or cover in blogs or other mediums. For "opaque", I don't see that much in the Development PDF apart from Nano services. Are they used outside of nano services? Is there additional docs I should check out or just the Dev PDF?

I don’t know, I think I’d rather do a little bit of python than getting super deep into template services.
    Yeah, my original design was to have Python Development in a different course series. I feel like there is a whole set of things to figure out when adding coding logic, like connecting to a resource manager or outside data sources. We should definitely mention that Python is easier to maintain than going too crazy with pure XML and XPATH. 

For 301, maybe move service discovery there. Probably just the basics of RFM, but maybe something about things like resource allocation is helpful.

Teaching the Core Concepts in Action - NSO Services:
- FASTMAP Basics (focusing on benefits and practical example rather than theory)
- 


- Learn by Doing: The Breakdown of a Simple Service (40%)
  - use ncs-make-package, but paste in yang/templates and run makefile
    - Simple Yang model
    - Simple Template (covering at least two NED types / device types)
    - No code yet
    - explain the file layout
  - Show service CRUD on CLI/GUI, including dry-run, re-deploy, diff from Out of Band change


- NSO Services Overview (40%)
  - What is a NSO Service?
    - An abstraction of collected configuration, variable inputs and associated optional code logic
    - Services vs. Other NSO Device Config Mgmt
      - Other Device Manager Config Mgmt
        - Device Templates
        - Device Manager ad hoc changes (in CLI, API, etc.)
      - Services allow bundling of logic, service lifecycle management (this concept needs explanation)
      - FASTMAP
        - service meta data, backpointer / refcount, giving an example, showing that config is kept track of when removed or added. 
        - re-deploy, check-sync deep, removing service if overlapping config with other service 
    - Defining terms: (NSO Development Guide PDF 5.5 p.194)
      - Service model
      - Service Instance
      - Service Type
      - Device Configuration
      - Service Template
        - template is declarative. 