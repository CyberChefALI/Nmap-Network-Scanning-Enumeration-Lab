# Nmap-Network-Scanning-Enumeration-Lab

## Introduction:-

* Nmap is an open-source network scanning and security auditing tool used to discover hosts, identify open ports, detect running services, and gather information about target systems. This project demonstrates practical network reconnaissance and enumeration using Nmap in an isolated Metasploitable 2 laboratory environment.*

## Overview :-

In this project, Nmap was used to perform host discovery, full TCP port scanning, service and version detection, OS detection, NSE script scanning, and firewall/packet-filtering analysis against a Metasploitable 2 virtual machine. The scan results were documented using command outputs and screenshots.

## Tools Used :-

Kali Linux — scanning platform Nmap 7.99 — network scanning and enumeration Metasploitable 2 — intentionally vulnerable target VM VMware 

## Nmap-Network-Scanning-lab

Host Discovery Port Scanning Service & Version Detection OS Detection NSE Script Scanning Firewall Detection Scan Report

## STEP-1 Environment Verification & Tool Setup

Before running scans, verify your interface settings and explore the Nmap utility syntax.
<img width="1920" height="991" alt="kali-linux-2026 1-virtualbox-amd64  Running  - Oracle VirtualBox 26_09_2026 14_15_05" src="https://github.com/user-attachments/assets/06891211-cc85-46e2-be24-6741e5f1a1c2" /> 

## STEP-2 HOST DISCOVERY

Discover which hosts are active on a target subnet without performing a full port scan.
nmap -sn 10.0.2.4/24
(The -sn flag tells Nmap to only run host discovery and skip port scanning).<img width="1920" height="991" alt="meta  Running  - Oracle VirtualBox 26_09_2026 14_47_01" src="https://github.com/user-attachments/assets/6d88d0d2-a6ce-49ca-b51c-16d0f792fb64" />


