# Difference Between Process and Thread (Easy Exam Table)

| **Process**                                   | **Thread**                                                         |
| --------------------------------------------- | ------------------------------------------------------------------ |
| Large unit of execution                       | Smallest unit of execution                                         |
| Heavyweight                                   | Lightweight                                                        |
| Has its own memory                            | Shares memory with other threads                                   |
| Creation is slow                              | Creation is fast                                                   |
| Communication is slow (IPC)                   | Communication is fast (shared memory)                              |
| Context switching is slower                   | Context switching is faster                                        |
| More resource usage                           | Less resource usage                                                |
| Failure of one process does not affect others | Failure of one thread may affect other threads in the same process |

### Memory Trick

**Process = House 🏠**
**Thread = Family Members 👨‍👩‍👧**

* House has separate rooms and resources.
* Family members share the same house.

---

# Difference Between User-Level Thread (ULT) and Kernel-Level Thread (KLT)

| **User-Level Thread (ULT)**                 | **Kernel-Level Thread (KLT)**              |
| ------------------------------------------- | ------------------------------------------ |
| Managed by user thread library              | Managed by OS kernel                       |
| OS is not aware of threads                  | OS knows all threads                       |
| Faster to create                            | Slower to create                           |
| Low overhead                                | High overhead                              |
| Context switch is fast                      | Context switch is slower                   |
| If one thread blocks, all threads may block | One blocked thread does not block others   |
| Cannot fully utilize multiple CPUs          | Supports true parallelism on multiple CPUs |

### Memory Trick

**ULT = User manages everything** 👤

**KLT = Kernel (OS) is the Boss** 🖥️

---

# 2-Mark Revision

## Process vs Thread

* Process = Heavyweight, separate memory.
* Thread = Lightweight, shared memory.
* Process creation = Slow.
* Thread creation = Fast.

## User Thread vs Kernel Thread

* User Thread = Managed by user library, fast, OS unaware.
* Kernel Thread = Managed by OS, slower, OS aware, better scheduling.

---

# Super Easy Exam Keywords

### Process

**Heavy → Separate Memory → Slow**

### Thread

**Light → Shared Memory → Fast**

### User Thread

**User manages → Fast → OS doesn't know**

### Kernel Thread

**OS manages → Slower → OS knows**
