# Workstream: QIR Modules and Externs

## Motivation & Benefits
Current QIR specification assumes all code is in the same executable main module. 
This assumption is limiting modular code development and code reuse.
Ability to define common libraries of reusable algorithms as standard QIR modules can enhance QIR ecosystem attractiveness for developers.

Additionally, many QPU platforms offer platform capabilities that can be called directly from QIR.
These can provide specific hardware control or generic access to classical control extensions often used for QEC decoding 
or other forms of accelerated classical computing that are not easy or practical to express in QIR natively.

Both capabilities are expected to play a key role as the industry migrates to larger fault-tolerant machines. 
In FT world QIR can be used to represent programs at computational qubit level, QEC gadget level, and physical qubit level. 
QIR libraries may be used to provide QEC gadget definitions in this scenario.
While QEC may be an attractive use case for reusable QIR libraries, the workstream shall consider a generic capability applicable to any other future use case.

This workstream will define a standard LLVM-compliant way of constructing and referencing library modules and external platform functions.

## Requirements
- Define QIR library module format
- Define QIR library module reference
  - Consider hierarchical library dependencies
- Define external function reference
  - Consider platform-specific attributes
- Use LLVM-standard techniques as much as possible

## Dependencies & Related Projects
This workstream does not depend on any prior profiles and defines a new foundational QIR capability.

## Deliverable(s) & Expected Outcome
The workstream will deliver a new profile or a set of changes to the base QIR specification depending on the outcome.

Additionally, a set of examples using new capabilities shall be constructed and made available as a reference for the community.

## Future Work (Out of Scope)
- Further customization for use with QEC, logical qubit block encoding, etc.

## Working Group & Getting Involved

Chair: Proposed Kartik Singhal (Quantinuum)\
Members: TBD

If you would like to contribute to the workstream, please contact the chair.

## Schedule

Launch date: November 2, 2026\
Estimated end date: May 1, 2027\
Meeting schedule and/or channel(s) of communication: TBD

## Status & Discussions

The work and status is tracked in the form of a GitHub issue \<insert link\>.

We encourage comments, inputs, and discussions on that issue.

The GitHub issue is labeled as `Approved` after approval by the steering
committee.

## Open Questions
