# Yang for NSO 101

Persona(s) Relevant:

- NetDevOps
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

> Note: the concepts should be taught in active learning, with student using NSO to visualize the different Yang features in the CLI / GUI, and build their own simple models with packages (not services, but packages with simple data models).

The student will understand:

- Additional Yang and NSO Concepts (30%)
  - Callpoints and callbacks (http://66.218.245.39/doc/html/ch06.html )
  - Tail-F Actions and package pre-built from ncs-make-package
    - Tail-f Action or Yang action with Yang 1.1
  - tailf specific typedef that can be used in addition to the IETF ones (Guillaume feedbac)
  - best practices in using current() and deref() when building references and XPaths.
  - Common Data Models and data types
    - Working with multiple NED versions
    - Migrating from one NED version to another with existing data in the CDB
- Working with NEDs (20%)
  - using leafrefs to point to configuration in a device stored in the CDB, with multiple examples for different yang statement types (leaf, leaf-list, etc.)
    - note the cost / tradeoff:
      - not a best practice as it tend to lock your service models a bit and it can lead to quite weird scenarios, the need to import a sometimes 30K+ lines of YANG to one poor leafref in your 100 lines service model
      - can become tricky to handle when upgrading NEDs
  - identifying gaps in the data model in NSO, so support can add additional features
  - how you can do IOS interface refs vs. XR vs. …
- Working with NETCONF Devices (50%)
  - Building a NETCONF NED
  - Seeing Yang capablities
  - Talking to a NETCONF Device