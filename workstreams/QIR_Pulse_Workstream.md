# Workstream: Pulse Support

## Motivation & Benefits

We propose adding Pulse Profile to the QIR specification to natively support
pulse-level abstractions. Pulse-level access enables fine-grained qubit
manipulation across different quantum technologies, supporting applications
such as automated calibration, error mitigation, and optimal control.

## Requirements

The workstream should specify the requirements to support defining and
executing quantum pulse-level programs. This includes introducing new data
types and instructions to the specification.

The specification should define the data types that are essential to represent
abstractions required for pulse support. These abstractions may include, but
are not limited to, port, frame, and waveform.

- Port: A software representation of the hardware input and output channels
  used to manipulate and read out qubits. It exposes vendor-defined actuation
  knobs for targeting useraccessible hardware components, such as drive or
  acquisition channels, while abstracting away device-specific complexity.
- Waveform: A time-ordered array of samples, defining the amplitude envelope
  of a control signal. The amplitudes can be provided either explicitly or by
  parametrized functions which, when assigned with specific parameter values,
  evaluate to a concrete array of samples.
- Frame: Stateful timing and carrier signal abstraction combining a reference
  clock, carrier frequency, and phase. It tracks the elapsed time and provides
  the timing, frequency, and phase context for playing waveforms, enabling
  precise carrier modulation and virtual phase rotations.

The specification should also define the following instructions for the
quantum instruction set:

- play: run a given pulse on a port
- delay: insert a delay between waveforms (pulses).

## Dependencies & Related Projects

A related Base-Profile Definition workstream is to specify the minimal
requirements to support defining and executing quantum programs. The current
workstream should make sure that the specification are complaint with the Base
profile.

## Deliverable(s) & Expected Outcome

The expected outcome is a document that clearly defines the requirements
outlined [above](#requirements).

## Future Work (Out of Scope)

## Working Group & Getting Involved

Members: <br/>
Chairs: Muhammad Nufail Farooqi, Jorge Echavarria

If you would like to contribute to the workstream, please contact
[qiralliance@mail.com](mailto:qiralliance@mail.com),
[quantum@lrz.de](mailto:quantum@lrz.de), or
[mqss@munich-quantum-valley.de](mailto:mqss@munich-quantum-valley.de).

## Schedule

Launch date: October 2025 <br/>
Estimated end date: March 2026 <br/>
Meeting schedule and/or channel(s) of communication: TBA

## Status & Discussions

The work and status is tracked in the form of a GitHub issue
[#48](https://github.com/qir-alliance/.github/issues/48).
<br/>
We encourage comments, inputs, and discussions on that issue.

The GitHub issue is labeled as `Approved` after approval by the steering
committee.

## Open Questions
