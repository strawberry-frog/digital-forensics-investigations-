[linux-system-forensics-README.md](https://github.com/user-attachments/files/32971600/linux-system-forensics-README.md)
# 🐧🔎 Linux System Forensics Investigation

**Graduate Computer Forensics Coursework --- James Madison University,
CS 633**

## Overview

This case study documents a forensic investigation of a simulated Linux
workstation involved in a suspected theft of company information. The
goal was to reconstruct user and system activity from a forensic disk
image, identify relevant artifacts, and build an evidence-based
timeline.

> **Portfolio note:** This is a sanitized summary of an educational lab.
> Case names and events come from the course scenario. Raw evidence,
> account identifiers, and lengthy evidentiary appendices are
> intentionally omitted.

## Tools & Evidence

-   **Autopsy 4.22.1**
-   Linux forensic disk image (`.dd`)
-   Linux authentication and system artifacts
-   User command history
-   Browser and web artifacts
-   File-system metadata and timestamps

## Investigation Process

I examined the forensic image to identify user profiles, system
activity, file activity, authentication events, and web artifacts
relevant to the incident.

The investigation included:

-   Reviewing Linux authentication activity and SSH connection attempts.
-   Examining user and group activity associated with the system
    timeline.
-   Tracking creation, modification, access, and deletion of files
    relevant to the case.
-   Comparing file-system timestamps with user activity and
    command-history evidence.
-   Reviewing browser and email-related artifacts to correlate activity
    with events found elsewhere on the system.
-   Identifying inconsistencies between file activity and command
    history rather than relying on a single artifact as proof.
-   Building a chronological timeline to connect system events across
    multiple sources.

## Key Technical Work

### Authentication & SSH Analysis

The forensic image contained repeated SSH authentication activity,
including rejected connection attempts and a smaller number of accepted
sessions. I incorporated these events into the timeline alongside local
user activity to determine when potentially relevant access occurred.

### File-System & Metadata Analysis

I tracked relevant files through their creation, access, modification,
and deletion timestamps. Several files had activity that required
comparison with other artifacts because the apparent timing or user
attribution was not internally consistent.

Rather than treating timestamps in isolation, I compared them with
command histories and other system activity to determine where
additional investigation was warranted.

### User Activity Reconstruction

I correlated artifacts associated with multiple user profiles to
reconstruct what occurred on the workstation. This included
command-history evidence, browser activity, email-related artifacts,
authentication records, and file-system events.

### Timeline Development

The final investigation organized relevant events chronologically,
including:

-   authentication and SSH activity,
-   user sessions,
-   changes to users/groups,
-   creation and modification of sensitive files,
-   browser and email activity,
-   creation and deletion of suspicious files.

The timeline made it possible to compare activity across different
evidence sources and identify inconsistencies that were difficult to see
when examining artifacts individually.

## Findings

The investigation supported the course scenario's conclusion that
sensitive company information had left the local workstation. The
strongest value of the analysis was not a single artifact, but the
correlation of system, file, authentication, browser, and user-history
evidence into a broader incident timeline.

## Skills Demonstrated

`Digital Forensics` `Linux` `Autopsy` `Disk Image Analysis`
`File-System Analysis` `Metadata Analysis` `Timeline Analysis` `SSH`
`Authentication Logs` `Incident Investigation` `Evidence Correlation`
`Technical Reporting`

## What I Learned

This investigation reinforced the importance of correlating evidence
from multiple sources. File timestamps, user histories, authentication
activity, and browser artifacts can each provide useful context, but
they become much more meaningful when evaluated together as part of a
timeline.

It also demonstrated why forensic conclusions should account for
inconsistencies in metadata and user attribution rather than assuming
every artifact is complete or independently reliable.
