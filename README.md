# Akash

<p>
  <strong>CS Undergraduate (AI & ML)</strong> · SRM Institute of Science & Technology · <em>Class of 2029</em><br>
  <code>systems programming</code> · <code>concurrency</code> · <code>unix internals</code> · <code>algorithms</code> · <code>applied ml</code>
</p>

<p>
  <a href="https://akattri.github.io"><strong>Website</strong></a> &nbsp;•&nbsp;
  <a href="https://github.com/akattri"><strong>GitHub</strong></a> &nbsp;•&nbsp;
  <a href="https://www.linkedin.com/in/akattri"><strong>LinkedIn</strong></a> &nbsp;•&nbsp;
  <a href="mailto:akashattri62@gmail.com"><strong>Email</strong></a>
</p>

I am an undergraduate focused on understanding software systems beneath their abstractions. Rather than chasing ephemeral frameworks, I spend my time writing C, studying operating system primitives, experimenting with concurrency, and observing how machine learning workloads behave on physical hardware.

---

### `/now`

A real-time snapshot of current technical focus:

| Domain | Target | Focus & Primitives | State |
| :--- | :--- | :--- | :--- |
| **Systems** | [`seashell`](https://github.com/akattri/seashell) | Unix shell in C99 · `fork()`/`execvp()` · pipelines · redirection · signal handling | `● Active` |
| **Concurrency** | [`thread-safe-queue`](https://github.com/akattri/thread-safe-queue) | POSIX threads (`pthreads`) · `mutex` · condition variables · race prevention | `● Active` |
| **OOP & Testing** | Univ. of Helsinki Java | Software construction · data structures · unit testing with JUnit | `● Active` |
| **Algorithms** | Princeton Algorithms I & II | Sedgewick & Wayne · asymptotic analysis · balanced trees · graphs | `○ Queued` |
| **Systems for ML** | [`llm-resource-mon`](https://github.com/akattri/llm-resource-mon) | Linux hardware telemetry · `nvidia-smi` + `psutil` · VRAM / power profiling | `● Refining` |

---

### `/code`

#### Primary Systems Work

##### [`seashell`](https://github.com/akattri/seashell) — Educational Unix Shell
`C99` · `POSIX System Calls` · `Process Management` · `IPC` · `Make`

An educational Unix shell built in C99 to understand operating system primitives from the ground up:
- **Process Orchestration**: Process creation and lifecycle tracking via `fork()`, `execvp()`, and `waitpid()`.
- **I/O Redirection & IPC**: File descriptor duplication via `dup2()` (`<`, `>`, `>>`) and unidirectional inter-process communication pipelines via `pipe()`.
- **Signals & Job Control**: Signal routing (`SIGINT`, `sigaction`), builtin execution in the parent process (`cd`, `pwd`, `export`), and non-blocking background zombie reaping (`WNOHANG`).
- **Validation**: 29-case automated behavioral test suite (`tests/test_shell.sh`).
- *Why it exists*: To understand how Unix processes, file descriptor tables, and terminal control operate directly against kernel syscalls rather than libc wrappers.

##### [`thread-safe-queue`](https://github.com/akattri/thread-safe-queue) — Concurrent FIFO Queue
`C` · `POSIX Threads (pthreads)` · `Mutual Exclusion` · `Condition Variables`

A concurrent First-In, First-Out queue in C supporting multiple simultaneous producer and consumer threads:
- **Synchronization Mechanics**: Guards shared mutable state (`front`, `rear`, `size`) with `pthread_mutex_t`. Synchronizes producer-consumer flow with `pthread_cond_t` so consumer threads sleep when idle rather than burning CPU in busy-wait loops.
- **Defensive Concurrency**: Wraps condition waits in `while` loops to protect against spurious wakeups; features a shutdown broadcast protocol to wake all blocked threads and drain memory cleanly.
- **Verification**: Multi-threaded test harness simulating concurrent producers and consumers with checksum and count verification.
- *Why it exists*: To confront race conditions, lock contention, and memory ordering bugs in multi-core execution firsthand.

#### Experiments & Tooling

| Repository | Stack | Scope & Key Mechanism |
| :--- | :--- | :--- |
| **[`llm-resource-mon`](https://github.com/akattri/llm-resource-mon)** | `Python` · `nvidia-smi` · `psutil` | Standalone telemetry probe sampling GPU compute load, VRAM allocation, and power draw (W) during local LLM inference (Ollama). Computes approximate energy consumption (J / Wh) and plots cold vs. warm start memory caching profiles. |
| **[`github-issue-classifier`](https://github.com/akattri/github-issue-classifier)** | `Python` · `scikit-learn` · `NLTK` | Automated NLP pipeline for triaging GitHub issues. Fetches raw issues via GitHub REST API, cleans developer prose, and classifies security vs. non-security reports using TF-IDF n-grams and Multinomial Naive Bayes. |
| **[`Archon`](https://github.com/akattri/Archon)** | `JavaScript` · `Manifest V3` · `OAuth 2.0` | Client-only browser productivity new-tab dashboard integrating Chrome bookmarks and Google Calendar agenda sync using event-driven background service workers and asynchronous local storage. |
| **[`akattri.github.io`](https://akattri.github.io)** | `Hugo` · `Markdown` · `CSS` | Personal engineering notebook and academic portfolio documenting systems notes, coursework logs, and project retrospectives. |

---

### `/foundations`

A deliberate progression emphasizing core computer science over framework churn:

| Stage | Domain | Curriculum & Milestones | Status |
| :---: | :--- | :--- | :--- |
| `01` | **Low-Level Foundations** | Harvard CS50x · Linux Essentials<br>*(Manual memory management, pointers, linked lists, hash tables, tries, Linux FHS, shell scripting)* | `Completed` |
| `02` | **Software Construction** | University of Helsinki Java Programming I & II<br>*(Object-oriented architecture, collection internals, defensive design, unit testing with JUnit)* | `Active` |
| `03` | **Systems & Concurrency** | POSIX System Calls · Concurrency in C<br>*(Process lifecycles, virtual memory layouts, `pthreads`, mutexes, condition variables, Seashell)* | `Active` |
| `04` | **Algorithms & Complexity** | Princeton University Algorithms, Part I & II *(Sedgewick & Wayne)*<br>*(Balanced search trees, graph algorithms, minimum spanning trees, network flow, intractability)* | `Queued` |
| `05` | **Systems for Machine Learning** | Local inference telemetry · memory bottlenecks · applied NLP · systems research | `Exploring` |

---

### `/environment`

```
OS / Kernel  : Linux (Fedora, Debian, Ubuntu) · POSIX
Languages    : C (C99), Python, Java, Bash, SQL
Toolchain    : GCC / Clang, GNU Make, GDB, Valgrind, Git, Neovim
Focus        : Operating Systems, Concurrency Primitives, Algorithms, Systems for ML
```

---

### `/notes`

> *"I like understanding what happens underneath the abstraction."*

Most of my computer science interests trace back to using Linux as a daily driver. Once you see the predictable modularity of Unix—small utilities communicating across pipes, processes arbitrated by kernel schedulers, and memory managed with precision—it becomes difficult to treat software as an opaque layer.

I am intentionally spending my early university semesters building strong mental models of memory, processes, and synchronization before specializing in systems and machine learning.

My longer-term goal is to pursue university research internships and open-source systems mentorship programs (such as Google Summer of Code and LFX Mentorship).

---

<p align="center">
  <small>
    <a href="https://akattri.github.io">akattri.github.io</a> &nbsp;•&nbsp;
    <a href="https://github.com/akattri">github.com/akattri</a> &nbsp;•&nbsp;
    <a href="https://www.linkedin.com/in/akattri">linkedin.com/in/akattri</a> &nbsp;•&nbsp;
    <a href="mailto:akashattri62@gmail.com">akashattri62@gmail.com</a>
  </small>
</p>
