# MiniLang – Toy Semaphore

Extension of the MiniLang interpreter that implements a **Toy Semaphore synchronization mechanism** for controlling access to shared resources across multiple threads.

Base project:
[MiniLang](https://github.com/BalaciSofia/MiniLang)

## Added Features

* Shared **SemaphoreTable** for thread coordination
* `newSemaphore(var, exp1, exp2)` – creates a semaphore
* `acquire(var)` – attempts to acquire access (blocks if limit reached)
* `release(var)` – releases access
* Atomic operations using Java synchronization

Limits the number of threads that can access a shared resource simultaneously, enabling controlled parallel execution.
