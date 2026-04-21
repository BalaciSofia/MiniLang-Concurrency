# MiniLang – Latch

Extension of the MiniLang interpreter that implements a **CountDownLatch synchronization mechanism** for coordinating thread execution.

Base project:
[MiniLang](https://github.com/BalaciSofia/MiniLang)


## Added Features

* Shared **LatchTable** for synchronization
* `newLatch(var, exp)` – creates a latch with an initial count
* `await(var)` – blocks execution until the count reaches zero
* `countDown(var)` – decrements the latch count
* Atomic operations using Java synchronization

Threads wait at `await` until the latch count reaches zero, enabling synchronization after multiple parallel operations complete.
