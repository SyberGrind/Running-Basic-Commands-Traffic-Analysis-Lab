<img width="1536" height="1024" alt="WhatsApp Image 2026-06-27 at 10 00 57" src="https://github.com/user-attachments/assets/e40e3762-a705-4bed-865c-4a4f1fa09932" />


----
# Running Basic Powershell Commands & Traffic Analysis Lab
This repository documents a comprehensive hands-on lab focused on cloud infrastructure provisioning, Windows systems administration, and network traffic analysis. The project begins with deploying a unified cloud environment in Microsoft Azure, consisting of Windows and Linux virtual machines within a single virtual network. Building on this infrastructure, the lab explores practical network administration using Windows PowerShell commands and culminates in deep-packet analysis using Wireshark, specifically targeting ICMP and SSH protocols to observe network behavior.
>
<br>

----
### 🔹 Phase 1: Resource Group Initialization, Virtual Machine Provisioning (Windows & Linux) & Secure Remote Access,this covers the first 22 Steps.
----
>
<br>
<br>

**Step 1: Navigated to the "Create a resource group" page in Azure to begin the project setup.**
<br>
<img width="1366" height="768" alt="1 Resource Group Creation Portal on Microsoft Azure" src="https://github.com/user-attachments/assets/5af2b732-5b7e-464c-9aa2-d32ced20d4da" />
>
<br>
<br>

**Step 2: Entered the basic project details, including the subscription and the resource group name ("Network-Activities"), to define the project container.**
<br>
<img width="1366" height="768" alt="2 Creating Resource Group Network Activities" src="https://github.com/user-attachments/assets/46ac2d6c-0502-4350-9058-4d8e9a7b4718" />
>
<br>
<br>

**Step 3: Conducted a final review of the configuration details to ensure all parameters were correct before finalizing the creation.**
<br>
<img width="1366" height="768" alt="3 Confirming Creation of Network Activities Resource Group" src="https://github.com/user-attachments/assets/3c2d7584-561a-487a-b243-d45bbe2500fa" />
>
<br>
<br>

**Step 4: Verified that the "Network-Activities" resource group was created successfully and appeared in the manager dashboard.**
<br>
<img width="1366" height="768" alt="4 Network Activities Resource Group Created on Microsoft Azure" src="https://github.com/user-attachments/assets/d55fa153-2737-4855-bfdf-6a29c0aea86c" />
>
<br>
<br>

**Step 5: Navigated to the "Compute infrastructure" dashboard to start the virtual machine deployment process.**
<br>
<img width="1366" height="768" alt="5 Virtual Machine Creation Portal" src="https://github.com/user-attachments/assets/81a4cce6-d1fa-40f1-82ae-0f0624ed066a" />
>
<br>
<br>

**Step 6: Clicked the "Create" button to initialize the setup of a new virtual machine instance.**
<br>
<img width="1366" height="768" alt="6 Creating Windows Virtual Machine on Microsoft Azure" src="https://github.com/user-attachments/assets/b0ae602f-e0de-414b-8925-a6273d3807e3" />
>
<br>
<br>

**Step 7: Opened the VM configuration menu to define the instance settings.**
<br>
<img width="1366" height="768" alt="7 Selecting Resource Group   Region for Windows Virtual Machine" src="https://github.com/user-attachments/assets/616717a7-2bf4-42d2-9649-e7be18f7207e" />
>
<br>
<br>

**Step 8: Configured the basic instance details and assigned the name "WindowsVM" to the Windows-based virtual machine.**
<br>
<img width="1366" height="768" alt="8 Selecting Image   Size for Windows Virtual Machine" src="https://github.com/user-attachments/assets/32e1d901-adce-42f4-bdcd-55b73a2e9968" />
>
<br>
<br>

**Step 9: Configured the basic instance details and assigned the name "LinuxVM" to the Ubuntu-based virtual machine.**
<br>
<img width="1366" height="768" alt="9 Choosing Password   Username for Windows Virtual Machine" src="https://github.com/user-attachments/assets/b21b176c-a867-4ed4-ba4e-377d9ec11138" />
>
<br>
<br>

**Step 10: Selected the "Ubuntu Server 24.04 LTS" image to serve as the Linux endpoint for this network lab.**
<br>
<img width="1366" height="768" alt="10 Password   Username Crafted for Windows Virtual Machine" src="https://github.com/user-attachments/assets/528f7e5c-c323-49e4-8d9f-83f29e315ae7" />
>
<br>
<br>

**Step 11: Returned to the compute infrastructure dashboard to audit the current status of the virtual machines.**
<img width="1366" height="768" alt="11 Windows Virtual Machine Created Confirmation" src="https://github.com/user-attachments/assets/4cd17bf8-c605-4584-9c96-e8b9c0f065f8" />
>
<br>
<br>

**Step 12: Opened the configuration menu specifically for the Linux virtual machine deployment.**
<br>
<img width="1366" height="768" alt="12 Creating Linux-Ubuntu Virtual Machine on Azure" src="https://github.com/user-attachments/assets/4dca549a-f71d-465a-af80-086770a96f05" />
<br>
<br>

**Step 13: Refined the instance details for the Linux virtual machine to ensure consistency with project requirements.**
<br>
<img width="1366" height="768" alt="13 Selecting Resource Group   Region for Linux-Ubuntu Virtual Machine" src="https://github.com/user-attachments/assets/f8581266-867b-4237-842d-0ac46acfd1e6" />
>
<br>
<br>

**Step 14: Validated the OS image selection for the Linux server ("Ubuntu Server 24.04 LTS").**
<br>
<img width="1366" height="768" alt="14 Selecting Image for Linux-Ubuntu Virtual Machine" src="https://github.com/user-attachments/assets/d58542b7-bedb-440d-b8a8-cdc291f3d479" />
>
<br>
<br>

**Step 15: Configured the authentication settings for the Linux VM to prepare for deployment.**
<br>
<img width="1366" height="768" alt="15 Selecting Size for Linux-Ubuntu Virtual Machine" src="https://github.com/user-attachments/assets/cb07090e-1a60-45cc-90c1-396b85a847c8" />
>
<br>
<br>

**Step 16: Reviewed configuration validation errors to ensure all system settings met the Azure deployment requirements.**
<br>
<img width="1366" height="768" alt="16 Choosing Password   Username for Linux-Ubuntu Virtual Machine" src="https://github.com/user-attachments/assets/04c48512-2666-4ffe-8c64-18485f32f4f2" />
>
<br>
<br>

**Step 17: Successfully resolved the validation errors by providing the necessary administrator credentials.**
<br>
<img width="1366" height="768" alt="17 Password   Username Crafted for Linux-Ubuntu Virtual Machine" src="https://github.com/user-attachments/assets/f53982e9-e142-48f3-965b-1820789b824f" />
>
<br>
<br>

**Step 18: Confirmed that both "LinuxVM" and "WindowsVM" were successfully deployed and were marked as "Running" in the infrastructure list.**
<br>
<img width="1366" height="768" alt="18 Linux-Ubuntu Virtual Machine Created on Microsoft Azure" src="https://github.com/user-attachments/assets/80967bc6-92f7-42a3-95fe-715cd48e10e3" />
>
<br>
<br>

**Step 19: Prepared to access the "WindowsVM" remotely using the Windows "Remote Desktop Connection" tool.**
<img width="1366" height="768" alt="19 Opening Remote Desktop on LocalPC" src="https://github.com/user-attachments/assets/76832694-af9a-4bdb-88f7-9fb5187c1eee" />
>
<br>

**Step 20: Entered the Public IP address of the Windows VM & provided the administrator credentials (HNTlab) when prompted by Windows Security to authorize the connection**
<br>
<img width="1366" height="768" alt="20 Inputting WindowsVM IP Address   Username in Remote Desktop" src="https://github.com/user-attachments/assets/042a5687-4675-44c1-b907-4c2c9ac00eaa" />
>
<br>

**Step 21: Inputting Password.**
<br>
 <img width="1366" height="768" alt="21 Inputting Password in Remote Desktop to log in WindowsVM" src="https://github.com/user-attachments/assets/2a6c50ba-1c10-43bf-9ced-09d28f68a276" />
>
<br>
<br>

**Step 22: Successfully logged in, confirming full access to the remote Windows desktop environment.**
<br>
<img width="1366" height="768" alt="22 Successful log in into Windows Virtual Machine" src="https://github.com/user-attachments/assets/02812443-7ed2-4e9f-b775-ae922221f95c" />
>
<br>
<br>

----
## 🔹 Phase 2: Running basic Windows Command Line prompts.
In this 19 steps phase , I utilized the Windows PowerShell environment to perform standard system administration tasks and network diagnostics. I executed core networking commands, including ipconfig, ping, tracert, and netstat, to verify IP configuration, analyze DNS resolution, map network paths, and audit active TCP/UDP connections
----
>
<br>

**Step 23: Accessing the Windows PowerShell environment on the `WindowsVM` to begin system-level administration.**
<br>
<img width="1366" height="768" alt="23 Navigating to Windows Powershell on WindowsVM" src="https://github.com/user-attachments/assets/71709c3c-107b-4921-826e-d818b6767ae9" />
>
<br>
<br>

**Step 24: Verifying that the PowerShell environment has initialized correctly and is ready for administrative input.**
<br>
<img width="1366" height="768" alt="24 Successful openning of Windows Powershell on WindowsVM" src="https://github.com/user-attachments/assets/3ff6e7e8-e880-405a-9fc4-f380cc353acb" />
>
<br>
<br>

**Step 25: Executing the `ipconfig` command to retrieve the current IPv4 address, subnet mask, and default gateway settings for the virtual machine.**
<br>
<img width="1366" height="768" alt="25 Prompting ipconfig command on Windows Powershell in WindowsVM" src="https://github.com/user-attachments/assets/c9035730-4c07-47b1-96bb-946ced90bf42" />
>
<br>
<br>

**Step 26: Reviewing the network configuration report to confirm the virtual machine has a valid IP assignment.**
<br>
<img width="1366" height="768" alt="26  Successful ipconfig command   Checking Report-Powershell WindowsVM" src="https://github.com/user-attachments/assets/0b6922a8-9c5e-48a2-aaee-f86d274f5628" />
>
<br>
<br>

**Step 27: Executing `ipconfig /all` to access comprehensive network configuration, including DNS, DHCP, and physical (MAC) address details.**
<br>
<img width="1366" height="768" alt="27 Prompting ipconfig all command on Windows Powershell in WindowsVM" src="https://github.com/user-attachments/assets/ea03dbcc-6a17-4186-9439-0d4b094f733d" />
>
<br>
<br>

**Step 28: Reviewing the detailed PowerShell report to confirm network adapter status and DNS server configuration.**
<br>
<img width="1366" height="768" alt="28 Successful ipconfig all command   Checking Report-Powershell WindowsVM" src="https://github.com/user-attachments/assets/af18c7ee-4239-44c3-9abf-be86dee4dded" />
>
<br>
<br>

**Step 29: Executing a `ping` command targeting Google’s public IP address to test end-to-end network reachability and latency.**
<br>
<img width="1366" height="768" alt="29 Prompting ping command on Windows Powershell in WindowsVM - pinging using Google IP Address" src="https://github.com/user-attachments/assets/c55b5f89-6ee3-4b85-8eb9-05eafff76940" />
>
<br>
<br>

**Step 30: Confirming successful ICMP echo requests and replies, indicating active connectivity to the destination IP.**
<br>
<img width="1366" height="768" alt="30 Succssful ping command on Windows Powershell in WindowsVM of Google" src="https://github.com/user-attachments/assets/717f509c-db25-4829-8b8a-b39137cf23f7" />
>
<br>
<br>

**Step 31: Executing `ping` using a domain name (`google.com`) to verify that the system can resolve hostnames to IP addresses.**
<br>
<img width="1366" height="768" alt="31 Prompting to ping Google by name on Windows Powershell in WindowsVM" src="https://github.com/user-attachments/assets/d93fea12-e04f-45bf-bf35-ec2021eb2486" />
>
<br>
<br>

**Step 32: Confirming the system successfully resolved the hostname and established connectivity via ICMP.**
<br>
<img width="1366" height="768" alt="32 Successful ping of Google by name on Windows Powershell in WindowsVM" src="https://github.com/user-attachments/assets/99ee9285-b92a-4830-8b32-b383816a5fa6" />
>
<br>
<br>

**Step 33: Executing the `hostname` command to identify the unique system name assigned to the virtual machine.**
<br>
<img width="1366" height="768" alt="33 Prompting hostname command on Windows Powershell in WindowsVM" src="https://github.com/user-attachments/assets/5b0359bf-71cd-4352-bfdb-72aafaa595d9" />
>
<br>
<br>

**Step 34: Verifying the system identity within the PowerShell console.**
<br>
<img width="1366" height="768" alt="34 Hostname confirmation Windows Powershell on WindowsVM" src="https://github.com/user-attachments/assets/af0fdac5-c066-46a7-b7cc-68293e7960f4" />
>
<br>
<br>

**Step 35: Executing `tracert` to map the network path and hop count from the `WindowsVM` to Google.com.**
<br>
<img width="1366" height="768" alt="35 Prompting tracert command for google on Windows Powershell in WindowsVM" src="https://github.com/user-attachments/assets/f1c6df89-ba5e-4d05-9103-7f92ac42c736" />
>
<br>
<br>

**Step 36: Reviewing the `tracert` hops result to confirm the path taken through the network to the destination.**
<br>
<img width="1366" height="768" alt="36 Successful Google hops check using tracert command on Windows Powershell in WindowsVM" src="https://github.com/user-attachments/assets/1557a8ad-abe1-480c-8328-c1947f622fa3" />
>
<br>
<br>

**Step 37: Executing `nslookup` for the FIFA website to verify DNS resolution for a specific external domain.**
<br>
<img width="1366" height="768" alt="37 Prompting nslookup command of FIFA website on Windows Powershell on WindowsVM" src="https://github.com/user-attachments/assets/6160658d-9f23-4806-b60d-f352d5bca835" />
>
<br>
<br>

**Step 38: Reviewing the DNS query results to confirm the system correctly retrieved the IP address for the target domain.**
<br>
<img width="1366" height="768" alt="38 Successful nslookup command of FIFA - Windows Powershell on WindowsVM" src="https://github.com/user-attachments/assets/247e55fc-cd51-4b6f-a6ec-2296cc8689a3" />
>
<br>
<br>

**Step 39: Executing `netstat` to view active TCP/UDP connections and listening ports on the virtual machine.**
<br>
<img width="1366" height="768" alt="39 Prompting netstat command on Windows Powershell in WindowsVM" src="https://github.com/user-attachments/assets/c2928063-24e4-43b1-b6d6-f10082bfcfbb" />
>
<br>
<br>

**Step 40: Analyzing the active connection table to identify current network traffic.**
<br>
<img width="1366" height="768" alt="40 Successful netstat command   Results on Windows Powershell in WindowsVM" src="https://github.com/user-attachments/assets/16ea9ada-5c74-42d1-9cb9-76ca5e748cdc" />
>
<br>
<br>

**Step 41: Executing `netstat -ano` to display active connections with the associated Process ID (PID) for further system analysis.**
<br>
<img width="1366" height="768" alt="41 Successful Prompting netstat -ano command on Windows Powershell in WindowsVM" src="https://github.com/user-attachments/assets/220c1498-c034-408f-8684-344f9294d386" />
>
<br>
<br>

----
## 🔹 Phase 3: Network Traffic Analysis (Wireshark, ICMP, & SSH)
In this phase which consits of 30 steps, I performed end-to-end packet analysis to monitor network connectivity, implemented firewall security measures to block specific traffic, and established secure remote access to the Linux environment.
----
>
<br>
<br>

**Step 42: Searching for Wireshark on Microsoft Edge**
Utilizing Microsoft Edge to locate and download the Wireshark distribution for network protocol analysis.
<img width="1366" height="768" alt="42 Searching for Wireshark on Microsoft Edge on WindowsVM" src="https://github.com/user-attachments/assets/60c261a5-1c2e-4392-b09b-ceb02aa7617c" />
>
<br>
<br>

**Step 43: Initiating the download of the Wireshark installer to prepare the virtual environment for packet capture and inspection.**
<br>
<img width="1366" height="768" alt="43 Download of Wireshark on WindowsVM" src="https://github.com/user-attachments/assets/53ab0152-2db1-4a5f-bea0-cbe793b106a1" />
>
<br>
<br>

**Step 44: Configuring the Wireshark setup wizard on the WindowsVM, ensuring all necessary components are selected for installation.**
<br>
<img width="1366" height="768" alt="44 Setting Up Wireshark on WindowsVM" src="https://github.com/user-attachments/assets/824a7536-da48-424e-8c5d-ff414cb48510" />
>
<br>

**Step 45: Completing the installation process for Wireshark to enable deep-packet inspection capabilities.**
<br>
<img width="1366" height="768" alt="45 Installing Wireshark on WindowsVM" src="https://github.com/user-attachments/assets/652e95bb-2f71-4610-b75b-24b9eaf5f998" />
>
<br>
<br>

**Step 46: Launching the Wireshark application and verifying the primary network interface is initialized for monitoring.**
<br>
<img width="1366" height="768" alt="46 Openning Wireshark on WindowsVM" src="https://github.com/user-attachments/assets/7ffd8da7-b68a-4ffd-9a65-6df4439bab2e" />
>
<br>
<br>

**Step 47: Selecting the primary Ethernet network adapter to capture and inspect all raw traffic traversing the WindowsVM.**
<br>
<img width="1366" height="768" alt="47 Selecting Ethernet for packet capture on Wireshark - WindowsVM" src="https://github.com/user-attachments/assets/17df5efc-3ab7-4aa8-bb28-f5bb07c12475" />
>
<br>
<br>

**Step 48: Reviewing live network traffic, identifying background broadcasts and standard system protocols active on the virtual network.**
<br>
<img width="1366" height="768" alt="48 General Network packets   traffic inspection on Wireshark - WindowsVM" src="https://github.com/user-attachments/assets/7b5349b6-e8f1-46b2-a571-5a8c5a3c655c" />
>
<br>

**Step 49: Applying an `icmp` display filter in Wireshark to isolate Echo Request and Echo Reply packets for connectivity verification.**
<br>
<img width="1366" height="768" alt="49 Prompting to filter for ICMP traffic on Wireshark - WindowsVM" src="https://github.com/user-attachments/assets/a94bf28a-b859-4c76-95f9-20a1c3a1886a" />
>
<br>
<br>

**Step 50: Clearing the Wireshark capture buffer to focus exclusively on the specific ICMP traffic patterns.**
<br>
<img width="1366" height="768" alt="50 Cleared traffic on Wireshark for ICMP results - WindowsVM" src="https://github.com/user-attachments/assets/13069214-7ac3-479e-8bc2-dd0114c40197" />
>
<br>
<br>

**Step 51: Accessing the Windows PowerShell terminal on WindowsVM to prepare for traffic flitering - active connectivity testing.**
<img width="1366" height="768" alt="51 Openning Windows Powershell on WindowsVM for ICMP traffic filter" src="https://github.com/user-attachments/assets/6d15ae21-fad8-4074-ab7c-e32c63b4aa60" />
>
<br>
<br>

**Step 52: Arranging the workspace with PowerShell and Wireshark side-by-side to correlate command execution with live network packet capture.**
<br>
<img width="1366" height="768" alt="52 Powershell   Wireshark open on WindowsVm for ICMP traffic filter" src="https://github.com/user-attachments/assets/18af44ea-809f-4309-814f-f164ff5a8951" />
>
<br>
<br>

**Step 53: Identifying the Linux-UbuntuVM private IP address (10.0.0.5) to serve as the destination target for connectivity testing.**
<br>
<img width="1366" height="768" alt="53 Obtaining Linux-UbuntuVM Private IP Address for ICMP traffic filter - WindowsVM" src="https://github.com/user-attachments/assets/d39e82fb-9692-447d-bb07-89a8d33c7f81" />
>
<br>
<br>

**Step 54: Executing the `ping` command to initiate network communication with the remote Linux instance.**
<br>
<img width="1366" height="768" alt="54 Promtp to ping Linux-UbuntuVM for ICMP traffic filter - WindowsVM" src="https://github.com/user-attachments/assets/0b4693fd-b713-4344-b737-fe896d5c1916" />
>
<br>
<br>

**Step 55: Inspecting captured ICMP packets in Wireshark to verify successful packet transmission and round-trip response.**
<br>
<img width="1366" height="768" alt="55 Analysing ICMP traffic on Powershell   Wireshark - WindowsVM" src="https://github.com/user-attachments/assets/bf1caf95-3678-4655-859b-8f45ae30eaa3" />
>
<br>
<br>

**Step 56: Executing `ping 10.0.0.5 -t` perpetual ping to create a continuous, nonstop stream of ICMP traffic for sustained observation in Wireshark.**
<br>
<img width="1366" height="768" alt="56 Prompt of perpetual nonstop ping of Linux-UbuntuVM for ICMP traffic filter Powershell   Wireshark - WindowsVM" src="https://github.com/user-attachments/assets/96dc8830-1ac5-44cc-b975-2c8db07a5c27" />
>
<br>
<br>

**Step 57: Confirming the continuous connectivity stream is active and being logged in the Wireshark packet capture.**
<br>
<img width="1366" height="768" alt="57 Successful prompt of perpetual nonstop ping of Linux-UbuntuVM for ICMP traffic filter Powershell   Wireshark - WindowsVM" src="https://github.com/user-attachments/assets/9e530f1f-41d0-4179-88ee-554f094d1b94" />
>
<br>

**Step 58: Navigating to the Network Security Group settings to define inbound firewall rules for the Linux-UbuntuVM.**
<br>
<img width="1366" height="768" alt="58 Creating port for Linux-UbuntuVM" src="https://github.com/user-attachments/assets/9f206365-bf17-4abb-a5a2-e49377a9e2fb" />
>
<br>
<br>

**Step 59: Modifying the inbound security rule to explicitly "Deny" ICMP traffic, testing the firewall's ability to block the perpetual ping stream.**
<br>
<img width="1366" height="768" alt="59 Changing of Inbound Security Rules to block perptual nonstop ping of Linux-UbuntuVM" src="https://github.com/user-attachments/assets/d8c3e20a-3d3e-4c79-9799-919291eacf48" />
>
<br>
<br>

**Step 60: Verifying the updated network security (Inbound Security Rule) configuration is saved and effectively applied to the Linux-UbuntuVM.**
<br>
<img width="1366" height="768" alt="60 Successful Change of Inbound Security Rules to block perptual nonstop ping of Linux-UbuntuVM" src="https://github.com/user-attachments/assets/15cfa7bf-c10a-46b8-bae3-8253cae36567" />
>
<br>
<br>

**Step 61: Correlating the PowerShell "Request Timed Out" errors with the block of ICMP packets captured in Wireshark.**
<br>
<img width="1366" height="768" alt="61 Analysing block of perptual nonstop ping of Linux-UbuntuVM on Powershell   Wireshark - WindowsVM" src="https://github.com/user-attachments/assets/66451c51-8174-4e7e-b2ba-a02455fc9d43" />
>
<br>
<br>

**Step 62: Deep-diving into Wireshark logs to confirm that ICMP traffic is successfully dropped by the configured firewall rule.**
<img width="1366" height="768" alt="62 Analysing block of perptual nonstop ping of Linux-UbuntuVM on Wireshark - WindowsVM" src="https://github.com/user-attachments/assets/e23a2234-9570-4a19-8662-e839103505da" />
>
<br>
<br>

**Step 63: Preparing the SSH command structure (`ssh [user]@[ip]`) to initiate a secure management session.**
<br>
<img width="1366" height="768" alt="63 Prompt of shh traffic on Wireshark on WindowsVM" src="https://github.com/user-attachments/assets/f72bfc86-fb16-4604-b9eb-b5960d0b4fab" />
>
<br>
<br>

**Step 64: Configuring the environment to capture the SSH handshake and encryption negotiation phases in Wireshark.**
<br>
<img width="1366" height="768" alt="64 Prompt of shh traffic on Powershell   Wireshark on WindowsVM" src="https://github.com/user-attachments/assets/b5c5dc0a-baaf-470d-bac9-d3fd9e11e9d8" />
>
<br>
<br>

**Step 65: Executing the `ssh` command in PowerShell to attempt a remote authenticated login to the Linux-UbuntuVM.**
<br>
<img width="1366" height="768" alt="65 Prompt to log in Linux-UbuntuVM using Powershell via ssh on WindowsVM" src="https://github.com/user-attachments/assets/61c3e4f7-6bfe-43ee-8daa-ab819b59bd2c" />
>
<br>
<br>

**Step 66: Inspecting the captured SSH packets to identify the TCP handshake and secure protocol negotiation.**
<br>
<img width="1366" height="768" alt="66 Analysing ssh traffic on Wireshark Linux-UbuntuVM on Powershell using ssh - WindowsVM" src="https://github.com/user-attachments/assets/8d9d220c-59f2-4092-ae8c-2670af8684f6" />
>
<br>
<br>

**Step 67: Verifying the authentication handshake packets as the secure SSH session is established.**
<br>
<img width="1366" height="768" alt="67 Analysing ssh traffic on Wireshark   confirming to log in Linux-UbuntuVM on Powershell using ssh - WindowsVM" src="https://github.com/user-attachments/assets/31e30ffd-d3db-47b5-b76d-ab84b882f958" />
>
<br>
<br>

**Step 68: Confirming the authenticated session is established and the remote command prompt is active to log in to Linux VM.**
<br>
<img width="1366" height="768" alt="68 Successfull log in Linux-UbuntuVM on Powershell using ssh - WindowsVM" src="https://github.com/user-attachments/assets/6c7d6f00-105c-4428-b20b-7ab19d640bb8" />
>
<br>
<br>

**Step 69: Validating that the remote connection is stable and authenticated for command execution on Linux VM.**
<br.
<img width="1366" height="768" alt="69 Login confirmed of Linux-UbuntuVM on Powershell - WindowsVM" src="https://github.com/user-attachments/assets/71d706d0-57ea-4eb6-91ef-e0df385f4c26" />
>
<br>
<br>

**Step 70: Executing the `hostname` command on the remote Linux-UbuntuVM to verify i am utilizing my LInux VM.**
<br>
<img width="1366" height="768" alt="70 Prompting hostname command on Linux-UbuntuVM using powershell - WindowsVM" src="https://github.com/user-attachments/assets/5dbdbd91-ab7e-409d-bbba-a5ad7d0f9bb7" />
>
<br>
<br>

**Step 71: Receiving the correct hostname from the remote system, demonstrating full remote management via SSH.**
<br>
<img width="1366" height="768" alt="71 Successful hostname promtp Linux-UbuntuVM - WindowsVM" src="https://github.com/user-attachments/assets/dd1ca81e-1e33-4dd0-a0ea-4aa70238da72" />
>
<br>
<br>

----
## 🔹 Phase 4: Lab Conclusion & Resource Cleanup
This final phase concludes the project by securely terminating the active SSH session and decommissioning all provisioned Azure virtual machines to ensure efficient resource management and environmental cleanup in 3 steps.
----
>
<br>

**Step 72: Concluding the secure SSH session and closing the terminal to return to the local WindowsVM environment.**
<br>
<img width="1366" height="768" alt="72 Existing Linux-UbuntuVM using Powershell on WindowsVM" src="https://github.com/user-attachments/assets/b7aaf5d5-2ebf-4dad-abdb-6defc4b9644f" />
>
<br>
<br>

**Step 73: Navigating to the Azure resource dashboard to initiate the deletion of the Windows and Linux virtual machine instances.**
<br>
<img width="1366" height="768" alt="73 Deleting Virtual Machines Linux   Windows on Azure" src="https://github.com/user-attachments/assets/b84a17bf-db6a-4c34-8acc-c91607a24743" />
>
<br>
<br>

**Step 74: Confirming the successful removal of all provisioned cloud resources to maintain a clean environment and prevent unnecessary costs.**
<br>
<img width="1366" height="768" alt="74 Succesful Deletion of Virtual Machines Linux   Windows on Azure" src="https://github.com/user-attachments/assets/b5e29c8c-1323-4e5b-a885-5f58866f20b7" />
>
<br>
<br>

----
# 🏁Conclusion 
This project successfully demonstrated an end-to-end cloud computing workflow, starting with the provisioning of a virtualized infrastructure in Microsoft Azure and advancing to hands-on systems administration and network traffic analysis. By deploying both Windows and Linux virtual machines within a unified virtual network, I gained practical experience in remote access protocols, Windows command-line diagnostics, and deep-packet inspection using Wireshark to observe ICMP and SSH behavior. The lab concluded with a structured teardown of all cloud resources, reinforcing the critical importance of resource lifecycle management and cost efficiency in professional cloud infrastructure administration.
