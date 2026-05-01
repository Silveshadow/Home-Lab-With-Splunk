# Home Lab with Splunk
I created a SIEM manager and a SIEM agent account to experience a real work SOC environment.

## Project Overview 

In this first photo I created a virtualized lab environment using Oracle VirtualBox to simulate an enterprise security infrastructure. Within this environment, I deployed a Linux-based virtual machine using an Ubuntu ISO image, ensuring a stable and widely supported operating system for security operations.

![Step 1.png](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%201.png)


# Step 2:

 In the second photo I configured the virtual machine with appropriate system resources, including sufficient CPU allocation, memory, and storage. This step was critical to handle log ingestion, indexing, and real-time analysis workloads typically associated with SIEM platforms.


![Capture](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%202.png)

# Step 3

After establishing the system baseline, I installed and configured the Wazuh SIEM solution via the command-line interface. This included adding the official Wazuh repository, importing GPG keys for package verification, and executing the automated installation script. The deployment successfully initialized core components such as the Wazuh manager, indexer, and dashboard, enabling centralized log collection, threat detection, and security monitoring capabilities. I also created credentials to login to the dashboard.

![Capture3](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%203.png)

# Step 4

I accessed the Wazuh dashboard by navigating to the Linux host’s IP address over HTTPS (port 443), confirming secure connectivity to the SIEM interface.


![Capture2](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%204.png)

# Step 5

Upon successful authentication, I reviewed the centralized dashboard, which provided visibility into security events, alerts, and identified vulnerabilities across the environment. The interface allowed me to monitor alert severity levels and gain insight into potential threats and system exposures in real time.


![Capture2](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%205.png)

# Step 6

To extend endpoint visibility, I deployed the Wazuh Agent on a Windows system. After installation, I configured the agent to communicate with the Wazuh manager by specifying the manager’s IP address and importing the authentication key. This enabled secure registration of the endpoint.

![Capture2](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%206.png)

# Step 7

During the initial deployment, the Wazuh agent failed to connect to the manager, as indicated in the log: the connection attempt to 192.168.86.209:1514 was unsuccessful. Upon investigation, it was determined that the authentication key configured on the agent was incorrect, preventing successful communication with the SIEM manager.

![Captureii](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%207.png)

# Step 8

After retrieving the correct authentication key, the agent was reconfigured and successfully started.

![Capture;;](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%208.png)

# Step 9

Cheching the logs confirmed that the agent established a connection with the Wazuh manager, and all relevant modules, including File Integrity Monitoring (FIM), initialized correctly. Policy evaluations and security configuration assessments executed as expected, indicating the agent is now fully operational and actively monitoring the endpoint.

![eee](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%209.png)

# Step 10

I went back to my linux virtual machine and saw that the agent account was able to connect to the SIEM manager

![Capturedd](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%2010.png)

#Step 11

Finally, I was able to review the most recent alerts demonstrating that the agent is actively collecting and forwarding security telemetry to the manager. The alert data includes detailed system and network activity, indicating that monitoring and compliance modules are functioning as expected.

![Capturedd](https://github.com/Silveshadow/Home-Lab-with-SIEM-Tool-and-Manager-Wazuh-/blob/main/Step%2011.png)

