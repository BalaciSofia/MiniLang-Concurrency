# MiniLang-Concurrency
This repository contains multiple extensions of the MiniLang interpreter, each implementing a different concurrency mechanism on top of a shared execution model.
[View the base MiniLang repository](https://github.com/BalaciSofia/MiniLang)

The base interpreter supports memory management, file operations, and type checking, while each variant explores synchronization techniques such as locks, semaphores, latches, barriers, and procedures.

## Variants

| Variant | What it adds |
|---|---|
| [Lock](MiniLang-Lock) | `newLock`, `lock`, `unlock` – mutual exclusion on shared memory |
| [Count Semaphore](MiniLang-Semaphore) | `createSemaphore`, `acquire`, `release` – limits concurrent access with permits |
| [Toy Semaphore](MiniLang-ToySemaphore) | `newSemaphore(var, exp1, exp2)`, `acquire`, `release` – semaphore whose capacity is `exp1 - exp2` |
| [CountDownLatch](MiniLang-Latch) | `newLatch`, `countDown`, `await` – waits until a count reaches zero |
| [Cyclic Barrier](MiniLang-CyclicBarrier) | `newBarrier`, `await` – threads wait until all of them reach the barrier |
| [Procedures](MiniLang-Procedure) | `call fname(...)` – call-by-value procedures with a stack of symbol tables |

Each variant is a complete copy of the interpreter with its own shared table
(LockTable, SemaphoreTable, LatchTable, BarrierTable, ProcTable) and thread-safe
statements built on Java synchronization.

## How to Run

Requirements: JDK 25+ and the [JavaFX SDK](https://openjfx.io/) 25 for the GUI.
Run the commands from inside a variant folder, e.g. `MiniLang-Lock`:

```bash
cd MiniLang-Lock
javac -d out --module-path <path-to-javafx>/lib --add-modules javafx.controls $(find src -name "*.java")
java -cp out view.Interpreter                    # console
java -cp out --module-path <path-to-javafx>/lib --add-modules javafx.controls GUI.SelectProgramGUI   # GUI
```
