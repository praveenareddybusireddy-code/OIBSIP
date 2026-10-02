# Common Network Security Threats



## Introduction



Network security threats are malicious activities that attempt to disrupt, damage, access, or misuse computer networks and the systems connected to them. As organizations increasingly depend on networks for communication, cloud services, online transactions, and data storage, network attacks can affect confidentiality, integrity, and availability. Common threats such as DoS/DDoS attacks, Man-in-the-Middle attacks, IP spoofing, and DNS poisoning can lead to service disruption, unauthorized access, data theft, or users being redirected to malicious destinations. Understanding how these attacks work and applying appropriate security controls are essential for protecting organizational networks and maintaining reliable services.



---



## 1. DoS/DDoS Attacks



### What is a DoS/DDoS Attack?



A Denial-of-Service (DoS) attack attempts to make a system, server, or network service unavailable to legitimate users by overwhelming it with requests or consuming its available resources.



A Distributed Denial-of-Service (DDoS) attack uses multiple compromised devices, often called a botnet, to send large volumes of traffic or requests toward the target.



### How It Works



1. The attacker identifies a target service or server.

2. In a DoS attack, the attacker sends excessive traffic or requests.

3. In a DDoS attack, many compromised devices send traffic simultaneously.

4. The target consumes its bandwidth, processing power, memory, or other resources.

5. Legitimate users experience slow service or complete service unavailability.



### Impact



- Website or application downtime

- Loss of availability

- Reduced business productivity

- Financial losses

- Damage to customer trust

- Increased recovery costs



### Real-World Example



In 2016, the Mirai botnet was used in large-scale DDoS attacks. The malware compromised vulnerable Internet of Things (IoT) devices and used them as a botnet to generate large amounts of traffic. One major attack targeted Dyn, a DNS infrastructure provider, and caused availability problems for several major Internet services.



### Mitigation Strategies



1. **Traffic filtering:** Use firewalls and filtering systems to block malicious or abnormal traffic.

2. **Rate limiting:** Limit the number of requests that a client can send within a given period.

3. **DDoS protection services:** Use specialized DDoS mitigation and traffic-scrubbing services.



---



## 2. Man-in-the-Middle (MITM) Attacks



### What is a MITM Attack?



A Man-in-the-Middle attack occurs when an attacker secretly positions themselves between two communicating parties and intercepts or potentially modifies their communication.



### How It Works



1. Two parties establish communication.

2. The attacker positions themselves between the parties.

3. The attacker intercepts network traffic.

4. The attacker may read, capture, or modify information.

5. The communication may continue while the victims are unaware of the interception.



### Impact



- Theft of sensitive information

- Exposure of login credentials

- Session hijacking

- Modification of transmitted information

- Privacy violations



### Real-World Example



A documented type of MITM attack involves attackers creating malicious or compromised Wi-Fi access points in public locations. Users who connect to an attacker-controlled network may have their unencrypted or improperly protected traffic intercepted.



### Mitigation Strategies



1. **Use HTTPS/TLS:** Encrypt communication between clients and servers.

2. **Use secure Wi-Fi:** Avoid untrusted wireless networks and use properly secured networks.

3. **Certificate validation:** Ensure that systems correctly validate digital certificates and do not ignore certificate warnings.



---



## 3. IP Spoofing



### What is IP Spoofing?



IP spoofing is a technique in which an attacker creates network packets with a forged source IP address. The receiving system may therefore see a source address that does not represent the actual origin of the traffic.



### How It Works



1. The attacker creates a network packet.

2. The attacker changes the source IP address in the packet.

3. The packet is transmitted toward the target.

4. The target receives the packet and sees the forged source address.



### Impact



- Bypass of weak IP-based access controls

- Reflection and amplification attacks

- Difficulty identifying the true source of malicious traffic

- Network abuse



### Real-World Example



IP spoofing has been widely used in reflection and amplification DDoS attacks. In these attacks, an attacker sends requests to third-party servers while forging the victim's IP address as the source. The third-party servers then send their responses to the victim, increasing the amount of unwanted traffic received by the victim.



### Mitigation Strategies



1. **Ingress and egress filtering:** Filter packets whose source addresses are invalid for the network from which they arrive.

2. **Network monitoring:** Monitor unusual traffic patterns and suspicious source addresses.

3. **Strong authentication:** Do not rely only on source IP addresses for authentication or authorization.



---



## 4. DNS Poisoning/Spoofing



### What is DNS Poisoning?



DNS poisoning, also called DNS cache poisoning, is an attack in which false DNS information is introduced into a DNS resolver's cache. This can cause users to be directed to an incorrect or malicious IP address when they request a legitimate domain.



### How It Works



1. A user requests a domain name.

2. A DNS resolver processes the request.

3. The attacker causes false DNS information to be stored or returned.

4. The resolver provides the incorrect IP address.

5. The user may be redirected to a malicious or fraudulent destination.



### Impact



- Users can be redirected to fake websites.

- Login credentials may be stolen.

- Malware may be distributed.

- Users may be exposed to phishing attacks.

- Trust in legitimate services can be affected.



### Real-World Example



In 2008, security researcher Dan Kaminsky disclosed a serious DNS cache-poisoning vulnerability affecting DNS servers. The vulnerability could allow attackers to insert fraudulent DNS records into caches and redirect users to incorrect destinations. DNS software vendors released patches and organizations were advised to update their DNS systems.



### Mitigation Strategies



1. **DNSSEC:** Use DNS Security Extensions to provide authentication and integrity for DNS responses.

2. **Secure DNS infrastructure:** Keep DNS software updated and properly configured.

3. **Monitoring:** Monitor DNS records and investigate unexpected changes or suspicious DNS responses.



---



## 5. Comparison Table



| Threat | Attack Vector | Who Is at Risk? | Difficulty to Execute | Ease of Mitigation |

|---|---|---|---|---|

| DoS/DDoS | Excessive traffic or requests | Websites, servers, organizations | Moderate to High | Moderate |

| MITM | Interception of network communication | Network users and organizations | Moderate | Moderate |

| IP Spoofing | Forged source IP address | Networks and Internet services | Moderate | Moderate |

| DNS Poisoning/Spoofing | Manipulation of DNS information | DNS users and organizations | High | Moderate |



---



## Conclusion



Network administrators should focus on three key areas when protecting networks from these threats:



1. **Monitor network traffic:** Continuous monitoring can help identify unusual traffic, suspicious connections, and possible attacks.

2. **Use layered security controls:** Firewalls, encryption, authentication, DNS security, filtering, and rate limiting provide multiple layers of protection.

3. **Keep systems secure and updated:** Regular updates, secure configurations, and appropriate security policies reduce opportunities for attackers to exploit weaknesses.



Understanding common network threats and applying appropriate preventive controls helps organizations maintain the confidentiality, integrity, and availability of their network resources.



---



## References



1. National Institute of Standards and Technology (NIST) — https://www.nist.gov/

2. Cybersecurity and Infrastructure Security Agency (CISA) — https://www.cisa.gov/

3. MITRE ATT&CK — https://attack.mitre.org/

4. SANS Institute — https://www.sans.org/


