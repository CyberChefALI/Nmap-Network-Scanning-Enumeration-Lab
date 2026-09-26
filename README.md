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

nmap -sn 10.0.2.4/24

Discover which hosts are active on a target subnet without performing a full port scan.


(The -sn flag tells Nmap to only run host discovery and skip port scanning).<img width="1920" height="991" alt="meta  Running  - Oracle VirtualBox 26_09_2026 14_47_01" src="https://github.com/user-attachments/assets/6d88d0d2-a6ce-49ca-b51c-16d0f792fb64" />   

## STEP-3 •	TCP SYN Scan (Stealth Scan)

nmap -Ss 10.0.2.4

The default and most popular scan; it sends SYN packets and infers port states without completing the full 3-way handshake
<img width="1920" height="991" alt="kali-linux-2026 1-virtualbox-amd64  Running  - Oracle VirtualBox 26_09_2026 14_59_29" src="https://github.com/user-attachments/assets/c725994d-d8b3-4b26-9de9-8914bc60ed6d" />  

## STEP-4 Service & Version Detection

nmap -sV 10.0.2.4

Service & Version Detection means figuring out what application or program is running on an open port and its exact version number.
<img width="1920" height="991" alt="kali-linux-2026 1-virtualbox-amd64  Running  - Oracle VirtualBox 26_09_2026 15_18_31" src="https://github.com/user-attachments/assets/cbb5f616-ce6a-48d1-b997-56ce5300730a" /> 

## STEP-5  OS Detection

nmap -O 10.0.2.4

OS Detection (Operating System Detection) means using Nmap to figure out what operating system is running on a target device
<img width="1920" height="991" alt="Captures - File Explorer 26_09_2026 15_22_30" src="https://github.com/user-attachments/assets/0955b370-d8b3-43b8-aba4-661e6a33987f" />  

## STEP-6 Default script scan (NSE)

nmap -sC 10.0.2.4

Instead of just checking if a port is open, it automatically runs a collection of safe, pre-written scripts tailored to the specific services found
<img width="1920" height="991" alt="Captures - File Explorer 26_09_2026 15_34_52" src="https://github.com/user-attachments/assets/98948bed-555e-4213-8877-472c32e0bd0f" />  

## STEP-7  Firewall/Filtering Analysis

nmap -sA 10.0.2.4

Unlike most other scans, it is not used to find open ports. Instead, it is used to map out firewall rules and filter configurations
<img width="1920" height="991" alt="Captures - File Explorer 26_09_2026 15_44_58" src="https://github.com/user-attachments/assets/baeddf16-d839-4fa7-83fc-ba8869e6e3cc" />  

## STEP-8 comprehensive scan/Deep enumeration scan

 nmap -sC -sV -O 192.168.5.129 -oN scanreport.txt

<img width="1920" height="991" alt="kali-linux-2026 1-virtualbox-amd64  Running  - Oracle VirtualBox 26_09_2026 15_57_08" src="https://github.com/user-attachments/assets/620a882a-c622-44e1-b35e-9ebcfaa0595c" />
<img width="1920" height="991" alt="Captures - File Explorer 26_09_2026 15_56_09" src="https://github.com/user-attachments/assets/a7241e69-79bb-42e4-b503-b57aebbed5a8" />

## STEP-9 Aggressive reconnaissance command

nmap -sV  -p- -A -T4 10.0.2.4
<img width="1920" height="991" alt="kali-linux-2026 1-virtualbox-amd64  Running  - Oracle VirtualBox 26_09_2026 16_17_16" src="https://github.com/user-attachments/assets/2f57be2a-7ddf-49a9-a778-bdb3e334d7eb" />
<img width="1920" height="991" alt="kali-linux-2026 1-virtualbox-amd64  Running  - Oracle VirtualBox 26_09_2026 16_17_02" src="https://github.com/user-attachments/assets/dea15f94-a724-4bc6-a893-0f83db9e3c1d" />
<img width="1920" height="991" alt="kali-linux-2026 1-virtualbox-amd64  Running  - Oracle VirtualBox 26_09_2026 16_16_40" src="https://github.com/user-attachments/assets/0d59d77b-9ce4-40dd-b5f9-87b034d5f9fe" />  


## CONCLUSION:

In conclusion, this lab successfully demonstrated how to use Nmap for comprehensive network reconnaissance, ranging from rapid host discovery and stealth port scanning to deep service and OS fingerprinting. Mastering these techniques highlights not only how attackers map targets, but also why strict firewall configurations, regular auditing, and service hardening are vital for network defense.












