# Home_Lab

![image](https://github.com/user-attachments/assets/387b5b62-8e66-4ef0-b4fc-7ec90d9b0b2a)



# Cybersecurity Home Lab

## Project Overview
This repository documents the creation and configuration of a Cybersecurity Home Lab designed for practicing and improving skills in network security, penetration testing, and system hardening. The lab simulates a controlled virtual network environment using multiple virtual machines (VMs) to experiment with network attacks, defenses, and traffic analysis.

---

## Objectives

The main goals of this project are:
- To set up a home lab for cybersecurity learning and practice.
- To simulate network attacks and implement defenses.
- To analyze network traffic using tools like Wireshark.
- To document configurations and create a network diagram for reference.

---

## Features

- Virtual network with multiple VMs (Ubuntu and Kali Linux).
- Network simulation using NAT Networking.
- Tools for cybersecurity analysis installed and configured (e.g., Wireshark, nmap, UFW).
- Documentation of VM configurations and network architecture.

---

## Prerequisites

- Basic knowledge of computer networking.
- A computer with at least 8GB of RAM and sufficient disk space.
- Virtualization software (e.g., VirtualBox or VMware Workstation).

---

## Step-by-Step Implementation

### Step 1: Install Virtualization Software
1. Download and install VirtualBox for your operating system (Windows, macOS, or Linux).
2. Install the VirtualBox Extension Pack for additional functionality.

### Step 2: Create Virtual Machines
1. **Download OS images:**
   - Ubuntu
   - Kali Linux
2. **Create new VMs in VirtualBox:**
   - Allocate 2GB RAM (minimum) for Ubuntu/Kali or 4GB RAM (recommended).
   - Assign at least 20GB virtual disk space per VM.
3. **Install the operating systems:**
   - Follow the installation steps for Ubuntu and Kali Linux.

### Step 3: Set Up Networking
1. Configure VMs to use a NAT Network for isolated communication:
   - Go to `File > Preferences > Network` in VirtualBox.
   - Add a new NAT Network (e.g., `10.0.2.0/24`).
   - Connect VMs to this network via `Settings > Network`.
2. Test connectivity between VMs using ping commands.

### Step 4: Install and Configure Tools
#### Ubuntu VM:
1. **Update the system:**
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```
2. **Install essential tools:**
   ```bash
   sudo apt install -y build-essential git curl wget
   ```
#### Kali Linux VM:
1. **Update the system:**
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```
2. **Install additional tools:**
   ```bash
   sudo apt install -y nmap wireshark metasploit-framework
   ```

### Step 5: Simulate Network Attacks and Defenses
#### Simulate an Attack:
1. Using Kali Linux, perform a basic `nmap` scan on the Ubuntu VM:
   ```bash
   nmap -A 10.0.2.15
   ```
   Replace `10.0.2.15` with the IP address of your Ubuntu VM.
   
   ![Simulating an attack (Using Kali Linux against Ubuntu)](https://github.com/user-attachments/assets/3ed88968-338d-4b80-bbbe-4b140fb022db)

#### Defend Against Attacks:
1. On Ubuntu, install and configure the Uncomplicated Firewall (UFW):
   ```bash
   sudo apt install ufw
   sudo ufw enable
   sudo ufw allow ssh
   sudo ufw allow from 10.0.2.16 # Replace with the IP of Kali VM
   sudo ufw status
   ```
   
   ![Configuring Firewall](https://github.com/user-attachments/assets/98a6643b-7ce8-48d5-8279-236987b053ef)

### Step 6: Analyze Network Traffic
1. Install and launch Wireshark on the Ubuntu VM:
   ```bash
   sudo apt install wireshark
   sudo wireshark
   ```
2. Use Wireshark to capture and analyze network traffic during simulated attacks.
   
   ![Analyzing Network Traffic](https://github.com/user-attachments/assets/9ddf6718-d688-4b26-a3f9-f78761271397)

### Step 7: Document Your Setup
1. **Network Diagram:**
   ![image](https://github.com/user-attachments/assets/387b5b62-8e66-4ef0-b4fc-7ec90d9b0b2a)
2. **Configuration Details:**
   - Document settings for each VM, including:
     - Network configurations (e.g., NAT Network setup).
     - Installed tools and their configurations.
     - Any custom rules (e.g., UFW rules).

---

## Network Diagram

*(Replace this section with your actual diagram)*

---

## Conclusion

This project successfully establishes a home lab environment for cybersecurity practice. The lab can:
- Simulate network attacks and defenses.
- Provide hands-on experience with tools like Wireshark, nmap, and UFW.
- Serve as a foundation for learning advanced cybersecurity concepts.




1. Simulating an attack(Using Kali Linux against Ubuntu)
![image](https://github.com/user-attachments/assets/3ed88968-338d-4b80-bbbe-4b140fb022db)

Configuring Firewall:

![image](https://github.com/user-attachments/assets/98a6643b-7ce8-48d5-8279-236987b053ef)


Analyzing Network Traffic:
![image](https://github.com/user-attachments/assets/9ddf6718-d688-4b26-a3f9-f78761271397)
