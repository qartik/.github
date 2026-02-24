# Workstream: Dynamic Qubit Allocation and Arrays

This workstream aims to add support for dynamic qubit allocation, fixed-size
qubit arrays and measurement result arrays to QIR. Relatedly, the workstream
will determine the semantics for passing of qubits and qubit arrays as function
arguments, array iteration and indexing, and efficient return of measurement
results, all while keeping classical data management simple with stack
allocation.

## Motivation & Benefits

- Dynamic qubit allocation enables support for algorithms (e.g., quantum error
  correction) that require allocating ancilla qubits during execution.
- First-class array and iteration support make it practical to express families
  of quantum circuits (e.g., quantum Fourier transform, variational algorithms)
  that scale with input parameters or hardware resources.
- Modeling qubits and qubit arrays as function arguments allows for
  parameterized programs allowing the same algorithm to efficiently target
  devices with varying qubit counts, assuming device support.
- Improve interoperability for advanced quantum languages, facilitate compiler
  optimizations, and broaden backend and platform compatibility.

## Requirements

- Extend QIR to:
  - Represent dynamic allocation of individual qubits within the IR.
  - Support declarations of fixed-size qubit and measurement arrays.
  - Support passing qubits and qubit arrays as function arguments.
  - Support iteration over qubit arrays within the IR.
  - Enable returning arrays of measurement results.
  - Maintain backward compatibility with existing QIR ecosystem tooling.
- Document specification changes with clear illustrative examples.
- Gather input and iterate with frontend and backend implementers.

## Dependencies & Related Projects

- QIR Base and Adaptive profile specifications.
- Opaque Pointer Workstream

## Deliverables & Expected Outcome

- An extension to the QIR specification supporting:
  - Dynamic allocation of individual qubits.
  - Declaration of fixed-size qubit/measurement arrays.
  - Passing qubits to functions.
  - Iteration over qubit arrays.
  - Returning arrays of measurement results.
- Example QIR code snippets that utilize new calling and return conventions,
  demonstrating interoperability and modular quantum algorithms.

## Open Questions

- What IR conventions should be adopted for iteration over and indexed access
  into qubit arrays in a portable and efficient manner?
- How can returning arrays of measurements be standardized to ensure
  interoperability?
- How to balance simplicity and expressivity in function return semantics for
  qubit arrays without introducing complex ownership or lifetime semantics?
- What practices will ensure backward compatibility for existing QIR consumers?

## Future Work (Out of Scope)

- Dynamic classical memory allocation (unsupported in the current proposal).
- Compiler or runtime optimizations unrelated to the core IR representation.
- Generic classical or quantum resource management beyond stack lifecycle.

## Working Group & Getting Involved

Members: Adam Geller, Alex Chernoguzov, Bettina Heim, Ian Davis, Kartik Singhal, Luca Mondada, Stefan Wernli, Thomas Alexander

Chair: Kartik Singhal

If you would like to contribute to the workstream, please contact [@qartik](https://github.com/qartik).

## Schedule

- Launch date: October, 2025
- Estimated end date: March, 2026
- Meeting schedule and/or channel(s) of communication: every other week

## Status & Discussions

The work and status are tracked in the form of a
[GitHub issue](https://github.com/qir-alliance/qir-spec/issues/58)
in the QIR Spec. We encourage comments, inputs, and discussions on that issue.

The GitHub issue is labeled as `Approved` after approval by the steering
committee.
