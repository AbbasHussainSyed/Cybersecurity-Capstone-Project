
# Metasploitable VM Security Project

## Overview
This project involved identifying and mitigating vulnerabilities on a Metasploitable virtual machine. The primary goal was to enhance the security posture of the VM by applying patches, securing network services, and configuring firewalls.

## Tools Used
- **Nmap**: For network scanning and port identification.
- **Metasploit**: For vulnerability assessment and exploitation testing.

## Steps Taken
1. **Vulnerability Identification**:
    - Conducted a comprehensive scan using `nmap` to identify open ports and services.
    - Used `Metasploit` to exploit known vulnerabilities and gather information on potential weaknesses.
    
    ```bash
    nmap -sV -O 192.168.1.100
    msfconsole
    ```

2. **Vulnerability Mitigation**:
    - Applied necessary patches and updates to the system.
    - Disabled unnecessary services running on open ports.
    - Implemented strict firewall rules to limit access to essential services only.
    
    ```bash
    sudo apt-get update && sudo apt-get upgrade
    sudo systemctl disable [service_name]
    sudo ufw allow from [trusted_ip] to any port [port_number]
    sudo ufw enable
    ```

3. **Securing Ports**:
    - Closed non-essential ports and secured necessary ones using firewall configurations.
    - Verified the security of the remaining open ports by ensuring they had proper authentication and encryption mechanisms in place.
    
    ```bash
    sudo ufw deny 23/tcp
    sudo ufw allow 22/tcp
    sudo ufw status
    ```

## Findings
- Several critical vulnerabilities were identified and successfully mitigated.
- Open ports such as FTP (21), Telnet (23), and HTTP (80) were secured or disabled as appropriate.
- Implemented best practices for firewall configurations, reducing the attack surface significantly.

## Conclusion
This project provided hands-on experience in vulnerability management, penetration testing, and system hardening. The actions taken significantly improved the security of the Metasploitable VM, demonstrating practical skills in cybersecurity.

## Documentation
A detailed document of findings and remediation steps is available upon request.
