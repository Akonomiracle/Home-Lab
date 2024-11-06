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

- VirtualBox
- ISO Images for Operating Systems
- Network Utilities

## Steps

Step 1: Installing VirtualBox & Virtual Machines

1. Begin by downloading and installing VirtualBox on your host computer, along with virtual machine (VM) ISO image files for your desired operating systems (e.g., Windows, Kali Linux).
    - Ensure that the ISO files are compatible with VirtualBox to prevent installation issues.
2. Load the ISO images into VirtualBox to initialize the VMs.

Ref 1. (Image showcasing the VirtualBox and VM installation setup).



Step 2: Configuring Virtual Machines (VMs)

1. Set Up Networking: Configure each VM's network settings to manage connectivity, essential for tasks such as malware analysis or network scanning, ensuring these operations do not impact the host machine.
    - Key Network Options in VirtualBox:
        - NAT: Grants VM internet access via the host's network.
        - Bridge Adapter: Connects VMs to the same network as the host, where each VM acts as an independent device.
        - Internal Network: Connects VMs only to each other, isolating them from the host and the internet. Ideal for malware testing and secure communication between VMs.
        - Host-Only Network: Creates a private network between VMs and the host, with no internet access.
        - NAT Network: Similar to NAT, but allows multiple VMs on the same network with internet access.
        - Cloud Network: Connects VMs to the cloud.
        - Not Attached: Disconnects VMs from any network.
2. Preferred Network Configuration: Using the Internal Network is recommended to isolate the VMs from the host and internet, allowing safe internal communication for testing purposes.

Ref 2. (Image detailing network configurations).


Step 3: Assigning IP Addresses to the VMs

1. Windows VM: Assign a static IP address to ensure consistent connectivity during testing.
    - Verify the IP assignment using ipconfig in Command Prompt to confirm accurate network settings.
2. Kali Linux VM: Similarly, assign and check the IP address using ifconfig.
    - Document the IP configurations to maintain consistency and avoid conflicts.

Ref 3. (Image showing IP assignment for Windows).
Ref 4. (Image showing IP assignment for Kali Linux).

