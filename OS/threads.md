# Threads – Easy Exam Notes (2–5 Marks)

---

# 1. Thread Overview

## Definition

A **Thread** is the **smallest unit of CPU execution** inside a process.

* A process can have **one or more threads**.
* Threads of the same process **share memory and resources**.

### Memory Trick

**Process = House 🏠**
**Thread = Family Members 👨‍👩‍👧**

* House (Process)
* Family Members (Threads)

All family members share the same house.

---

## Diagram

```text
Process
│
├── Thread 1
├── Thread 2
├── Thread 3
└── Thread 4
```

---

## Each Thread has its own

* Program Counter (PC)
* Registers
* Stack

## Threads Share

* Code
* Data
* Files
* Memory

### Memory Trick

**Own → PCS**

* Program Counter
* CPU Registers
* Stack

**Share → CDFM**

* Code
* Data
* Files
* Memory

---

# 2. Benefits of Threads

### 1. Faster Execution

Multiple threads run simultaneously.

---

### 2. Better CPU Utilization

CPU remains busy.

---

### 3. Resource Sharing

Threads share the same memory.

---

### 4. Easy Communication

Communication between threads is faster.

---

### 5. Economy

Creating a thread is cheaper than creating a process.

---

### 6. Responsiveness

One thread can continue while another waits.

Example:

* Browser downloads a file while you continue browsing.

---

## Memory Trick

Remember:

### **FBERE**

* **F** → Faster
* **B** → Better CPU utilization
* **E** → Easy communication
* **R** → Resource sharing
* **E** → Economy

---

# Advantages of Threads

* Fast execution
* Less memory
* Better performance
* Easy communication
* Parallel processing

---

# Disadvantages

* Synchronization problems
* Race conditions
* Debugging is difficult
* One thread error may affect others

---

# 3. Types of Threads

There are **2 types**:

1. User-Level Threads (ULT)
2. Kernel-Level Threads (KLT)

---

# A. User-Level Threads (ULT)

## Definition

Managed by the **user thread library**.

The **Operating System is not aware** of these threads.

### Diagram

```text
Application
      │
Thread Library
      │
Operating System
```

---

## Advantages

* Fast creation
* Fast switching
* No kernel support required

---

## Disadvantages

* If one thread blocks, all threads block.
* Cannot fully use multiple CPUs.

---

## Examples

* POSIX Pthreads (user library)
* Green Threads

---

## Memory Trick

**User Thread = User Manages Everything**

---

# B. Kernel-Level Threads (KLT)

## Definition

Managed directly by the **Operating System Kernel**.

OS knows every thread.

### Diagram

```text
Application
      │
Operating System Kernel
      │
Hardware
```

---

## Advantages

* Better scheduling
* True parallel execution
* One blocked thread does not stop others

---

## Disadvantages

* Slower creation
* Higher overhead

---

## Examples

* Windows Threads
* Linux Kernel Threads

---

## Memory Trick

**Kernel Thread = OS is the Boss**

---

# User Threads vs Kernel Threads

| User Threads                  | Kernel Threads         |
| ----------------------------- | ---------------------- |
| Managed by user library       | Managed by OS kernel   |
| Fast                          | Slower                 |
| Low overhead                  | High overhead          |
| OS not aware                  | OS aware               |
| No true parallelism           | True parallelism       |
| One blocked thread blocks all | Other threads continue |

---

# Process vs Thread

| Process                 | Thread                  |
| ----------------------- | ----------------------- |
| Heavyweight             | Lightweight             |
| Own memory              | Shared memory           |
| Slower creation         | Faster creation         |
| Communication is slower | Communication is faster |
| Higher overhead         | Lower overhead          |

---

# Real-Life Example

### Process = Browser

Threads:

* Thread 1 → Display webpage
* Thread 2 → Download images
* Thread 3 → Play video
* Thread 4 → Check network

All belong to the same browser process.

---

# 2-Mark Revision

### Thread

Smallest unit of CPU execution.

### Benefits

* Faster
* Resource sharing
* Better CPU utilization
* Easy communication
* Economy

### User Threads

* Managed by user library
* Fast
* OS unaware

### Kernel Threads

* Managed by OS
* Slower
* OS aware
* Better scheduling

---

# One-Line Revision

* **Thread:** Smallest unit of execution.
* **Process:** Collection of one or more threads.
* **Thread Shares:** **Code, Data, Files, Memory (CDFM)**.
* **Thread Owns:** **Program Counter, Registers, Stack (PCS)**.
* **User Thread:** Managed by user library.
* **Kernel Thread:** Managed by OS kernel.
* **Thread Benefits:** **FBERE** → Faster, Better CPU, Easy communication, Resource sharing, Economy.

---

# ⭐ Memory Cheatsheet

| Topic         | Memory Trick                                |
| ------------- | ------------------------------------------- |
| Thread        | Smallest unit of execution                  |
| Thread Owns   | **PCS** → Program Counter, Registers, Stack |
| Thread Shares | **CDFM** → Code, Data, Files, Memory        |
| Benefits      | **FBERE**                                   |
| User Thread   | **User manages everything**                 |
| Kernel Thread | **OS is the Boss**                          |
| Process       | Heavyweight                                 |
| Thread        | Lightweight                                 |
