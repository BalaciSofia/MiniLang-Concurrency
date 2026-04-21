# MiniLang – Cyclic Barrier

Extension of the MiniLang interpreter that implements a **Cyclic Barrier synchronization mechanism** for coordinating multiple threads.

Base project:
[MiniLang](https://github.com/BalaciSofia/MiniLang)

## Added Features

* Shared **BarrierTable** for thread synchronization
* `newBarrier(var, exp)` – creates a barrier with a required number of threads
* `await(var)` – blocks execution until all threads reach the barrier
* Thread-safe operations using Java synchronization

Threads pause at `await` and continue execution only when all required threads reach the barrier, enabling coordinated parallel execution.
