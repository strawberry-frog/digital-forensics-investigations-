[README-digital-forensics-investigations.md](https://github.com/user-attachments/files/32971395/README-digital-forensics-investigations.md)
# 🔎 Digital Forensics Investigations

A collection of graduate cybersecurity projects exploring **Linux system
forensics, network forensics, and malware/binary analysis**.

These projects were completed as part of **CS 633 --- Computer Forensics
at James Madison University** and demonstrate hands-on experience
analyzing forensic evidence, reconstructing system and network activity,
examining unknown binaries, and documenting technical findings.

> **Portfolio Note:** All investigations in this repository were
> completed in controlled academic environments using course-provided
> scenarios and evidence. They do not represent real criminal
> investigations or incidents involving actual organizations.

------------------------------------------------------------------------

## 🐧 Linux System Forensics Investigation

Investigated a simulated Linux workstation involved in a suspected
information-theft incident.

The investigation focused on correlating multiple sources of host-based
evidence to reconstruct user and system activity.

### Technical work included

-   Examining a Linux forensic disk image with **Autopsy**
-   Analyzing authentication and SSH activity
-   Reviewing command-history and browser-related artifacts
-   Examining file-system metadata and timestamps
-   Tracking file creation, modification, access, and deletion
-   Comparing artifacts to identify inconsistencies in timing and
    attribution
-   Building a chronological forensic timeline from multiple evidence
    sources

**Tools & concepts:** `Linux` `Autopsy` `Disk Image Analysis`
`File-System Analysis` `Metadata Analysis` `SSH` `Authentication Logs`
`Timeline Analysis`

➡️ See the **Linux System Forensics** folder for the full case study.

------------------------------------------------------------------------

## 🧬 Linux Binary & Malware Analysis

Analyzed an unknown Linux binary in a controlled environment to
determine its behavior and reconstruct its underlying logic.

The project combined behavioral testing with assembly-level analysis and
C programming.

### Technical work included

-   Observing program behavior in a controlled Linux environment
-   Disassembling the binary with **objdump**
-   Analyzing **x86-64 assembly**
-   Identifying library and system-function calls
-   Tracing conditional jumps and control flow
-   Analyzing socket and command-execution behavior
-   Reconstructing the program's functionality in **C**
-   Comparing the reconstructed program with the original binary
-   Using **Wireshark** to observe associated network behavior

Functions encountered during analysis included behavior associated with
`socket`, `htons`, `fgets`, `popen`, `fread`, `sendto`, and `pclose`.

**Tools & concepts:** `Malware Analysis` `Reverse Engineering`
`Binary Analysis` `Static Analysis` `Linux` `C` `x86-64 Assembly`
`objdump` `Wireshark` `Socket Programming`

➡️ See the **Linux Binary & Malware Analysis** folder for the full case
study.

------------------------------------------------------------------------

## 🌐 Network Forensics Investigation

Analyzed a large packet capture from a simulated corporate incident to
identify relevant communications, reconstruct network activity, and
correlate network evidence with host-based forensic findings.

### Technical work included

-   Filtering and analyzing **PCAP** traffic in Wireshark
-   Examining TCP, HTTP, TLS, SSH, DNS, and ICMP traffic
-   Reconstructing TCP and HTTP streams
-   Isolating and merging relevant packet sets
-   Exporting HTTP objects from network traffic
-   Inspecting exported data with **xxd** and **Binwalk**
-   Investigating unusual ports and suspicious traffic patterns
-   Correlating account, cookie, timing, and packet-level information
    when IP/MAC information alone was insufficient for attribution
-   Comparing network evidence with host-forensics findings to develop a
    more complete incident timeline

**Tools & concepts:** `Network Forensics` `Wireshark` `PCAP Analysis`
`TCP/IP` `HTTP` `TLS` `SSH` `DNS` `ICMP` `Traffic Analysis`
`TCP Stream Reconstruction` `xxd` `Binwalk`

➡️ See the **Network Forensics** folder for the full case study.

------------------------------------------------------------------------

## 🧰 Tools & Technologies

  -----------------------------------------------------------------------
  Area                                Tools / Technologies
  ----------------------------------- -----------------------------------
  Host Forensics                      Linux, Autopsy, disk-image
                                      analysis, file-system metadata

  Network Forensics                   Wireshark, PCAP analysis, TCP/HTTP
                                      stream reconstruction

  Binary Analysis                     objdump, x86-64 assembly, static
                                      analysis

  Programming                         C

  Data Inspection                     xxd, Binwalk

  Networking                          TCP/IP, HTTP, TLS, SSH, DNS, ICMP

  Investigation                       Timeline reconstruction, artifact
                                      correlation, technical reporting
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 🎯 Skills Demonstrated

-   Digital forensics
-   Linux system analysis
-   Network forensics
-   PCAP and packet analysis
-   Malware and binary analysis
-   Reverse engineering
-   x86-64 assembly analysis
-   C programming
-   File-system and metadata analysis
-   Evidence correlation
-   Forensic timeline reconstruction
-   Technical investigation and reporting

------------------------------------------------------------------------

## 📁 Repository Structure

``` text
digital-forensics-investigations/
│
├── README.md
│
├── linux-system-forensics/
│   └── README.md
│
├── malware-binary-analysis/
│   └── README.md
│
└── network-forensics/
    └── README.md
```

Each folder contains a sanitized case study explaining the **objective,
tools, investigation process, technical work, findings, and skills
demonstrated** for that project.

Raw forensic evidence and lengthy course-report appendices are
intentionally excluded from this public portfolio.

------------------------------------------------------------------------

## 🎓 Academic Context

These projects were completed as graduate-level Computer Forensics
coursework at **James Madison University**.

The repository is intended to document the technical methods and skills
I practiced during the investigations while presenting the work in a
concise portfolio format.

The projects emphasize an important theme across digital forensics:
**individual artifacts rarely tell the entire story**. Host activity,
file-system metadata, authentication records, network traffic, and
program behavior become significantly more useful when they are
correlated and evaluated together.
