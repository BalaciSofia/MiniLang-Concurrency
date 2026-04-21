# MiniLang – Count Semaphore

Extension of the MiniLang interpreter that implements a **Count Semaphore synchronization mechanism** for limiting concurrent access to shared resources.

Base project:
[MiniLang](https://github.com/BalaciSofia/MiniLang)


## Added Features

* Shared **SemaphoreTable** for thread coordination
* `createSemaphore(var, exp)` – creates a semaphore with a maximum number of permits
* `acquire(var)` – acquires a permit (blocks if limit reached)
* `release(var)` – releases a permit
* Atomic operations using Java synchronization

Controls how many threads can access a shared resource at the same time using a fixed number of permits.
