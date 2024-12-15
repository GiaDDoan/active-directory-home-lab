# Active Directory Project

![active-directory-schema](https://github.com/user-attachments/assets/e6462b6d-8240-43b5-9f1e-0429f76162e3)

## Objective

In my Active Directory Lab project, I aimed to showcase the process of building a home lab environment focused on learning Active Directory management and security. My goal was to create an environment that simulates real-world IT infrastructure and supports both blue team and general IT skill development. This comprehensive, hands-on project involved configuring an Active Directory domain, deploying assets such as Windows Server 2022, Windows 10, Kali Linux, and Splunk, and ingesting logs for event monitoring.

I concluded the project by using Kali Linux to conduct a brute-force attack on the domain and leveraging Splunk to observe and analyze the generated telemetry. I also incorporated Atomic Red Team for further testing and analysis. This immersive experience helped me deepen my understanding of Active Directory administration, domain structure, and cybersecurity monitoring practices, while building my technical confidence and troubleshooting skills!

I hope this inspires you to try building your own lab environment and see what you can learn!



### Skills Learned

- Gained hands-on experience with Active Directory configuration and administration.
- Enhanced proficiency in setting up and managing a lab environment using virtual machines.
- Improved skills in using Splunk for log ingestion, analysis, and monitoring.
- Developed the ability to detect and analyze telemetry from simulated cyber-attacks.
- Strengthened understanding of brute-force attack methods and their detection.
- Acquired knowledge in deploying and utilizing Sysmon for detailed event logging.
- Fostered critical thinking and problem-solving abilities in a cybersecurity context.

### Tools Used

- VirtualBox for creating and managing virtual environments.
- Windows Server 2022 and Windows 10 for Active Directory setup and domain management.
- Kali Linux for conducting penetration testing and generating attack scenarios.
- Splunk as the SIEM tool for log analysis and telemetry monitoring.
- Atomic Red Team for creating realistic attack simulations and telemetry generation.
- Sysmon for advanced event logging and system monitoring.

## Overview

1. Installed the required Virtual Machines for the project

- AD-Win-10 (Windows 10): Client Machine
- AD-Kali-Linux (Kali Linux): Attacker Machine
- AD-Win-Serv-2022 (Windows Server 2022): Server
- AD-Splunk (Ubuntu): Splunk

![image](https://github.com/user-attachments/assets/86d6328c-eab1-4d59-8720-ce483ea32791)

2. Set up a NAT network, enabling all virtual machines to share the same network and be able to communicate with each other.

![image](https://github.com/user-attachments/assets/baed67dd-3db8-45eb-aca1-615b2626bc28)

3. Installed and configured Splunk on the Splunk Server (Ubuntu).

![image](https://github.com/user-attachments/assets/9d9c2a7a-1e66-48ab-a89e-bc93cdbe217f)

3. Installed and configured Splunk Forwarder and Sysmon on the target machine (Windows 10).

![image](https://github.com/user-attachments/assets/be586e26-dea3-434c-97a8-15d644005f9d)

4. Connected and Sent the target logs to the Splunk Server.

![image](https://github.com/user-attachments/assets/b72f4087-a578-45e0-9987-ec3737c40190)


