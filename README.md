
# Ethical Hacking: A Guide to Cybersecurity Fundamentals 🛡️

*For educational purposes only. Always obtain proper authorization before testing security measures.*  
<img src="https://github.com/user-attachments/assets/faf937aa-8cfd-4298-bb50-149a2e2cb27d" width="800" height="500" alt="Cybersecurity Banner">

---

## Table of Contents
1. [Phishing Attacks](#phishing)
2. [Brute-Force Attacks](#brute-force)
3. [SQL Injection](#sql-injection)
4. [Man-in-the-Middle (MitM) Attacks](#mitm)
5. [Password Cracking](#password-cracking)
6. [Defensive Tools & Strategies](#defense)
7. [Legal & Ethical Guidelines](#legal)
8. [Contribute](#contribute)

---

## <a name="phishing"></a>1. Phishing Attacks

### What is Phishing?
Phishing involves tricking users into revealing sensitive information (e.g., passwords, credit card numbers) via fake emails, websites, or messages.

### Real-World Example: **2013 Target Breach**
- Attackers sent phishing emails to HVAC contractors to steal credentials and infiltrate Target’s network, compromising 40M credit cards.

### Tools & Techniques
- **Offensive**: 
  - **Social-Engineer Toolkit (SET)**: Automates phishing campaign creation.
  - **GoPhish**: Open-source phishing framework.
- **Defensive**: 
  - **Email Filters** (e.g., Mimecast).
  - **User Training**: Simulate attacks with tools like [KnowBe4](https://www.knowbe4.com/).

```bash
# Example: Launching a phishing test with SET
sudo setoolkit
> 1 (Social-Engineering Attacks)
> 2 (Website Attack Vectors)
> 3 (Credential Harvester)


---

## <a name="brute-force"></a>2. Brute-Force Attacks

### What is a Brute-Force Attack?
A method of guessing passwords or encryption keys by systematically trying all possible combinations.

### Real-World Example: **2012 LinkedIn Breach**
- Hackers brute-forced 6.5M SHA-1 hashed passwords using GPU clusters.

### Tools & Mitigation
- **Offensive**: 
  - **John the Ripper**: Password-cracking tool.
  - **Hashcat**: GPU-accelerated cracking.
- **Defensive**:
  - **Rate Limiting**: Lock accounts after failed attempts.
  - **Multi-Factor Authentication (MFA)**.

```bash
# Example: Cracking MD5 hashes with Hashcat
hashcat -m 0 -a 3 hashes.txt ?l?l?l?l?l
```

---

## <a name="sql-injection"></a>3. SQL Injection (SQLi)

### What is SQLi?
Injecting malicious SQL queries into input fields to manipulate databases.

### Real-World Example: **2009 Heartland Payment Systems**
- SQLi vulnerabilities led to the theft of 130M credit card records.

### Tools & Prevention
- **Offensive**: 
  - **sqlmap**: Automated SQL injection tool.
- **Defensive**:
  - **Parameterized Queries**: Use prepared statements in code.
  - **Web Application Firewalls (WAFs)** like ModSecurity.

```bash
# Example: Testing for SQLi with sqlmap
sqlmap -u "https://example.com/login?id=1" --dbs
```

---

## <a name="mitm"></a>4. Man-in-the-Middle (MitM) Attacks

### What is MitM?
Intercepting communication between two parties to steal or alter data.

### Real-World Example: **2017 Equifax Breach**
- Attackers exploited MitM vulnerabilities to intercept unencrypted data.

### Tools & Defense
- **Offensive**: 
  - **Wireshark**: Packet sniffing.
  - **Ettercap**: ARP spoofing tool.
- **Defensive**:
  - **HTTPS Everywhere**: Encrypt web traffic.
  - **Certificate Pinning**.

```bash
# Example: ARP spoofing with Ettercap
ettercap -T -i eth0 -M arp:remote /192.168.1.1// /192.168.1.2//
```

---

## <a name="password-cracking"></a>5. Password Cracking

### Techniques
- **Dictionary Attacks**: Use precomputed wordlists (e.g., `rockyou.txt`).
- **Rainbow Tables**: Precomputed hash lookup tables.

### Tools
- **Offensive**: 
  - **Hydra**: Network login cracker.
  - **Crunch**: Custom wordlist generator.
- **Defensive**:
  - **Password Managers** (e.g., 1Password).
  - **Salting Hashes**: Add random data to passwords before hashing.

```bash
# Example: Generating a wordlist with Crunch
crunch 6 8 0123456789 -o wordlist.txt
```

---

## <a name="defense"></a>6. Defensive Tools & Strategies

### Tools for Security Professionals
- **Snort**: Intrusion Detection System (IDS).
- **Nmap**: Network scanning for vulnerability assessment.
- **OSSEC**: Host-based intrusion detection.

### Best Practices
- Regular penetration testing.
- Patch management (e.g., Automox).
- Security audits with **OpenVAS** or **Nessus**.

---

## <a name="legal"></a>7. Legal & Ethical Guidelines
- **Never test systems without written permission**.
- Follow frameworks like **OSSTMM** (Open Source Security Testing Methodology Manual).
- Report vulnerabilities responsibly (e.g., via HackerOne).

---

## <a name="contribute"></a>8. Contribute
- **Submit Pull Requests**: Improve accuracy or add new sections.
- **Report Issues**: Flag outdated tools or methods.
- **Share Responsibly**: Ensure content is used ethically.

---

**License**: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)  
**Maintained by**: [Aditya Solanki](https://github.com/1uci1er) | **Disclaimer**: For educational use only.
```

---

### How to Use This Guide:
This structure balances offensive examples (for understanding attacks) and defensive strategies (for building resilience), making it ideal for a GitHub repo focused on ethical hacking education.
