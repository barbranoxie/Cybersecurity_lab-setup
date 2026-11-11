# CYBERSECURITY LAB SETUP DOCUMENTATION

**Project:** Cybersecurity Virtual Lab Environment  
**Platform:** Oracle VirtualBox  
**Operating System:** Kali Linux  
**Network Configuration:** NAT Network  
**Network Subnet:** 10.0.0.0/24

## 1. Introduction

This documentation explains the process of setting up a cybersecurity laboratory using Oracle VirtualBox. The purpose of the lab is to create a controlled virtual environment where cybersecurity practical exercises, vulnerability assessments, network testing and security investigations can be performed safely.

The laboratory uses Kali Linux as the attacking machine. VirtualBox provides the virtualisation platform, allowing the virtual machine to operate independently from the host computer.

Attached is the picture of Kali linux Natnetwork setup
<img src= "network1.PNG" width="300">
## 2. Lab Requirements

The following software and resources were required:

| Component | Description |
|---|---|
| Host computer | Laptop |
| Virtualisation software | Oracle VirtualBox |
| Operating system | Kali Linux |
| Network type | NAT Network |
| Network subnet | 10.0.0.0/24 |
| Attacking machine | Kali Linux VM |
| Internet connection | NAT Network |

## 3. Installation and Configuration

### 3.1 Install Oracle VirtualBox

Oracle VirtualBox was installed on the laptop to provide a platform for creating and managing virtual machines.

The installation process involved:
1. Downloading VirtualBox from the official website.
2. Running the installation file.
3. Following the installation instructions.
4. Opening VirtualBox after installation.
5. Confirming that the software was working correctly.

Official website: https://www.virtualbox.org/

### 3.2 Download and Import Kali Linux

Kali Linux was downloaded from its official website.

The following steps were followed:
1. Open the official Kali Linux website.
2. Download the pre-built VirtualBox virtual machine image.
3. Open Oracle VirtualBox.
4. Import the downloaded virtual machine.
5. Review the virtual machine settings.
6. Start the Kali Linux virtual machine.
7. Confirm that Kali Linux starts successfully.

Official website: https://www.kali.org/

### 3.3 Configure the NAT Network

A NAT Network was created in VirtualBox to allow the virtual machine to communicate with the internet.

The following configuration was applied:

| Setting | Configuration |
|---|---|
| Network name | NATNetwork |
| Network mode | NAT Network |
| IPv4 subnet | 10.0.0.0/24 |
| Gateway | 10.0.0.1 |
| Kali Linux IP | 10.0.0.2 |
| DNS server | 8.8.8.8 |

The Kali Linux virtual machine was connected to the NAT Network.

The network adapter settings were configured as follows:
1. Open VirtualBox.
2. Select the Kali Linux virtual machine.
3. Open Settings.
4. Select Network.
5. Enable the network adapter.
6. Select NAT Network as the attachment type.
7. Choose NATNetwork.
8. Enable the cable connected option.
9. Save the settings.

Promiscuous Mode was also configured to Allow All.

### 3.4 Configure Kali Linux Network Settings

After connecting Kali Linux to the NAT Network, the network configuration was checked.

The following network settings were used:

| Network setting | Value |
|---|---|
| Interface | Wired Connection 1 |
| IPv4 address | 10.0.0.2 |
| Subnet mask | 255.255.255.0 |
| Default gateway | 10.0.0.1 |
| DNS | 8.8.8.8 |

The network connection was tested to confirm that Kali Linux could communicate with the gateway and access the internet.

### 3.5 Configure Shared Folders

A shared folder was configured to allow files to be transferred between the host computer and Kali Linux.

The host computer's Downloads folder was selected as the shared folder.

The configuration allowed Kali Linux to access files stored on the host computer.

### 3.6 Enable Clipboard and Drag-and-Drop

For easier communication between the host computer and the virtual machine, the following VirtualBox features were enabled:

- Shared Clipboard: Bidirectional.
- Drag and Drop: Bidirectional.

These settings made it easier to copy text and transfer files between the two environments.

## 4. Network Connectivity Testing

After completing the configuration, connectivity tests were performed to confirm that the virtual machine was connected correctly.

The following commands were executed in the Kali Linux terminal.

**Test 1: Check IP address**

```bash
ip addr
```

This command displays the network interfaces and assigned IP addresses.

**Test 2: Check default gateway**

```bash
ip route
```

This command displays the routing information and default gateway.

**Test 3: Test gateway connectivity**

```bash
ping -c 4 10.0.0.1
```

This test checks communication between Kali Linux and the NAT Network gateway.

**Test 4: Test internet connectivity**

```bash
ping -c 4 8.8.8.8
```

This test checks whether Kali Linux can reach an external IP address.

**Test 5: Test DNS connectivity**

```bash
ping -c 4 google.com
```

This test checks whether DNS name resolution is working.

The connectivity tests confirmed that the virtual machine could communicate with its gateway and access the internet.

## 5. Create a Virtual Machine Snapshot

After completing the installation and configuration, a snapshot was created.

The snapshot provides a recovery point that can be used to restore the virtual machine to its working condition if configuration problems occur during future practical exercises.

## 6. Cybersecurity Tools and Future Practical Activities

Kali Linux provides a platform for cybersecurity practical activities.

The laboratory can be used for authorised exercises involving:

- Network scanning and discovery.
- Vulnerability assessment.
- Network traffic analysis.
- Password security testing.
- Security monitoring.
- Basic penetration testing.
- Linux security administration.

All testing should be conducted on systems that are owned by the student or where explicit permission has been granted.

## 7. Conclusion

The cybersecurity laboratory was successfully configured using Oracle VirtualBox and Kali Linux. A NAT Network with the subnet 10.0.0.0/24 was created, and the Kali Linux virtual machine was assigned the IP address 10.0.0.2. Shared folders, bidirectional clipboard and drag-and-drop were also configured to improve communication between the host computer and the virtual machine.

Connectivity testing confirmed that the virtual machine could communicate with the gateway and access the internet. Finally, a snapshot was created to preserve the working configuration. This laboratory provides a foundation for performing cybersecurity practical exercises in a controlled virtual environment.

## 8. References

1. Oracle. (n.d.). *Oracle VM VirtualBox*. https://www.virtualbox.org/
2. Kali Linux. (n.d.). *Kali Linux Documentation*. https://www.kali.org/docs/
3. Kali Linux. (n.d.). *Kali Linux Downloads*. https://www.kali.org/get-kali/
