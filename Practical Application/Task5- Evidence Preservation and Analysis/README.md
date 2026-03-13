# Evidence Preservation and Analysis

## Overview

This project demonstrates the process of collecting and preserving digital forensic evidence using Velociraptor and PowerShell. The objective is to capture volatile system data and memory artifacts while maintaining evidence integrity and proper documentation.

This task simulates a Security Operations Center (SOC) investigation scenario.

## Tools Used

- Velociraptor
- FTK Imager
- PowerShell
- Windows Virtual Machine

# Step 1: Volatile Data Collection

Volatile data refers to information stored in system memory or active processes that can be lost when the system shuts down.

To collect volatile network connection data, the Velociraptor artifact:

Windows.Network.Netstat

was executed on the Windows SOC virtual machine.

This artifact retrieves active network connections using the `netstat()` query.

The collected data includes:

- Process ID (PID)
- Process Name
- Local Address
- Remote Address
- Port Numbers
- Connection Status

This information helps identify suspicious communication or possible command-and-control connections.

# Step 2: Memory Acquisition

Memory acquisition is an important step in digital forensics because malicious code often resides in system memory.

The Velociraptor artifact used:

Artifact.Windows.Memory.Acquisition

This artifact collects a memory dump from the system for forensic investigation.

The memory dump can later be analyzed using forensic tools such as FTK Imager or Volatility.

# Step 3: Evidence Integrity Verification

To ensure the integrity of the collected memory dump, a SHA256 hash was generated using PowerShell.

Command used:

CertUtil -hashfile memory_dump.raw SHA256

Hashing ensures the evidence has not been altered and maintains forensic integrity.


# Chain of Custody

| Item | Description | Collected By | Date | Hash Value |
|-----|-------------|-------------|------|------------|
| Memory Dump | Server-Y Dump | SOC Analyst | 2025-08-18 | 398c654ef2aeb9805d3263617863e93d34fb0c7547a5e7ed8c2f379c6d4d1fae |


# Conclusion

This investigation demonstrates how forensic analysts can collect volatile data and system memory evidence using Velociraptor while preserving evidence integrity through hashing and documentation.

These techniques are commonly used in digital forensic investigations and incident response operations in modern Security Operations Centers.
