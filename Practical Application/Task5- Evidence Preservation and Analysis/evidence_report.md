# Evidence Collection Report

## Investigator
SOC Analyst

## System
Windows SOC Virtual Machine

## Tools Used
- Velociraptor
- PowerShell

## Evidence Collected

1. Volatile Network Connections
Artifact used: Windows.Network.Netstat

2. System Memory Dump
Artifact used: Artifact.Windows.Memory.Acquisition

## Hash Verification

The collected memory dump was verified using SHA256 hashing to maintain evidence integrity.

Command used:

CertUtil -hashfile memory_dump.raw SHA256

## Notes

All evidence was collected in a controlled virtual lab environment for digital forensics training purposes.
