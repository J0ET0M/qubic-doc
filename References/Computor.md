# Computor
In Qubic we call a Computor one of 676 validators.

Technically a Computor is "just" a Qubic Id. (e.g. SUKAZZMJWWSHFBEKJLPMNUEOWXSBDMFTWPWFANCVMGCPOHIDGQWIEYCCWZII).

The duties of a Computor are:
- Executing Smart Contracts
- Preparing [TickData](d:/dev/qubic/qubic-doc/References/TickData.md)
- Validating Chain information


## Tick Leader
The Tick Leader is the Computor which is responsible for a given [Tick](Tick.md)).

It is determined by `CURRENTTICK % COMPUTORINDEX == 0`.

**Example:**

Tick: `15104383`

ComputorIndex: `515`

This resolves to: `15104383 % 515 == 0`



