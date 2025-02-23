# Lab #1: Using Zenmap to Perform Basic Reconnaissance, Performing a Vulnerability Assessment
## Deliverables

> [!WARNING]
> This section is still-in progress! Come back later!

<!--TODO-->

## Task 1 & 2: Install and Configure Windows Virtual Machines
### Install and Configure Windows 10 VM

1. Install and launch Oracle VM VirtualBox
1. Download Windows 10 22H2 > [.iso](https://drive.google.com/file/d/1x-0Jm8ADMHwN19fM1y_TBvhAGO-h4o5F/view)
1. On VirtualBox, select "machine>new"
1. Select the iso
1. Set the memory to 4096 mb or higher & the processors to 8 or higher and then click next
1. Set the Disk Size to 32GB or higher and then click next > finish
1. Launch the VM
1. Click next > install now
1. Select "Windows Server 2022 Standard Evaluation (Desktop Expirence)" and then click next
1. Accept the EULA and then click next
1. Select Custom, then click next on the next window
1. Click finish and wait for it to finished installing

### Install and Configure Windows Server 2022 VM

1. Download Windows Server 2022 (Evaluation edition) > [.iso](https://go.microsoft.com/fwlink/p/?LinkID=2195280&clcid=0x409&culture=en-us&country=US)
1. Launch VirtualBox and create a new machine, selecting the .iso you downloaded
1. Check "skip unattended installation" and then click next
1. Set the memory to 4096 mb or higher & the processors to 8 or higher and then click next
1. Set the Disk Size to 32GB or higher and then click next > finish
1. Launch the VM
1. Click next > install now
1. Select "Windows Server 2022 Standard Evaluation (Desktop Expirence)" and then click next
1. Accept the EULA and then click next
1. Select Custom, then click next on the next window
1. Click finish and wait for it to finished installing



## Task 6.5: Questions & Answers

Answer the following questions:

1. What is promiscuous mode?
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