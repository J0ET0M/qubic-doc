# TickData
The `TickData` is the definition of a `Tick`.

Source Code: https://github.com/qubic/core/blob/main/src/network_messages/tick.h

The [Tickleader](Computor.md#tick-leader) creates the ´TickData´ and will propagate the ´TickData´ in advance to the network.

The `#define TICK_TRANSACTIONS_PUBLICATION_OFFSET 2 // Must be only 2` in [qubic.cpp](https://github.com/qubic/core/blob/main/src/qubic.cpp) defines at which time the TickData is broadcasted.

2 means that each `TickLeader` will broadcast the `TickData` when he the Computor is leader in `currentTick + 2`.