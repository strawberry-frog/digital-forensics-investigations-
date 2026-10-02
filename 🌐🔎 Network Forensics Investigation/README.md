[network-forensics-README.md](https://github.com/user-attachments/files/32971720/network-forensics-README.md)
# 🌐🔎 Network Forensics Investigation

**Graduate Computer Forensics Coursework --- James Madison University,
CS 633**

## Overview

This case study documents a network-forensics investigation of a
simulated corporate incident. I analyzed a large packet capture to
identify communications relevant to the case, reconstruct network
activity, correlate users with traffic, and connect network evidence
with findings from an earlier host-forensics investigation.

> **Portfolio note:** This is a sanitized summary of an educational lab.
> The original report contains raw packet evidence and course-scenario
> identifiers that are intentionally omitted here.

## Tools

-   **Wireshark**
-   **xxd**
-   **Binwalk**
-   PCAP files
-   TCP/HTTP stream reconstruction
-   Hex and ASCII inspection

## Protocols & Traffic Examined

`TCP` `HTTP` `TLS` `SSH` `DNS` `ICMP`

## Investigation Process

The packet capture contained a large volume of traffic, so I narrowed
the dataset through targeted filtering and stream analysis.

My workflow included:

-   filtering packets by IP address, protocol, strings, and other
    case-relevant indicators,
-   searching packet details for identifiers associated with known
    users,
-   isolating relevant traffic into smaller PCAP files,
-   merging filtered packet sets to create clearer investigative views,
-   reconstructing TCP and HTTP streams,
-   reviewing stream contents in ASCII and hexadecimal form,
-   exporting HTTP objects for additional inspection,
-   using `xxd` and Binwalk to examine exported content and look for
    embedded or hidden data,
-   reviewing unusual ports, repeated HTTP errors, ICMP activity, and
    other suspicious traffic patterns.

## Key Technical Work

### TCP/HTTP Stream Reconstruction

I identified TCP/HTTP streams containing communications relevant to the
simulated incident. Reconstructing these streams provided context that
was difficult to obtain from individual packets and helped connect email
activity, transferred attachments, and later communications.

### HTTP Object Extraction

I exported HTTP objects from Wireshark and examined selected content
outside the packet capture. `xxd` provided a hexadecimal view of data,
while Binwalk was used to inspect content for embedded data.

### User Attribution Under Shared Network Identifiers

A major challenge was that multiple users' outbound traffic appeared
under the same network identifiers in the course environment. IP and MAC
addresses alone therefore were not sufficient for attribution.

To distinguish activity, I correlated additional packet-level evidence,
including:

-   account/email identifiers,
-   cookie identifiers,
-   hardware-related information available in traffic,
-   application activity,
-   timing and surrounding network events.

This required treating attribution as a correlation problem rather than
assuming one IP address represented one user.

### Suspicious Traffic Analysis

I also examined traffic outside the primary incident path, including
unusual ports, large numbers of HTTP error responses, ICMP unreachable
traffic, and a stream that appeared to expose privileged account
information. Where the evidence was not conclusive, the original report
identified the activity as requiring further investigation rather than
treating suspicion alone as proof.

### Cross-Source Timeline Correlation

The network capture provided timestamps, addresses, streams, and
communications that could be compared with the earlier Linux workstation
investigation. Combining host and network evidence produced a more
complete timeline than either source alone.

## Findings

The analysis identified network communications relevant to the simulated
data-theft scenario, including an email attachment associated with the
incident and later communications concerning access to externally stored
information.

The investigation also demonstrated the value of network evidence when
host artifacts contain ambiguous or inconsistent timing. Packet captures
can provide an independent source of event timing and communication
context, although encrypted traffic and shared network identifiers can
limit what can be concluded from individual packets.

## Skills Demonstrated

`Network Forensics` `Wireshark` `PCAP Analysis` `Packet Analysis`
`TCP/IP` `HTTP` `TLS` `SSH` `DNS` `ICMP` `TCP Stream Reconstruction`
`Traffic Filtering` `HTTP Object Extraction` `xxd` `Binwalk`
`Evidence Correlation` `Incident Investigation`
`Forensic Timeline Analysis`

## What I Learned

This project strengthened my ability to work through a high-volume
packet capture methodically. The most important challenge was
attribution: when IP and MAC information could not uniquely identify a
user, I had to correlate multiple artifacts and network indicators
before drawing conclusions.

It also showed how host and network forensics complement each other.
Host artifacts provide detailed local context, while network captures
can provide independent timing and communication evidence that helps
validate or challenge the host-based timeline.
