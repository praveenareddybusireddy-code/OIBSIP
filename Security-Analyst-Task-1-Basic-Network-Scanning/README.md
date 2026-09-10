Yes 😊 Sorry for the confusion. \*\*I mean you should copy the following complete text and paste it into the blank Notepad window.\*\*



\# Task 1 – Basic Network Scanning with Nmap



\## 1. Objective



The objective of this task is to perform a basic network scan on my own Windows computer using Nmap. The scan is used to identify open ports, running services, service versions, and the operating system.



This task helps in understanding basic network reconnaissance and identifying services that may require security review.



\## 2. Tools Used



\* Nmap 7.991

\* Windows PowerShell

\* Windows 11



\## 3. Target



The target used for this practical was my own Windows computer.



\*\*Target IP Address:\*\* `10.122.1.80`



The scan was performed only on a system under my control.



\## 4. Commands Used



\### Check Nmap installation



```powershell

nmap --version

```



\### Find the local IP address



```powershell

ipconfig

```



\### Basic Nmap scan



```powershell

nmap 10.122.1.80

```



\### Service and version detection



```powershell

nmap -sV 10.122.1.80

```



\### Operating system detection



```powershell

nmap -O 10.122.1.80

```



\### Save service scan results



```powershell

nmap -sV 10.122.1.80 -oN nmap\_scan\_results.txt

```



\### Save OS detection results



```powershell

nmap -O 10.122.1.80 -oN nmap\_os\_results.txt

```



\## 5. Scan Results



The basic scan identified four open TCP ports.



| Port     | State | Service      | Detected Version            |

| -------- | ----- | ------------ | --------------------------- |

| 135/tcp  | Open  | msrpc        | Microsoft Windows RPC       |

| 139/tcp  | Open  | netbios-ssn  | Microsoft Windows NetBIOS   |

| 445/tcp  | Open  | microsoft-ds | SMB-related Windows service |

| 8080/tcp | Open  | http         | Jetty 12.1.8                |



Nmap also identified the operating system as:



\*\*Microsoft Windows 11\*\*



Nmap reported the OS details as:



\*\*Microsoft Windows 11 24H2 – 25H2\*\*



\## 6. Security Analysis



\### Port 135 – MSRPC



Port 135 is associated with Microsoft RPC services. It is commonly used by Windows for communication between applications and services.



\*\*Security consideration:\*\* If unnecessarily exposed to untrusted networks, Windows RPC services can increase the attack surface.



\*\*Recommendation:\*\* Keep Windows updated and use firewall rules to restrict unnecessary access.



\### Port 139 – NetBIOS



Port 139 is associated with NetBIOS over TCP/IP and can be used for Windows network communication and file sharing.



\*\*Security consideration:\*\* NetBIOS is an older networking protocol and may expose information about Windows systems when unnecessarily accessible.



\*\*Recommendation:\*\* Disable NetBIOS where it is not required and restrict access using firewall rules.



\### Port 445 – Microsoft-DS / SMB



Port 445 is commonly associated with SMB file and printer sharing.



\*\*Security consideration:\*\* SMB should not be unnecessarily exposed to untrusted networks.



\*\*Recommendation:\*\* Keep Windows and SMB components updated and restrict SMB access using firewall rules and network segmentation.



\### Port 8080 – HTTP / Jetty



Nmap detected an HTTP service running on port 8080 and identified the server as Jetty 12.1.8.



\*\*Security consideration:\*\* A web service can introduce vulnerabilities depending on its configuration, application, authentication, and software version.



\*\*Recommendation:\*\* Verify whether the service is required, keep the application and Jetty server updated, and restrict access when the service does not need to be publicly accessible.



\## 7. Key Findings



The scan identified four open TCP ports:



\* 135/tcp

\* 139/tcp

\* 445/tcp

\* 8080/tcp



The most important observation is that multiple Windows networking services are listening on the system and a web service is running on port 8080.



An open port does not automatically mean that the system is vulnerable. Further security assessment is required to determine whether a vulnerability actually exists.



\## 8. Conclusion



Nmap was successfully used to perform network reconnaissance on my own Windows computer. The scan identified open ports, services, service versions, and the operating system.



This practical demonstrated how network scanning can help security analysts understand the attack surface of a system and identify services that require further security review.



\## 9. Ethical Considerations



Network scanning must only be performed on systems that are owned by the tester or where explicit authorization has been provided.



For this task, the scan was performed only against my own computer.





