# Yang for NSO 101

Persona(s) Relevant:

- NetDevOps
- Developer

Difficulty Level:

- NSO Basics

Time to Create Content:

- 2 Weeks

Estimated Student Time:

- 120 Minutes

Part of Larger Series:

- Yang in NSO

Content Type:

- Learning Lab

## High Level Design

> Note: the concepts should be taught in active learning, with student using NSO to visualize the different Yang features in the CLI / GUI, and build their own simple models with packages (not services, but packages with simple data models).

The student will understand:

- Yang Functional Overview (30%)
  - Modules and sub-modules
  - import and include
    - examples of useful types and statements to import from ncs, ietf, tailf-common, etc. 
  - linting and helping tools (pyang, IDE plugins - VS Code etc)
  - needing to be compiled and consumed by an app to be useful
    - Makefile basics and editing it to import another yang file
- Yang Statement Syntax: Learning by Example (70%)
  - C style with {} and ; instead of whitespace, commenting // /* */ 
  - compilation with makefile and .fxs files in NSO
  - container (and presence container)
  - leaf
  - leaf-list
  - list (compared to python dictionary not python list)
  - grouping / uses
  - rpc 
  - choice 
  - Built-In Types and Derived Types (typedef)
  - XML Namespace
  - XPATH usage 
  - Leafref
  - when
  - must
  - Identities and how they differ from Enumerations (which to pick when)
  - config vs operational data
  - NSO Specific Syntax with Yang (Guillaume offered to help on this one)
    - tailf_yang_extensions, tailf_yang_cli, focusing on commonly used ones 