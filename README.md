# Home Lab

## Introduction

A cybersecurity home lab is a controlled environment used to simulate real-world network and security scenarios, allowing for hands-on practice in a safe setting. VirtualBox, an open-source software, enables users to run multiple virtual machines (VMs) on a single host machine, with each VM operating as a separate computer. This setup facilitates safe experimentation with security tools, malware analysis, and network configurations without impacting the host system.

## Objective

The primary objective of this home lab is to create a secure environment for testing cybersecurity concepts and performing activities like malware analysis, threat hunting, and vulnerability assessments. Once configured, the lab can also be used to study network traffic, evaluate security tools, and refine cybersecurity skills through real-world simulations.

### Skills Learned

- Virtualization Management
    - Installing and configuring VirtualBox and managing multiple virtual machines (VMs) independently.
    - Familiarity with different virtualization settings and understanding their impact on VM performance and security.

- Network Configuration
    - Setting up various network modes (NAT, Bridge, Internal Network, Host-Only) in VirtualBox to control connectivity and isolate environments as needed.
    - Practical knowledge of network isolation, essential for malware analysis and secure testing.

- IP Addressing and Network Troubleshooting
    - Assigning static IP addresses to VMs and verifying connectivity using tools like ipconfig and ifconfig.
    - Basic troubleshooting skills to resolve connectivity issues between virtual machines, an important skill for network diagnostics.

- Security Awareness and Isolation Techniques
    - Implementing secure practices, such as using isolated internal networks to prevent potential malware from impacting the host.
    - Understanding how to safely analyze suspicious software in a contained environment, minimizing risk.

### Tools Used

- TCPDump
- Wireshark
- Bash (Shell)

## Steps

![P1](https://github.com/user-attachments/assets/e0a24ac6-f342-4948-a6e6-f1c3045629ce)

Ref 1. Building the shell script for the logging tool and exploring target options.
- -i limits the interface to be captured, in this case, any interface is allowed
- The capture is limited to port 22
- -w writes the captured data to sshcatpure.pcap
- -C & -G set the size and time limits respectively.

![P2 Once the script is executed, the  pcap file becomes visible](https://github.com/user-attachments/assets/44b3f723-a42c-436a-a6e5-e22fbe68033d)

Ref 2. Once the script is executed, the .pcap file becomes visible.
- -x execute right is given to checkspy.sh
- dump file stopped at 3MB and creates a new file

![P4](https://github.com/user-attachments/assets/fa8ad694-01d7-45d5-9efd-7b2e33611d11)

Ref 3. The SSH traffic is easily noticeable on Wireshark. Though the source IP is from our host machine.
- After generating traffic, captured data is opened in Wireshark for readability.

![P5](https://github.com/user-attachments/assets/f9049d2c-ece8-47e0-8c53-0bb37160f7ee)

Ref 4. It is easier to locate packets using display filters.

