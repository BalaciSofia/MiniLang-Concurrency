# MiniLang – Lock
Extension of the MiniLang interpreter that implements a **Lock-based synchronization mechanism** for safe access to shared memory.

Base project:
[MiniLang](https://github.com/BalaciSofia/MiniLang)

## Added Features

* Shared **LockTable** for mutual exclusion
* `newLock(var)` – creates a new lock
* `lock(var)` – acquires the lock (blocks if already taken)
* `unlock(var)` – releases the lock
* Atomic operations using Java synchronization

Ensures **mutual exclusion** when multiple threads access shared data, preventing race conditions.
