<p align="center">
  <img src="./assets/profile-banner.svg" alt="Keaton Mott — Windows and Linux internals, useful scripts, and educational proofs of concept" width="100%" />
</p>

<p align="center">
  <strong>Windows internals · Linux internals · Practical scripts · Educational PoCs</strong>
</p>

<p align="center">
  <a href="https://github.com/Keatonmott?tab=repositories">Explore my repositories</a>
  &nbsp; / &nbsp;
  <a href="#windows-internals">Windows</a>
  &nbsp; / &nbsp;
  <a href="#linux-internals">Linux</a>
  &nbsp; / &nbsp;
  <a href="#educational-proofs-of-concept">PoCs</a>
</p>

## Hi, I'm Keaton

I'm interested in what happens beneath the interface: how operating systems manage processes, memory, permissions, and the resources applications depend on.

This GitHub will focus on **useful scripts, practical workflows, and possible tool developments related to Windows and Linux internals**, alongside **proofs of concept for educational purposes**. My aim is to connect an underlying mechanism to something you can inspect, reproduce, and understand.

## What I'll be sharing

### Windows internals

Scripts, examples, and workflows for exploring how Windows behaves beneath everyday applications. Areas I plan to cover include:

- **Processes, threads, and handles** — inspecting execution, object references, resource use, and how applications interact with the operating system.
- **Memory and execution** — examining virtual memory, allocations, modules, and the relationship between application code and Windows APIs.
- **Services, the registry, and permissions** — understanding configuration, execution context, access tokens, and access checks.
- **Debugging and observation** — using tools such as WinDbg, event logs, and tracing to work from a symptom toward an explanation.

### Linux internals

Practical investigations into Linux behavior, with scripts and documented workflows that make system state easier to inspect. Areas I plan to explore include:

- **Processes and signals** — examining process relationships, execution state, and communication.
- **System calls and file descriptors** — following how programs request kernel services and interact with files, pipes, and sockets.
- **Memory and system interfaces** — investigating virtual memory and the information exposed through `/proc` and `/sys`.
- **Permissions and isolation** — exploring ownership, capabilities, namespaces, and the boundaries between processes and their environment.
- **Debugging and tracing** — using tools such as GDB and strace to connect observed behavior with the code and system calls behind it.

### Useful scripts and repeatable workflows

The emphasis will be on tools with a specific job: gathering relevant system information, reducing repetitive inspection work, comparing system state, or making a diagnostic process easier to repeat.

Workflows will explain **the question being investigated, the environment, the steps taken, the expected observations, and what those observations mean**. Where behavior depends on an operating-system version, configuration, or privilege level, I'll document that context.

### Educational proofs of concept

Focused examples that demonstrate an operating-system mechanism, security concept, or interesting failure condition in a reproducible lab setting.

The goal is to explain **why something happens**, not just present a result. I intend to include the setup, relevant code, expected behavior, an explanation of the outcome, and the limitations of each example. These will be learning material, with experimental work clearly identified.

## Possible developments

Some scripts and workflows may grow into more complete utilities when there is a useful reason to do so. I'll distinguish small experiments, working prototypes, and more mature tools so their status is clear.

**Atlas** is one current local prototype: a native Windows filesystem manager exploring keyboard-driven navigation, file operations, and an adaptable interface. Its source is not published here yet; any future repository will describe the implemented features and remaining work.

## What I want each post to provide

| Part | Purpose |
| :--- | :--- |
| **A clear problem or question** | Explain what the script, workflow, or PoC is meant to address. |
| **Setup and prerequisites** | Identify the environment and requirements needed to reproduce it. |
| **Readable code and practical examples** | Make the implementation useful to study and adapt. |
| **Observations and explanation** | Show the output and connect it to the underlying system behavior. |
| **Limitations and status** | Be clear about what was tested, what is experimental, and what remains unfinished. |

These are the areas I plan to publish in. The repositories themselves will show what is currently available.

---

<p align="center"><sub>Inspect the system. Understand the mechanism. Build something useful.</sub></p>
