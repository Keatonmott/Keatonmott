<p align="center">
  <img src="./assets/profile-banner.svg" alt="Keaton Mott — stock Windows security and educational security research" width="100%" />
</p>

<p align="center">
  <strong>Stock Windows security · Active Directory · Protocol fuzzing · Educational PoCs</strong>
</p>

<p align="center">
  <a href="https://github.com/Keatonmott?tab=repositories">Repositories</a>
  &nbsp; / &nbsp;
  <a href="#stock-windows-security">Windows security</a>
  &nbsp; / &nbsp;
  <a href="#active-directory-security">AD security</a>
  &nbsp; / &nbsp;
  <a href="#protocol-fuzzing">Fuzzing</a>
</p>

## Hi, I'm Keaton

I am interested in the security of Windows as it ships.

I want to understand the default attack surface before extra roles or third-party products change the system. That means looking at the parts people rely on every day and asking how they behave under stress.

This GitHub will hold useful scripts and repeatable workflows. It will also hold possible tool developments and educational proofs of concept.

Windows comes first. Linux research will follow after the Windows work has a solid base.

## Stock Windows security

The first phase will study a clean Windows installation. I want a clear picture of what is enabled and what trusts what.

Areas of interest include:

- Default services and scheduled tasks
- Processes and threads
- Handles and object lifetimes
- Access tokens and integrity levels
- ACLs and local privilege boundaries
- Registry persistence points
- COM and RPC surfaces
- Drivers and user-to-kernel boundaries
- Event logs and ETW providers
- Defender and firewall behavior
- Native APIs and system call paths

The work will start with observation. Scripts will collect state and compare changes after a controlled action.

Debugging will go deeper when the evidence points there. WinDbg and Application Verifier may be used with page heap or targeted tracing.

The goal is to explain the path from input to behavior. A useful result should show which component handled the input and why the result matters.

## Active Directory security

Active Directory will be the next major Windows focus. The work will begin with small lab domains and documented trust boundaries.

Planned areas include:

- Domain joins and machine accounts
- Kerberos tickets and delegation
- NTLM fallback behavior
- LDAP queries and directory permissions
- DNS integration and dynamic updates
- SMB shares and session security
- RPC endpoints and remote management
- Group Policy processing
- Service accounts and SPNs
- Delegated rights and nested groups
- AD Certificate Services
- Trust relationships and attack paths
- Logging and detection coverage

I want to trace how identity moves through the domain. That includes the point where a local decision becomes a domain decision.

Each AD workflow will show the lab design and the expected security boundary. It will also show the evidence that supports the conclusion.

## Protocol fuzzing

Protocol fuzzing will focus on parsers and state machines in controlled environments. Targets may include DNS and SSH plus Kerberos.

AD-related work may also cover LDAP and SMB plus RPC. The exact target will depend on what can be isolated and measured safely.

I plan to explore several fuzzing styles:

- Mutation fuzzing from known-good traffic
- Generation fuzzing from a protocol model
- Coverage-guided fuzzing
- Structure-aware fuzzing
- Stateful sequence fuzzing
- Differential testing between implementations
- Replay-based regression testing

A harness should make the target easy to drive and easy to observe. It should also keep each test case repeatable.

The useful part is not a pile of random crashes. The useful part is a minimized input with a clear execution path and a reasoned explanation.

## Custom harnesses and educational PoCs

Some findings need a custom harness before they can be understood. I plan to build small harnesses around the affected parser or API.

Memory safety research may cover:

- Use-after-free conditions caused by dangling pointers
- Double-free conditions
- Out-of-bounds reads or writes
- Integer overflow and truncation
- Race conditions
- Invalid lifetime transitions
- Unexpected state reuse

A use-after-free PoC should show when the object is released and when the stale reference is used. It should also show which allocation replaces the old object when that detail matters.

The harness will aim for deterministic reproduction. Crash capture and debugger traces will support the analysis.

The work will stop at controlled reproduction and root-cause analysis. The purpose is education and defensive understanding.

## Useful scripts and workflows

Scripts will have a specific job. A script may inventory a surface or collect evidence from a test.

Workflows will be written so another person can repeat them. Each one should include:

1. The question being tested
2. The lab setup
3. The required privilege level
4. The input or trigger
5. The expected behavior
6. The observed behavior
7. The debugger or log evidence
8. The limits of the conclusion
9. Possible mitigations or detection ideas

I will mark work as planned or experimental or working. Published results will say what was actually tested.

## Linux later

Linux internals will come later. That work may cover system calls and namespaces plus capabilities.

It may also cover memory behavior and service isolation plus protocol implementations. The same rule will apply: show the mechanism and document the evidence.

---

<p align="center"><sub>Inspect the boundary. Reproduce the behavior. Explain the cause.</sub></p>
