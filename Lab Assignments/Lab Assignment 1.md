# Lab #1: Using Zenmap to Perform Basic Reconnaissance, Performing a Vulnerability Assessment

>[!Note] Disclaimer
> All information in this guide is certified "Works on my Machine:tm:"! Individual expirence may vary.

## Deliverables

> [!WARNING]
> This section is still-in progress! Come back later!

A word doc containing the following:
- (Task 1, 2, 3) A screenshot of VirtualBox showing the installed Virtual Machines
- (Task 5) A screenshot of captured wireshark traffic
- (Task 8) The answers to the questions

<!--TODO-->

## Task 1 & 2: Install and Configure Windows Virtual Machines
### Install and Configure Windows 10 VM

1. Install and launch Oracle VM VirtualBox
1. Download Windows 10 22H2 > [.iso](https://drive.google.com/file/d/1x-0Jm8ADMHwN19fM1y_TBvhAGO-h4o5F/view)
1. On VirtualBox, select "machine>new"
1. Select the iso
1. Set the memory to 4096MG or higher & the processors to 8 or higher and then click next
1. Set the Disk Size to 32GB or higher and then click next > finish
1. Launch the VM and follow the installation instructions

### Install and Configure Windows Server 2022 VM

1. Download Windows Server 2022 (Evaluation edition) > [.iso](https://go.microsoft.com/fwlink/p/?LinkID=2195280&clcid=0x409&culture=en-us&country=US)
1. Launch VirtualBox and create a new machine, selecting the .iso you downloaded and the following values:
    - Skip Unattended Installation: check
    - Base Memory: 4096 MB
    - Processors: 8
    - Disk Size: 32 GB
1. Launch the VM
1. Click next > install now
1. Select "Windows Server 2022 Standard Evaluation (Desktop Expirence)" and then click next
1. Accept the EULA and then click next
1. Select Custom, then click next on the next window
1. Click finish and wait for it to finished installing

## Task 3: Install and Configure Kali Linux 

1. Download Kali Linux 2024.4 > [.iso](https://cdimage.kali.org/kali-2024.4/kali-linux-2024.4-installer-amd64.iso)
1. Launch VirtualBox and create a new machine using the following paramaters: 
    - Base Memory 2048 MB 
    - Processors: 4
    - Virtual Hard Disk Size: 25 GB
1. Click finish
1. **Before launching the VM**, select the VM in VirtualBox and go to Settings>Display>Graphics Controller and select "VBoxVGA" from the drop-down menu
    <!-- S/O to Thomas on the discord for this fix -->
1. Click okay, and then launch the VM
1. Follow the installation instructions, making sure to specify the following information:
    - Hostname: linuxtest
    - Domain: domain.edu
    - Name: user
    - Username: username
    - Partioning Method: 1
    - Partioning Scheme: All files in one partition
    - Installed software: 1 2 5 6 7
    - Device for boot loader installation: /dev/sda

>[!Caution]
> Make sure to double check your spelling. Also write down your username/password.

5. Once the GUI boots, select the top option and enter your username/password

## Task 4: Installing Necessary Software

In this exercise, we will be installed the following software onto both the Windows Server VM and the Kali Linux VM:
- FileZilla
- NetWitness Investigator
- OpenVAS
- PuTTY
- Tftpd64
- Wireshark
- Zenmap

>[!tip]
> If you are on a Windows Machine and are having trouble installing the software onto the Windows VM, try installing it on your local machine instead

### Configuring Kali Linux
1. Launch the Linux VM
1. Open the command line & run the following command to test internet connectivity
    ```bash
    ping 23.215.0.136 -c 4
    ```
1. If you are able to successfully ping the website, run the following block of commands:
    ```bash
    echo "deb http://http.kali.org/kali kali-last-snapshot main contrib non-free non-free-firmware" | sudo tee /etc/apt/sources.list
    sudo apt update
    sudo apt upgrade -y
    sudo apt install filezilla tftpd32 zenmap openvas -y
    ```
1. To configure OpenVas, run the following commands:
    ```bash
    sudo gvm-setup
    sudo gvm-check-setup
    sudo gvmd --user=admin --new-password=passwd;
    ```

### Configuring Windows Server VM

Install the following software onto the VM
- FileZilla > [.exe](https://dl3.cdn.filezilla-project.org/client/FileZilla_3.68.1_win64-setup.exe?h=U61GJtLX4WeCCWKnq-PPdA&x=1740356508)
- NetWitness Investigator > [.msi](https://www2.netwitness.com/l/934283/atorSetup-11-4-2-0-783-x64-msi/chpzq)
- Tftpd32 > [.exe](https://bitbucket.org/phjounin/tftpd64/downloads/Tftpd32-4.64-setup.exe)
- Wireshark > [.exe] (https://2.na.dl.wireshark.org/win64/Wireshark-4.4.4-x64.exe) [PortableApps .exe](https://2.na.dl.wireshark.org/win64/WiresharkPortable64_4.4.4.paf.exe)
- Zenmap > [.exe](https://nmap.org/dist/nmap-7.95-setup.exe)

## Task 5: NetWitness Investigator

> [!WARNING]
> This section is still-in progress! Come back later!

## Task 8: Questions & Answers

Answer the following questions:

1. What is promiscuous mode?
<!-- What your mom does every night, hehe -->
2. How does Wireshark differ from NetWitness Investigator?
3. What is the command line syntax for running an Intense Scan with Zenmap on a target
subnet of 172.30.0.0/24?
4. Name at least five different scans that may be performed with Zenmap.
5. How many different tests (i.e., scripts) did your Intense Scan perform?
6. Based on your interpretation of the Intense Scan, describe the purpose/results of each
tests script performed during the report.
7. How many total IP hosts did Zenmap find on the network?
8. Review the ZeNmap GUI (Nmap) network discovery and vulnerability assessment scan
report and identify the following:
9. What was the date and time stamp of the Nmap host scan?
10. How many total tests or scripts ran during the scan?
11. A SYN stealth scan discovers all open ports on the targeted host. How many ports are open
on the targeted host?
12. What ports are open on the targeted host?
13. What services/applications are on the targeted host?
14. What is the MAC layer address of the targeted host? 
15. What OS is loaded on the targeted host?
16. How many router hops away is the targeted host?
17. Does the ZeNmap GUI (Nmap) scan report provide any information regarding to risk,
threats, or vulnerabilities found?
18. What must you do to confirm or verify if the identified OS, software, application has the
latest release and/or software updates and patches?