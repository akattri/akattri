# Akash

> Computer Science undergraduate focused on systems programming, concurrency, machine learning, and open-source software.

I am a second-year undergraduate pursuing a B.Tech in Computer Science and Engineering (Specialization in AI & ML) at SRM Institute of Science and Technology, Kattankulathur (graduating 2029).

My primary interest lies in understanding software systems beneath their abstractions—transitioning from high-level frameworks down to operating system interfaces, concurrency primitives, memory layouts, and hardware telemetry. I use Linux as my daily driver and build software to explore how core computer science fundamentals work in practice.

---

## What I'm Working On

- **Systems Programming in C**: Exploring POSIX system calls, process lifecycles, memory layout, file descriptors, and I/O redirection.
- **Concurrency & Synchronization**: Multithreaded programming with POSIX threads (`pthreads`), mutual exclusion locks, condition variables, and synchronization protocols.
- **Core Algorithms & Data Structures**: Deepening algorithmic problem-solving, asymptotic analysis, and foundational data structures through university-level curricula.
- **Systems for ML & Applied NLP**: Empirical hardware profiling (GPU/CPU utilization, VRAM footprint, power telemetry) during local model execution, and domain-specific text classification pipelines.
- **Linux & Unix Internals**: Deepening practical understanding of IPC, signals, process groups, virtual memory, and standard Unix tooling.

---

## Selected Projects

### [seashell](https://github.com/akattri/seashell)
*C99 • POSIX System Calls • Linux • Make*
- A compact, educational Unix shell implementing process lifecycle management (`fork`, `execvp`, `waitpid`), file descriptor redirection (`open`, `dup2`, `close`), and inter-process communication through unidirectional pipelines (`pipe`).
- Handles terminal signals (`SIGINT`, `sigaction`), implements shell builtins (`cd`, `pwd`, `export`), and manages background jobs with non-blocking zombie process reaping (`WNOHANG`).
- Includes an automated test suite with 29 behavioral test cases.
- **Core concepts**: Process creation, virtual address space duplication, file descriptor tables, IPC, terminal control.

### [thread-safe-queue](https://github.com/akattri/thread-safe-queue)
*C • POSIX Threads (pthreads) • Concurrency • Synchronization*
- A concurrent First-In, First-Out (FIFO) queue implemented from scratch in C supporting multiple producer and consumer threads without data races.
- Uses `pthread_mutex_t` for mutual exclusion and `pthread_cond_t` for event signaling, ensuring consumers sleep when the queue is empty rather than burning CPU cycles in busy-polling loops.
- Features a graceful shutdown signaling protocol and a multi-threaded test driver with checksum and count verification.
- **Core concepts**: Mutual exclusion, condition variable wait loops (spurious wakeup handling), thread lifecycle, memory safety in shared state.

### [llm-resource-mon](https://github.com/akattri/llm-resource-mon)
*Python • Linux Diagnostics • Telemetry • Matplotlib*
- A lightweight hardware telemetry tool to monitor GPU compute utilization, VRAM allocation, on-board GPU power draw (`nvidia-smi`), and CPU load (`psutil`) during local LLM inference via Ollama.
- Logs empirical metrics to CSV at fixed sampling intervals, calculates summary statistics, estimates approximate GPU energy consumption (Joules/Watt-hours), and generates telemetry plots.
- **Core concepts**: Empirical hardware profiling, cold-start vs. warm-start memory caching behavior, Green AI / operational energy measurement.

### [github-issue-classifier](https://github.com/akattri/github-issue-classifier)
*Python • Scikit-learn • NLTK • REST APIs*
- A machine-learning pipeline designed to automate issue triage on GitHub repositories by classifying issues into security and non-security categories based on title and body text.
- Covers data collection via GitHub REST API, text preprocessing with NLTK, TF-IDF n-gram feature extraction, and Multinomial Naive Bayes classification with stratified train-test evaluation.
- **Core concepts**: Text preprocessing in developer domains, class-imbalance evaluation, NLP feature representation.

### [Archon](https://github.com/akattri/Archon)
*JavaScript • Chrome Extensions API (Manifest V3) • OAuth 2.0*
- A browser productivity dashboard extension that consolidates bookmarks, local task management, and Google Calendar agenda synchronization via OAuth 2.0.
- **Core concepts**: Non-persistent background service workers, browser security models, asynchronous client-side storage.

### [akattri.github.io](https://akattri.github.io)
*Hugo • Markdown • Git*
- Personal academic portfolio and technical notebook documenting coursework, systems engineering takeaways, and project design notes.
- **Source**: [akattri/akattri.github.io](https://github.com/akattri/akattri.github.io)

---

## Coursework & Foundations

### Completed
- **Harvard University — CS50x: Introduction to Computer Science**
  - C programming, manual memory management (`malloc`, `free`), pointers, data structures (linked lists, hash tables, tries), algorithmic complexity ($\mathcal{O}$, $\Omega$, $\Theta$), sorting/search, SQL, and foundational web concepts.
- **Linux Essentials**
  - Linux operating system architecture, file system hierarchy standard (FHS), permissions and security, process management, and shell scripting.

### In Progress
- **University of Helsinki — Java Programming I & II (MOOC.fi)**
  - Object-oriented programming, data structures, modular software design, interfaces, generics, and automated unit testing with JUnit.
- **SRM Institute of Science and Technology — B.Tech CSE (Year 2, Semester 3)**
  - Core curriculum in data structures, object-oriented paradigms, and discrete mathematics.

### Planned
- **Princeton University — Algorithms, Part I & II** (*Robert Sedgewick, Kevin Wayne / Coursera*)
  - Elementary sorts, balanced search trees (Red-Black BSTs), priority queues, graph algorithms (DFS, BFS, MST, shortest paths), string sorts, and intractability.
- **Harvard University — CS50 AI / CS50 Web**
  - Heuristic search, probabilistic models, machine learning fundamentals, and distributed web architectures.
- **Computer Systems & Operating Systems**
  - Self-directed exploration of virtual memory, paging, kernel-user mode transitions, and CPU scheduling.

---

## Technical Focus

```
Languages    : C (C99), Python, Java, Bash, SQL
Environment  : Linux (Debian, Fedora, Ubuntu), GCC/Clang, Make, GDB, Valgrind, Neovim, Git
Interests    : Operating Systems, Concurrency, Algorithms, Applied NLP, Systems for ML
```

---

## Open Source & Academic Goals

I am actively building the low-level systems, concurrency, and algorithmic foundation needed to contribute meaningfully to established open-source software and systems infrastructure. 

My longer-term goal is to pursue university research internships and open-source mentorship programs (such as Google Summer of Code and LFX Mentorship) centered on computer systems, operating systems, and systems for machine learning.

---

## Links

- **Website**: [akattri.github.io](https://akattri.github.io)
- **GitHub**: [github.com/akattri](https://github.com/akattri)
- **LinkedIn**: [linkedin.com/in/akattri](https://www.linkedin.com/in/akattri)
- **Email**: [akashattri62@gmail.com](mailto:akashattri62@gmail.com)

# akattri
